# Booking added via email scan

## Description

End user has integrated Road Warrior application with their email accounts in order to have add them easily. When a new booking information is received via email on their accounts Road Warrior application will transparently add the new booking to the user dashboard in case it is not already managed and notify the user.

## Interaction


```plantuml
@startuml use_case_markdown_filename
!theme aws-orange

skinparam BackgroundColor white
skinparam actorstyle awesome
autonumber 1

actor "User" as user
'participant "Mail\npoller" as mail_poller
'participant "Mail\nlistener" as mail_listener
'participant "Mail\nfilterer" as mail_filterer
'participant "Booking\ninterface" as booking_interface
'participant "Booking\nstorage" as booking_storage
'participant "Booking\ntracker" as booking_tracker
'participant "Notifier" as notifier
'participant "Agency\nconnector" agency_connector
'participant "GDS\nconnector" as gds_connector
'participant "Sharer" as sharer
'participant "Social Media\nconnector" as social_connector
'participant "Help\nGateway" as help_gateway
'participant "Data\nExporter" as data_exporter
'participant "Analytics\nGenerator" as analytics_generator
'participant "Analytics\nStorage" as analytics_storage
'participant "Analytics\nExporter" as analytics_exporter
'participant "Web" as web
'participant "App" as app

@enduml
```
