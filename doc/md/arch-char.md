
We started qualifying requirements and mapping them with significant architecture characteristics. We grouped them into driving and implicit characteristics. We also referred [Architecture characteristic worksheet](/assets/architecture-characteristics-worksheet.pdf) for this exercise. 

We will use driving characteristics to identify potential suitable architecture styles and implicit characteristics are important to be taken into account while implementing the most preferred architecture style or combination of them. We referred [Architecture Style Worksheet](/assets/architecture-styles-worksheet.pdf) to map architecture characteristics with architecture style.

### Driving Architecture Characteristics


| Requirement                                                                         | Characteristic  | Importance |
|-------------------------------------------------------------------------------------|-----------------|------------|
| Update within 5 minutes means we need an every minute batch or streaming approach.  | Performance     | Y          |
| 5 minutes per month downtime is 4 nines SLI, so system should be reliable.          | Fault Tolerance | Y          |
| 800ms for web and 1.4s for mobile means system should be performant (CDN, Caching). | Responsiveness  | Y          |
| 2 millions active user is requirement for DB/workers                                | Elasticity      ||
| 15 millions users size of DB.                                                       | Scalability     ||
| 15 millions users size of DB.                                                       | Scalability     ||


### Implicit Architecture Characteristics

| Requirement                                                     | Characteristic | Importance |
|-----------------------------------------------------------------|----------------|------------|
| Scan email via API and user forwards email via rule or manually | Security       |            |
| Store user personal data for long time                          | Security       ||
| Easy integration with GDS and travel agencies globally          | Extensibility  ||
