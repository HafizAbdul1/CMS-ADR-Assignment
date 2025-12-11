# Authentication Method

## Context
The CMS needs a secure authentication system whilst also adhereing to role-based access control.
* The system uses react for the front-end.
* The system uses .NET for the back-end.
* The system uses PostGREsql for the database.

## Potential authentication choices.

* Json Web Token (JWT)
* Session-Based Authentication.



## JWT Discussion
JWT is a compact and self-contained way for securely transmitting information between parties (JWT,n.d) .
This is important beacuse the case study requires us to create a system using a multi-tenant approach,where two tenants should not be able to access each others data.
JWT fulfills this requirement as it does not use shared sessions, where we would use a central session store, this would increase the likeliness of cross-tenant data leaks. 
However, an implication of JWT is that it may carry security concerns, if the token stores sensitive data such as a password, this is important as the CMS will be operating with major organisations who will bring millions of consumers for the CMS.
Another option was session-based authentication where all session information would get stored in the same server (SuperTokens,2024), this is a red flag for the CMS system as we need to avoid data breaches.
Furthermore, using the same server to store all session id would be highly inefficient, as we would increase memory overhead, which goes against our non-functional requirements (NFR04,NFR05).
However, a benefit of session-based authentication is that it only stores session IDs, reducing the risk of potential data breaches.

Overall, i have decided to use JWT for authentication. Firstly, it follows more non-functional requirements than session-based authentication scalability (NFR01), as there is not much server memory overhead. It also complies by multi-tenancy requirements, due to its data isolation (NFR07), leading to imporved security in the CMS.
Lastly as we are using a service-based approach, its important that services can approve and reject authentication without relying on each other. For example, if a consumer were to use the complaint service, the service can check the user's role from the JWT token, rather than depending on the role service, which is important for scalability in the future.

## Role-Based Access
The system will use a role-based access control, which grants different user roles. This is important as the system will have 5 different users that have different roles in the system.
This includes
* Consumer
* Help-Desk Agent
* Help-Desk Manager
* Support Staff
* System Administrator

Role-Based-access-control is implemented in the system by storing the roles in a database table, where each role would have its own RoleID. 
This is my roles table in my database.

<img width="477" height="275" alt="image" src="https://github.com/user-attachments/assets/4748843d-04ba-42da-b686-13c3d8fb70b7" />

 
## References
* Introduction to JSON Web Tokens,JWT Debugger [https://learn.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/common-web-application-architectures](https://www.jwt.io/introduction#what-is-json-web-token)
* Session-Based Authentication: A Detailed Guide [2024], SuperTokens https://supertokens.com/blog/session-based-authentication#what-is-session-based-authentication
