
| Requirement                                                                         | Charachterstic | Importance |
|-------------------------------------------------------------------------------------|----------------|------------|
| Update within 5 minutes means we need an every minute batch or streaming approach.  | Performance    | Y          |
| 5 minutes per month downtme is 4 nines SLI, so system should be reliable.           | Availability   | Y          |
| 800ms for web and 1.4s for mobile means system should be performant (CDN, Caching). | Responsiveness | Y          |
| Work internationaly means system should be geo distributed.                         |||
| 2 milions active user is requirement for DB/workers                                 | Elasticity     ||
| 15 milions users size of DB.                                                        | Scalability    ||