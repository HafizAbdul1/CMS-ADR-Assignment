# Multi Tenant Approach

## Context 

The CMS requires a multi-tenant approach where two tenants should not be able to access each others data. For example, Natwest should not be able to access LLoyds information and vice versa.

## Discussion
There is many ways to approach this problem.
Icluding:
* Shared Databases for all tenants.
* Seperate Databases for all tenants.

## Discussion
Shared database is one way to approach this problem, this is where all tenants would share the same database but would get differentiated thorugh TenantID. 
<img width="703" height="185" alt="image" src="https://github.com/user-attachments/assets/de6c0c11-2430-40c0-955e-f3790eb1443e" />

* An advantage of this is that it easy quick and easy to onboard new tenants, which is important for this system, as it looks to target larger markets in the future. 
* A disadvantage of this is that, that its less secure due to a shared database.

Seperate databases would mean that each tenant would have their own databases. 
* An advantage of this is that it provides the most data isolation, improving security (NFR11).
* A disadvantage of this is that it is harder to scale in the future, which is important (NFR01).

## Chosen Option

I have chosen a shared database for the proof-of-concept, as it allows faster development of the system and also reduces memory storage, which is beneficial for performance requirements (NFR04).
However, if this was to be a complete syste, it would be wiser to choose seperate databases, as it provides more security and data isolation, a key requiremment of the system.


