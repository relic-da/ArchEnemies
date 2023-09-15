# Yearly reports

## Description

## Interaction

```plantuml
title Yearly reports use case
!theme aws-orange
skinparam BackgroundColor white
skinparam actorstyle awesome
autonumber 1

participant "Reporter" as reporter
participant "Booking CRUD" as booking_crud
participant "Reporter" as reporter
participant "Booking DB" as booking_db
participant "Reporting Storage" as reporting_storage
participant "App" as app
actor "User" as user

reporter -> booking_crud: Get data
booking_crud -> booking_db
booking_db -> reporting_storage: Poll every minute
note right
Getting finished
bookings per user
end note
reporting_storage -> reporter
reporter -> app
app -> user

```
