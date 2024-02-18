

# Table of Contents

- [Introduction](#introduction)
- [Types of APIs](#types)
- [API Architecture Types](#architecture_types)
  - [RESTful API Guiding Principles](#guiding_principles)




<br/>
<br/>
<br/>


# Introduction <a name="introduction"></a>

<p>This is our RESTfull API Learning repository page. REST is an acronym for REpresentational State Transfer and an architectural style for distributed hypermedia systems. Roy Fielding first presented it in 2000 in his famous dissertation. Since then it has become one of the most widely used approaches for building web-based APIs (Application Programming Interfaces).

REST is not a protocol or a standard, it is an architectural style. During the development phase, API developers can implement REST in a variety of ways.</p> 




# Types of APIs <a name="types"></a>

<p>Most of the APIs you’ll encounter can be broken down into four main types: Open API, Partner API, Private API, and Composite API.  </p> 

## Open API
Also called Public APIs, these are your completely public access APIs, with no restrictions on who can use them.

## Partner API
These types of API is not open to the public, and access is restricted through the use of specific licenses. Business partners often Make Use Of These APIs. For example, you will see them used between a business and its client as part of a paid online service.

## Private API
Also called internal APIs or enterprise APIs, private APIs are types of APIs that are used only within a single company. These are often used to integrate different company services and streamline workflows.

## Composite API
Composite APIs are a combination of data and service are types of APIs that are used to speed up the execution of certain tasks and improve performance. A composite API can enable these calls to run together as a single service if a task uses multiple API endpoints. An example of this could be a shopping cart for an Ecommerce web application.

br/>
<br/>

# API Architecture Types <a name="architecture_types"></a>

<p>Another way to understand and categorize APIs is by their architecture. An API’s architecture effectively governs what information an API can share and how it does that sharing. Here’s a detailed look at some of the most popular APIs in use today.</p> 

## RESTful API Protocols
REST is short for “representational state transfer” and refers to an architectural style of API. The REST architecture has a set of characteristics that includes 

## SOAP (Simple Object Access Protocol)
SOAP (short for Simple Object Access Protocol) APIs are among the original web services, dating back to Web 1.0 days. 

## XML-RPC
XML stands for “Extensible Markup Language,” and RPC stands for “Remote Procedure Call.” XML-RPC uses XML to encode API calls and HTTP to transport them. 

## JSON-RPC
This is a similar protocol to XML-RPC except for the use of JSON instead of XML.


# RESTful API Guiding Principles <a name="guiding_principles"></a>

## The Six Guiding Principles of REST

 - Uniform Interface
 - Client-Server
 - Stateless
 - Cacheable
 - Layered System
 - Code on Demand (Optional)

<br/>

### For Effectiveness, Maintainability, and Scalability

#### 1. Nouns for Resources: NOT VERBS
To show resources, because verbs show actions.
Example: /users, /posts, /tasks
/users/{id}, /posts/{id}, /tasks/{id}

##### Best Practice: 

Synonymize a resource with a web page.
A resource should have links (HATEOAS) pointing to relative URIs to fetch related info.

#### 2. HTTP Methods: 
Use GET, POST, PUT, DELETE for CRUD operations on resources.

#### 3. HTTP Status Codes: 
To show Request Outcome 
##### Example: 
200 for success, 
401 for unauthorized
404 for not found, 
400 for bad request, 
500 for server errors

#### 5. Plural Nouns for Collections:
Use plural nouns to show collection of resources.
##### Example, /users NOT  /user.

#### 6. Proper HTTP Headers: 
For Additional Info, Cache-Control and Security.
##### Example: Content-Type, Accept, Authorization, etc.

#### 7. Statelessness: 
Each Request will have ALL necessary info for the server. 
DO NOT store client state on server.

#### 8. Pagination: 
For large collections to limit the data amount in a single response.
Improves Performance.
Use query parameters like page and limit.

#### 9. Response Formats: 
Return Responses in a Consistent Format across all endpoints.
Easier API Consumption for Clients.
##### Example: JSON

#### 10. HATEOAS (Hypermedia as the Engine of Application State): 
Include hyperlinks in responses for clients for Dynamic API Navigation

##### Best Practice: 
Include Cache Destroy API link to ALL API

#### 11. Authentication and Authorization:
To secure API endpoints
##### Example: 
Standards like JWT, OAuth

#### 12. Input Validation: 
Validate and sanitize input data 
To prevent security vulnerabilities for data integrity.
##### Example: 
Protect against injection attacks

#### 13. Error Handling: 
Provide meaningful error messages.
Follow consistent error response formats.
To help clients in debugging problems.

#### 14. Documentation: 
Create proper documentation explaining each endpoint.
##### Example: 
Purpose of the API, Required Parameters, Response Format, Usage Examples

#### 15. Testing: 
Test the API endpoints using Automated Testing Tools 
For Functionality, Performance, and Reliability.

#### 15. Compression: 
Response formats like XML, JSON, HTML, or even plain text can be compressed to save bandwidth.

#### 16. Caching: 
Client Cache, API Cache, Query Cache




