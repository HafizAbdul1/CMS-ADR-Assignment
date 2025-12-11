# Data Transfer Objects

## Context and Problem Statement
As the system handles alot of sensitive data, there is increased risk of database entities being exposed to front-end users (ASP.NET,2022).

# Considered Options
## DTOs
* DTOs are used so that clients can't see specific data, which helps reduce over-posting. This is important as it helps follow security requirements(NFR11).
* Using DTOs helps isolate data models from the front-end (learn.microsoft,2015), not only optimising data transfer but also improve data security (NFR07).

## Database Entities
* This is not an ideal choice as it increase security concerns, due to the fact that you overpost sensitive data.

## Chosen Option
I have chosen to use DTOs, even though it may increase complexity in the system, it is a key decision in terms of security as it is needed in all operations in the system including submitting complaints, assigning complaints and also changing user roles.
Therefore, it is important to be able to display this functionality of DTOs.
## References
* Create Data Transfer Objects (DTOs),ASP.NET (2022)[ https://martinfowler.com/articles/microservices.html](https://learn.microsoft.com/en-us/aspnet/web-api/overview/data/using-web-api-with-entity-framework/part-5)
* Cutting Edge - Pros and Cons of Data Transfer Objects, LEARN.MICROSOFT (2015) https://learn.microsoft.com/en-us/archive/msdn-magazine/2009/brownfield/pros-and-cons-of-data-transfer-objects
