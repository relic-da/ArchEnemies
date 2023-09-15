# Analytical metrics are generated and exported to 3rd parties

[Home](../../README.md#use-cases)

## Description

(Simplest use-case as a start, monthly batch data exports. Extensions: 3rd-parties can read from API, streaming metrics, dashboards, etc.)
Data analytics generator creates statistical reports on a scheduled basis and stores them in Analytics storage. Analytics exporter reads the metrics from Analytics storage and delivers them to 3rd parties.

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
## Observations

Analytics monetization is a crucial point for the system, since it brings revenue for the company. Data analytics generator and Analytics storage components need to be scalable to handle ever growing amout of users, their bookings, and new types of metrics. Extensibility is in the foundation of the Analytics exporter component so that new ways to deliver metrics and make the 3rd parties engaged can be added.
