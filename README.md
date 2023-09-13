# O'Reilly Architecture Katas 2023 - ArchEnemies

## Members

- Alvaro Salvador [LinkedIn](https://www.linkedin.com/in/alvarorafael/]
- Anand Bajpai [LinkedIn](https://www.linkedin.com/in/bajpai-anand)
- Constantine Korobov [LinkedIn](https://www.linkedin.com/in/ckorobov/)
- Mirco Paccusse [LinkedIn](https://www.linkedin.com/in/mirco-paccusse-97525012/)
- Sergiy Shelekh [LinkedIn](https://www.linkedin.com/in/proxitrone/)

## Problem/Mission

- [Problem statement](/problem.md)
- [Additional Clarifications](/doc/glosary.md)
- [Requirements](/doc/requirenments.md)
  - [Business / Functional](/doc/requirenments.md#functional)
  - [Technical/Architecture](/doc/requirenments.md#architecture-characteristics)
- Assumptions and Constraints

## Solution

- Actors and Actions
- Event Storming [[about](https://www.eventstorming.com/)]
- [[Q: Where do we priortize actions?]]
- [ADR](/doc/adr)
- Architecture Analysis
  - Architecture Characteristics
    - Identify *driving* architecture Characteristic using [Architecture Characteristics Worksheet](https://www.developertoarchitect.com/downloads/architecture-characteristics-worksheet.pdf) and small description why they are relevent
    - Mark top three driving Characteristics
    - | Rank | Characteristic | Relevence |
    - [[Q: How we mention implicit and other characteristics? ]]
  - Architecture Style
    - Start with mention that
      - analysis is done technology agnostic [cloud/on prem ]
      - end goal is to guide techinal implementation and not specify tools and softwares
      - Refer [Architecture Styles Worksheet](https://www.developertoarchitect.com/downloads/architecture-styles-worksheet.pdf) and identify 2/3 style which match well
      - Refer ADRs for different styles evalauted
      - Confirm decision and add iterate the reason.
- Domain Design [[Q: Would this come first of Architecture Styles?]]
- System Architecture
  - Services [In case of microservices]
  - Core and Plugins [In case of microkernel]
  - Core [made of Services] and Plugin Design [microservices + microkernel]
  - Other details based on style chosen

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
