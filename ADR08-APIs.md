# Using APIs

## Context
This CMS uses a service-oriented approach, meaning it has multiple services it relies on. 
APIs are needed for this system as for example, the CMS system could expose an API that asks a consumer for their name.

## Considered Options

* RESTful API
* graphQL


## Discussion
RESTFul APIs can be used in this system as react would communicates with .NET through rest APIs, this action would be done in a safe and secure manner(aws, n.d)
An advantage of RESTful Apis is that they are scalable, this is because REST Apis optimiste consumer-server interactions, meaning improved performance (NFR05). 
This means that the .net server would not have to keep previous consumer information, leading reduced memory overhead. This is important as this improve scalability (NFR01) for the long-term, due to optimised storage and communication.
However, a disadvantage is that it is less efficient in a more complex complete CMS.

Another option was using graphQL, an advantage of this was that is had efficient data fetching ( GeeksforGeeks,2025), this means that help-desk agents can request for only data they need, for example UserId and the ComplaintId. 
This is important as it improves security measures in the system (NFR11).
However, graphQL is a very complex system to set up, which could impact system performance, which goes against (NFR05) 
## Chosen option
I have chosen to go for RESTful APIs as it compliments my technology stacks and also its very useful for debugging. 
<img width="1015" height="654" alt="image" src="https://github.com/user-attachments/assets/d1feb18b-7556-4b2b-b8e7-d86510fe81ec" />

## References
* What is a RESTful API?, AWS (n.d) https://aws.amazon.com/what-is/restful-api/#:~:text=RESTful%20API%20is%20an%20interface,applications%20to%20perform%20various%20tasks.
* Advantage & Disadvantage of GraphQL, GeeksforGeeks (2025) https://www.geeksforgeeks.org/graphql/advantage-disadvantage-of-graphql/
