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

Chosen option: "Service-Oriented Architecture", because it provides important characteristics needed for the system, such as interoperability.
This is an important attribute as it allows systems to exchange data/information with one another. 
The CMS should use a multi-tenant approach as it will have different Tenants, such as Vodafone and EE, who may use different external systems, such as SMS systems.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Service-based architecture is good because it has a high reliability since it is easier to debug small services than large amounts of code.
* Service-based architecture is also good because it allows extensibility for the future, so the system can incorporate chatbots and other services.
* Service-based architecture may be bad because it can be highly complex to manage services, especially for larger businesses.
* Service-based architecture may also be bad because it can require a high initial investment, this is important as ABC limited still need to seek for capital funding.

