# Choice of Tech Stack

## Context
A technology stack is needed for this project.



## Chosen Options

* React
* ASP.NET
* PostgreSQL


## Discussion
For the front-end of this project, i have decided to use React . The reason why i have used React is because it uses component-based architecture (React,n.d.), this is important for this CMS as it means that we can integrate other features such as a chatbot in the future without  having to recoding the entire codebase.
Furthermore, this is also important as it allows the system to be more scalable, allowing extensability in the future as ABC Limited want to target other continents .However, a disadvantage of this component-based architetcture is that for bigger organisations it can introduce complexity as they may use more components.

For the back-end of this project, i have decided to use ASP.NET.The reason I'm using this is that it is a strong, robust foundation for RESTful APIs, which is important as I'm using a SOA. Another reason for this is because it provides much needed security for the system, as the system follows industry standard authentication protocols (dotnet, n.d.). This is important as ABC limited want a secure multi-tenant approach system that has data privacy, where 2 organisations can not see each others data.

I am using PostgreSQL as it has a high availability and sacalibility (azure.microsoft, n.d.) , this means that any potential downtime is reduced. This is important as this system will be a 24/7 system. Furthermore, it provides data integrity and data security, which is also important for the CMS, as we need to ensure that two tenants cannot access each others data.

## References
* Describing the UI, React (n.d.) https://react.dev/learn/describing-the-ui
* ASP.NET, dotnet (n.d.) https://dotnet.microsoft.com/en-us/apps/aspnet
* Azure Database for PostgreSQL, azure.microsoft (n.d.) https://azure.microsoft.com/en-gb/products/postgresql/?ef_id=_k_Cj0KCQiArOvIBhDLARIsAPwJXObkoi3RjG6X0qWX_VLmVUyhEqEIiZ_N7TrOPlB6p2ZW5lBtWthul-EaAgi7EALw_wcB_k_&OCID=AIDcmm3bvqzxp1_SEM__k_Cj0KCQiArOvIBhDLARIsAPwJXObkoi3RjG6X0qWX_VLmVUyhEqEIiZ_N7TrOPlB6p2ZW5lBtWthul-EaAgi7EALw_wcB_k_&gad_source=1&gad_campaignid=1635232712&gbraid=0AAAAADcJh_slLi2Z4dC10ACxAkpNinl06&gclid=Cj0KCQiArOvIBhDLARIsAPwJXObkoi3RjG6X0qWX_VLmVUyhEqEIiZ_N7TrOPlB6p2ZW5lBtWthul-EaAgi7EALw_wcB
