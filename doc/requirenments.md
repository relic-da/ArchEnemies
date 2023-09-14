# Requirenments

## Functional

## Architecture Characteristics

### Performance

Travel updates must be presented in the app within 5 minutes of generation by the source 

### availability

5 minutes per month downtme is 4 nines SLI, so system should be reliable

### Responsiveness

800ms for web and 1.4s for mobile means system should be performant

### Elasticity

2 mil active user per week, and 15 milion users registerd.
Each of the user can become active user. As consequence the system will have to poll
mails for all the active users.

### Scalability

15 milions users accounts
