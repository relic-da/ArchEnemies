# User adds manually a booking into the system

[[_TOC_]]

## Description

End user uses mobile app or public web interface and adds manually a booking PNR which has been already arranged upfront by the user. This new booking will be set by the user as part of an existing or new trip which will be shown in the dashboard and tracked.

## Interactions

### Booking addition

<div hidden>

```plantuml
@startuml user_add_booking_manually
!theme aws-orange

skinparam BackgroundColor white
skinparam actorstyle awesome
autonumber 1

actor "User" as user
participant "App/Web" as app
participant "Booking\ninterface" as booking_interface
participant "Agency\nconnector" as agency_connector
participant "GDS\nconnector" as gds_connector
participant "Agency/GDS/Third parties\nStandard API" as third_parties
participant "Booking\nstorage" as booking_storage
participant "Booking\ntracker" as booking_tracker

user -> app: Add new booking
app -> booking_interface: POST operation
booking_interface -> agency_connector
agency_connector -> third_parties

alt Response NOK
   third_parties --> agency_connector
   agency_connector --> booking_interface: Return error
   booking_interface --> app: Report error looking up the booking
   app --> user: Report error
   note over user
      App shows suggestion on how to recover
      from error if related with non valid
      booking PNR
   end note
else Response OK
   third_parties --> agency_connector
   agency_connector --> booking_interface
end

booking_interface -> booking_storage
return Confirm operation
booking_interface --> app: Confirm operation
app --> user: Show trip and booking data
note over user
   Rich information regarding the
   booking is shown
end note
@enduml

```
</div>

![user_add_booking_manually](./user_add_booking_manually.svg)

### Booking tracking

<div hidden>

```plantuml
@startuml booking_tracking
!theme aws-orange

skinparam BackgroundColor white
skinparam actorstyle awesome
autonumber 1

participant "Booking\ntracker" as booking_tracker
participant "Booking\ninterface" as booking_interface
participant "Booking\nstorage" as booking_storage
participant "Agency/GDS\nconnector" as agency_connector
participant "Agency/GDS/Third parties\nStandard API" as third_parties
participant "Notifier" as notifier
participant "App/Web" as app
actor "User" as user

booking_tracker -> booking_interface: Query active bookings
booking_interface -> booking_storage: Query
return Relation of active bookings
note right
   Active bookings are either bookings which:
   - Are part of an active trip defined by user
   - Have not being reported as cancelled by\n
     the relevant agency/supplier
   - Finalization date has not being reached
end note
booking_interface --> booking_tracker: Response
booking_tracker -> agency_connector
agency_connector -> third_parties
return Booking status
agency_connector --> booking_tracker: Booking status
== Booking change detected ==
note over booking_tracker
   If a meaningful change in the booking status
   is confirmed, notification workflow starts
   to inform end user
end note
booking_tracker -> notifier: POST end user message
notifier -> app: Render message on interface or mobile notification
app -> user

@enduml

```
</div>

![booking_tracking](./booking_tracking.svg)
