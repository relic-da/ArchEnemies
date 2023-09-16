# O'Reilly Architecture Katas 2023 - ArchEnemies

* [Members](#members)
* [Mission The Road Warrior](#mission-the-road-warrior)
  * [Challenge](#challenge)
* [Approach](#approach)
* [Actor/Action](#actor/action)
* [Use cases](#use-cases)
* [Architecture Analysis](#architecture-analysis)
* [Architecture Modeling](#architecture-modeling)
* [ADR](#adr)
* [Deployment](#deployment)
* [Cost Analysis](#cost-analysis)
* [Architectural Fitness](#architectural-fitness)
* [References](#references)

## Members

- Alvaro Salvador [LinkedIn](https://www.linkedin.com/in/alvarorafael/)
- Anand Bajpai [LinkedIn](https://www.linkedin.com/in/bajpai-anand)
- Constantine Korobov [LinkedIn](https://www.linkedin.com/in/ckorobov/)
- Mirco Paccusse [LinkedIn](https://www.linkedin.com/in/mirco-paccusse-97525012/)
- Sergiy Shelekh [LinkedIn](https://www.linkedin.com/in/proxitrone/)

## Mission The Road Warrior

![](/assets/logo_road_warrior.png)

>A new startup wants to build the next generation global online trip management dashboard to allow travelers to see all of their existing reservations organized by trip either online (web) or through their mobile device. Build a sustainable architecture for same.


### Challenge

- [Problem statement](/doc/md/problem.md)
- [Additional Clarifications](/doc/md/clarification.md)
- [Glossary](/doc/md/glossary.md)

## Approach

We follow actor/action model to begin with. We identify the actors and actions they need to perform. We, then, create components which will enable actors to perform specific actions. Next, we find interactions among actors. This provides us high level view of actors components required in the system, their relation to stakeholders and their (inter)dependency. 

We create use case diagrams to visualize the functional requirements to assists us making design choices and understanding the system on more granular level.

Now we understand the desired system behavior better so we qualify the requirements to identify architecture characteristics. These characteristics help us identify the most suitable architecture style for the solution. 

We use C4 model technique to design the architecture, starting with most abstract view of the system and going further in details in each step.

We use ADR approach to make a informed decision for all important architecture decisions.

## Actor/Action


![](/doc/actor-action.png)


## Use cases

- [User adds booking manually](./doc/use_cases/user_add_booking_manually.md)
- [Booking added via email scan](./doc/use_cases/booking_added_via_email_scan.md)
- [User shares trip information in social media](./doc/use_cases/user_share_trip_on_social_media.md)
- [User shares trip information with other user(s) ](./doc/use_cases/user_share_with_other_user.md)
- [Agency updates booking status](./doc/use_cases/agency_updates_booking_status.md)
- [User personal yearly reports](./doc/use_cases/user_yearly_report.md)
- [Data analytics and information access](/doc/use_cases/analytics_and_reporting.md)

## Architecture Analysis

- [Identify architecture characteristics](./doc/md/arch-char.md)
- [Identify deserving architecture style(s)](./doc/md/arch-style.md)
- [Components](./doc/md/components.md)

## Architecture Modeling C4

> The C4 model is an "abstraction-first" approach to diagramming software architecture, based upon abstractions that reflect how software architects and developers think about and build software.

* [Context](doc/c4/context.md)
* [Container](doc/c4/container.md)
* Components
  * [Booking Core](doc/c4/component-booking-core.md)
  * [Mail integration](doc/c4/component-mail-integration.md)
  * [Notifier](doc/c4/component-notifier.md)
  * [Analytics](doc/c4/component-analytics.md)
  * [Front End](doc/c4/component-front-end.md)

## ADR

- [Space based architecture style](/doc/adr/0001-arch-style-space-based.md)
- [Microservices vs Event driven architecture style](/doc/adr/0002-arch-style-microservices-vs-event-driven.md)
- [Dedicated storage for analytics](/doc/adr/0003-dedicated-db-for-analytics-usage.md)
- [Storing agency contact details for help](/doc/adr/0004-store-agency-contact-for-help.md)
- [One Analytics Generator for yearly user report and other analytics](/doc/adr/0005-data-reporter-and-analytics-generator.md)
- [Analytics generator and Analytics exporter](/doc/adr/0006-analytics-generator-and-analytics-exporter.md)
- [Efficient erythemal for booking tracker](/doc/adr/0007-efficient-oriented-algorithm-for-booking-tracker.md)

## Deployment

## Cost Analysis

## Architectural Fitness

Mention that continuously testing/checking th solution for architectural fitness is critical.

## References

Though it is not possible to mention every source material we were benefitted from, while working on this solution, we would lile to mention following as noteworthy

1. [Developer to Architect](https://www.developertoarchitect.com/)
2. [Fundamentals of Software Architecture](https://www.oreilly.com/library/view/fundamentals-of-software/9781492043447/)
3. [Software Architecture Patterns](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/)
4. [O'Reilly Software Architecture Kata Entries](https://github.com/tekiegirl/SoftwareArchitectureResources/blob/main/Resources/OReillyKata.md)
5. [C4 Model](https://c4model.com/)
