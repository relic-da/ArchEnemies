
### Driving Architecture Characteristics

| Requirement                                                                         | Charachterstic | Importance |
|-------------------------------------------------------------------------------------|----------------|------------|
| Update within 5 minutes means we need an every minute batch or streaming approach.  | Performance    | Y          |
| 5 minutes per month downtime is 4 nines SLI, so system should be reliable.          | Availability   | Y          |
| 800ms for web and 1.4s for mobile means system should be performant (CDN, Caching). | Responsiveness | Y          |
| 2 millions active user is requirement for DB/workers                                | Elasticity     ||
| 15 millions users size of DB.                                                       | Scalability    ||
| 15 millions users size of DB.                                                       | Scalability    ||


### Implicit Architecture Characteristics

| Requirement                                                     | Charachterstic | Importance |
|-----------------------------------------------------------------|----------------|------------|
| Scan email via API and user forwards email via rule or manually | Security       |            |
| Store user personal data for long time                          | Security       ||
| Easy integration with GDS and travel agencies globally          | Extensibility  ||
