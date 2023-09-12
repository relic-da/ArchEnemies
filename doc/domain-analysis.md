# Domain analysis

## 2023-09-12

```
@startuml firstMeeting
skinparam handwritten true
hide stereotype

left to right direction

'skinparam linetype ortho

skinparam rectangle{
    BackgroundColor WhiteSmoke
    borderColor black
    LineColor<<actor>> #86B56B
    borderColor<<actor>> #86B56B
    BackgroundColor<<actor>> #D6E8D5
    LineColor<<actor>> #D6E8D5
    RoundCorner<<actor>> 15

    borderColor<<action>> #3F75BB
    FontColor<<action>> #3F75BB
    BackgroundColor<<action>> #FFE5CC
'    RoundCorner<<action>> 30

    BackgroundColor<<sticky>> #F3D22B
    borderColor<<sticky>> black
 }


rectangle Actors {

    rectangle system  <<actor>> [
    System
    ]
    rectangle user <<actor>> [
    User
    ]
    rectangle supplier <<actor>>[
    Supplier
    ]
    rectangle email_prvider <<actor>> [
    Email Provider
    ]
}

' position actors
'
user                 .[hidden]                      system       
supplier             .[hidden]                      user         
email_prvider        .[hidden]                      supplier     


' action

rectangle mail_poller [
**Mail Poller**
——-

Get mail 
From provider
]

rectangle mail_filter [
Mail
Filter
]

rectangle booking_logger [
Booking Logger
]

rectangle travel_updates

rectangle booking_manual [
Booking
—-
* add
* update
* Delete
]

rectangle sharer  [
Sharer
]

rectangle help 

rectangle booking_viewer  [
Booking Viewer
]

rectangle booking_keeping 

rectangle data_reporter  [
Data Reporter
]

booking_viewer            .[hidden]               sharer
sharer                    .[hidden]               booking_manual
booking_manual            .[hidden].               help

' Links 
user -[#black]-- sharer
user -[#black]-- booking_viewer
user -[#black]-- booking_manual
user -[#black]-- help


supplier <... travel_updates

email_prvider <--- mail_poller

system .... data_reporter

'
' connectivty intermediate
booking_viewer   <..    data_reporter
'
help             .      travel_updates
booking_viewer   ...    booking_keeping
booking_manual   ...>   booking_keeping
sharer           ...    booking_keeping
'
mail_poller      <--    mail_filter

booking_logger   ..>    booking_keeping
'
'
mail_filter      ...    booking_logger
travel_updates   ...>   booking_logger
'
@enduml
```


 

 ![](firstMeeting.svg)
