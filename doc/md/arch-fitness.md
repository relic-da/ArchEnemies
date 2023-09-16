## Architecture Fitness

Architecture fitness implies tow main objectives
- System adheres to the architecture during implementation and expansion over time
- System meets the criteria which were driving and critical for choosing the particular architecture

These objectives are achieved by implementing fitness functions. 

>**Architectural Fitness Function** : any mechanism that performs an objective integrity assessment of some architecture characteristic or combination of architecture characteristics.

In this system, we will measure following criteria to ensure that architecture continuously meets the standards it was design to

**Responsiveness** : System has explicit requirement of responsiveness of its app and web versions. That has to be measured along the time and release. System performance KPIs, delivered by system monitoring can deliver this.

**Fault-tolerance** : System is designed to meet certain criteria in terms of availability and fault-tolerance. 

**Security** : System stores significant person data of users and it needs to be assessed continuously that architecture supports expected level of security. 

The concrete implementation of fitness function for these and other criteria can be done in many ways, depending on tools, technologies and team expertise, however it is recommended to embed fitness function into devOps process and implementing these functions as code. 

There would be some characteristics of the architecture which are not measurable as is, for example, agility or operation efficiency . For such cases, we can map some process KPIs with these and measure them. In particular, deployment time and deployment efficiency can be some good indicators of measuring operating efficiency. 

