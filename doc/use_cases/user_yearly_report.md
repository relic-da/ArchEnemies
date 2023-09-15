# Yearly report is generated and sent to a user

## Description

Data analytics generator creates yearly statistical reports (agregated metrics and views on user data) on a scheduled basis (for all users who need the report before next schedule: weekly/daily) and stores them in Analytics storage. Analytics exporter reads the report from Analytics storage and delivers the report to a user via front-end (and email).

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
