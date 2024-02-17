

# Table of Contents

- [Introduction](#introduction)
- [Types of APIs](#types)
- [API Architecture Types](#architecture_types)
 - [Guiding Principles](#guiding_principles)
- [Types of Method](#method_types)



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
SOAP (short for Simple Object Access Protocol) APIs are among the original web services, dating back to Web 1.0 days. However, SOAP APIs are still widely used by enterprises and government systems due to SOAP’s strict, more defined security protocols. Most businesses today would benefit more from the flexibility, simplicity, and reduced bandwidth REST Provides.  

## XML-RPC
XML stands for “Extensible Markup Language,” and RPC stands for “Remote Procedure Call.” XML-RPC uses XML to encode API calls and HTTP to transport them.   The use of the XML format is designed to be both human and machine-readable, which could be useful if you have minimal code knowledge and are willing to learn more. WordPress is one company that makes use of XML-RPC in its platform. 

## JSON-RPC
This is a similar protocol to XML-RPC except for the use of JSON instead of XML. JSON is short for “JavaScript Object Notation” and is similar in that it’s relatively simple to read by humans. It provides maximum browser compatibility and is simpler to implement and use.   Unlike REST and SOAP, both XML-RPC and JSON-RPC can initiate processes on the server. That means they can run scripts, launch applications, start data transfers, and other actions on the server. Not surprisingly, this raises some security concerns. For this reason, you most often see the RPC-style APIs used in internal systems, where there is no concern about external threats.  


# Guiding Principles <a name="guiding_principles"></a>

## The Six Guiding Principles of REST

 - Uniform Interface
 - Client-Server
 - Stateless
 - Cacheable
 - Layered System
 - Code on Demand (Optional)

<br/>
<br/>


# Types of Method <a name="method_types"></a>

### GET Method: 
The most common HTTP method is GET, which returns a representational view of a resource's contents and data. GET should be used in read-only mode, which keeps the data safe and the resource idempotent.
We can get two type of api route for get method, Generaly get-method like 

```bash
Route::get('/product', [ProductController::class, 'index']);
```
 - This api  ` http://localhost:8000/api/product `



Another for resource method as like 

```bash
Route::resource('/product', ProductController::class);
```

 - This api  ` http://localhost:8000/api/product `