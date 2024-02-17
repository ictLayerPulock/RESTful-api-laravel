

# Table of Contents

- [Introduction](#introduction)
- [Types of APIs](#types)
- [API Architecture Types](#architecture_types)
 - [Guiding Principles](#guiding_principles)



<br/>
<br/>
<br/>


# Introduction <a name="guiding_principles"></a>

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


### 1.1. Uniform Interface
By applying the principle of generality to the components interface, we can simplify the overall system architecture and improve the visibility of interactions. Multiple architectural constraints help in obtaining a uniform interface and guiding the behavior of components.

The following four constraints can achieve a uniform REST interface:

 - Identification of resources – The interface must uniquely identify each resource involved in the interaction between the client and the server.
 - Manipulation of resources through representations – The resources should have uniform representations in the server response. API consumers should use these representations to modify the resource state in the server.
 - Self-descriptive messages – Each resource representation should carry enough information to describe how to process the message. It should also provide information of the additional actions that the client can perform on the resource.
 - Hypermedia as the engine of application state – The client should have only the initial URI of the application. The client application should dynamically drive all other resources and interactions with the use of hyperlinks.

In simpler words, REST defines a consistent and uniform interface for interactions between clients and servers. For example, the HTTP-based REST APIs make use of the standard HTTP methods (GET, POST, PUT, DELETE, etc.) and the URIs (Uniform Resource Identifiers) to identify resources.

### 1.2. Client-Server
The client-server design pattern enforces the separation of concerns, which helps the client and the server components evolve independently.

By separating the user interface concerns (client) from the data storage concerns (server), we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.

While the client and the server evolve, we have to make sure that the interface/contract between the client and the server does not break.

### 1.3. Stateless
Statelessness mandates that each request from the client to the server must contain all of the information necessary to understand and complete the request.

The server cannot take advantage of any previously stored context information on the server.

For this reason, the client application must entirely keep the session state.

### 1.4. Cacheable
The cacheable constraint requires that a response should implicitly or explicitly label itself as cacheable or non-cacheable.

If the response is cacheable, the client application gets the right to reuse the response data later for equivalent requests and a specified period.

### 1.5. Layered System
The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior. In a layered system, each component cannot see beyond the immediate layer they are interacting with.

A layman’s example of a layered system is the MVC pattern. The MVC pattern allows for a clear separation of concerns, making it easier to develop, maintain, and scale the application.

### 1.6. Code on Demand (Optional)
REST also allows client functionality to extend by downloading and executing code in the form of applets or scripts.

The downloaded code simplifies clients by reducing the number of features required to be pre-implemented. Servers can provide part of features delivered to the client in the form of code, and the client only needs to execute the code.

<br/>
<br/>
