# Choice of Architecture for the Complaint Management System

## Context and Problem Statement

ABC Limited wants to create a Complaint Management system for Banking companies and Telecom providers. 
The system should have a multi-tenant approach where there is data privacy between tenants; for example, NatWest should not be able to view Barclays data and vice versa.
The system should also have extensibility for customer expansion in the future, and also integrate an AI chatbot in the future.
For this project, an appropriate architectural style needs to be chosen in order to create a comprehensive and seamless system that supports future scalability.
 
## Considered Options

* Service-Oriented Architecture
* Monolithic Architecture
* Microservices Architecture


## Decision Outcome

Monolithic is one potential architectural style for the CMS project. Monolithic architecture is where all the systems share one unit. This means all the systems would share a singular codebase. A benefit of the Monolithic architecture is that it has high performance, as all the systems are in one place. Whereas the microservices approach requires interoperability, meaning it may take slightly longer for data to be exchanged between systems. However, this means that the style will also have slower development, as we would have to redeploy the whole application rather than small parts.

Microservices Architecture is where the system is made of smaller services (APIs). A benefit of this architecture is that the system has faster development, as you can develop the application in smaller parts, minimising downtime. Whereas the monolithic approach requires the entire system to redeploy. However, a disadvantage of Microservice architecture is that for larger organisations such as NatWest, it may increase complexities as you will need more microservices. 

Service-based Architecture is where the system is made up of small services. A benefit of this architecture is that it has simple system management, because the architecture does not require a vast complex amount of APIs. Whereas the Microservice architecture does. A disadvantage is that this architecture gets moer complex depending on the size of the organisation. However, not as complex as the Microservice architecture.

Chosen option: "Service-Oriented Architecture", because it provides important characteristics needed for the system, such as interoperability.
Interoperability is where different systems have the ability to exchange information with one another. 
The CMS should use a multi-tenant approach as it will have different Tenants, such as Vodafone and EE, who may use different external systems, such as SMS systems.
This means that the Monolithic approach should not be considered. As the system will also cater to large tenants, using a Microservice architecture may make management too complex. Therefore, the service-oriented architecture is the best option.




