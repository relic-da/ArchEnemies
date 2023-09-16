## Deployment



We have proposed a tool agnostic architecture which can be implemented with any available tools that fit the architecture guidance on premise or in cloud.

We have designed system architecture based on unique components which take part in certain actions. 

Having said that, given nature of the system and its ecosystem, in particular, global presence with multiple user interfaces and high responsiveness, required fault tolerance and elasticity suggests that cloud would be a good choice to deploy the system. 

Some key benefits of using cloud are

- **Managed services** : Cloud providers offer a wide range of managed services for almost all use cases. It let team focus on core functionality by reducing operational overhead
- **Elasticity and Scalability** : Cloud providers offer auto-scaling capabilities in almost all their services with system defined boundaries. This optimizes the resource cost of the system in low load time and maintains availability and responsiveness to scale up in time of heavy load. 
- **Global Reach** : All major cloud providers already present globally and in our case it helps with high responsiveness required of the system and in some cases where data has to be stored locally, GDPR too.
- **Security** : Cloud providers work globally with managed services and invest heavily in security and compliance to reduce security and compliance overhead from their clients as much as possible. In particular, cloud providers take care of GDPR, encryption and access control to some extent or provide easy way to do so. This also helps our system to be present globally by meeting compliance requirements with less security overhead and more focus on core functionalities
- **Extreme analytics capabilities** : Cloud providers have launched state-of-the-art analytics products meeting the growing demand of data analytics. These products, combine with other benefits of cloud services, get analytics engines up and running in no time. 
- **Integration** : Cloud providers offer a wide range of integration services which benefits our system in integrating with agencies and our analytics clients.

From our our system architecture, we can identify some components which can be implemented using cloud products offered by leading cloud providers.

| Component/Container | AWS product(s)             | Azure product(s)                                 | GCP product(s)          |
|---------------------|----------------------------|--------------------------------------------------|-------------------------|
| CDN                 | Amazon CloudFront          | Azure Content Delivery Network, Azure Front Door | Cloud CDN               |
| API Gateway         | Amazon API Gateway         | Azure API Management                             | Apigee                  |
| Booking Tracker     | Lambda                     | Azure Functions                                  | Cloud Functions         |
| Analytics           | Amazon S3, Amazon Redshift | Cloud Storage, Azure Event Hubs                  | Cloud Storage, BigQuery |

