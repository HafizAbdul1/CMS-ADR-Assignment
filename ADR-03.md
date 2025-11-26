# Using Data Access Layering

## Context
The CMS exposes multiple domain services that all need to exhange data in the CMS database. 
If these services access the database directly, the business logic becomes tightly coupled to the persistence technology.
This makes it harder to conduct unit testing, which is an important part of the case study. Furthermore, a multi-tenant approach is required, so it is important to be implement this without major changes.
(ASP.NET,2023)




## Options

* Data Access Layering
* Direct Access from CMS API


## Discussion
I have chosen data access layering as it adds a layer of security to the CMS.
This is because direct access from the CMS API would mean that, the DAL services such as Complaint Services would directly contact the database.
This increases the chances of internal data to be exposed, this cannot happen in the system as we cannot bypass multi-tenancy checks, which was a key requirement outlined in the case study. 
Furthermore, adding a DAL will make it easier for the CMS to change the database without making major changes to the system.



## References
* Common web application architectures, .NET(07.2023) https://learn.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/common-web-application-architectures
