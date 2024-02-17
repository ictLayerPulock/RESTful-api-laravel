

# Table of Contents

- [Introduction](#introduction)
- [Types of APIs](#types)
- [API Architecture Types](#architecture_types)
 - [Guiding Principles](#guiding_principles)
- [Types of Method](#method_types)
- [SetUp REST API](#setup_api)
- [HATEOAS ](#hateoas)
- [HTTP Status Codes ](#status_codes)
- [Types of Versioning ](#types_versioning)
- [Clear and consistent naming convention ](#naming_convention)
- [Stateless Communications](#stateless_communications)
- [Layered systems](#layered_systems)
- [Cacheability systems](#cacheability_systems)



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


 
### POST Method: 
POST is the only RESTful API HTTP method that primarily operates on resource collections. When we menualy routing as like, 

```bash
Route::post('/product-store', [ProductController::class, 'store']);
```
 - This api  ` http://localhost:8000/api/product-store `



Another for resource method as like 

```bash
Route::resource('/product', ProductController::class);
```

 - This api  ` http://localhost:8000/api/product `


  
### PUT Method: 
Completely updates an existing resource by replacing it with new data. When we menualy routing as like, 

```bash
Route::put('/product-edit/{id}', [ProductController::class, 'edit']);
```
 - This api  ` http://localhost:8000/api/product-edit `



Another for resource method as like 

```bash
Route::resource('/product', ProductController::class);
```

 - This api  ` http://localhost:8000/api/product `


### PATCH Method: 
Partially updates a resource with specified changes. When we menualy routing as like, 

```bash
Route::patch('/product-update/{id}', [ProductController::class, 'update']);
```
 - This api  ` http://localhost:8000/api/product-update `



Another for resource method as like 

```bash
Route::resource('/product', ProductController::class);
```

 - This api  ` http://localhost:8000/api/product `


### DELETE Method: 
The last HTTP method to examine is DELETE. When a DELETE method targets a single resource, that resource is removed entirely. When we menualy routing as like, 

```bash
Route::patch('/product-delete/{id}', [ProductController::class, 'delete']);
```
 - This api  ` http://localhost:8000/api/product-delete `



Another for resource method as like 

```bash
Route::resource('/product', ProductController::class);
```

 - This api  ` http://localhost:8000/api/product `




# SetUp REST API <a name="setup_api"></a>

 - Identify Object
 The first step in designing a REST API-based application is identifying the objects that will be presented as resources.

 - Create Model URIs
Now when the object model is ready, it’s time to decide the resource URIs. 

```bash

/product
/product/{id}

```

 - Caching in REST APIs
 Being cacheable is one of the architectural constraints of REST.

  - GET requests should be cachable by default – until a special condition arises. Usually, browsers treat all GET requests as cacheable.
  - POST requests are not cacheable by default but can be made cacheable if either an Expires header or a Cache-Control header with a directive, to explicitly allows caching, is added to the response.
  - Responses to PUT and DELETE requests are not cacheable at all.

 - Cache Control Headers


 # HATEOAS - Hypermedia as an Engine of Application State <a name="hateoas"></a>

HATEOAS is a key constraint in RESTful API design and ensures that resources are interconnected through hypermedia links

```json
{
  "orderId": 12345,
  "Total Amount": 99.99,
  "_links": {
    "self": {
      "href": "https://api.example.com/orders/12345"
    },
    "buyer": {
      "href": "https://api.example.com/customers/54321"
    }
  }
}
```


 # HTTP Status Codes <a name="status_codes"></a>

These status codes are part of the HTTP protocol and are used by servers to communicate the outcome of a request to the client. They help developers and users understand what happened during the request and how to proceed accordingly.

 - 200 - OK:
 ```php
   return response()->json([
            'data'=> $data,
            'message'=>"request has succeeded",
            'code'=> 200
         ]);
```

Indicates that the request has succeeded.
It is typically used for successful GET requests or successful responses to POST, PUT, and DELETE requests.


 - 302 Found Redirect Responses:

These responses indicate that the client needs to take additional action to complete the request.
Example: 301 Moved Permanently, 302 Found


 - 404 - Not Found:

Indicates that the requested resource could not be found.
It is typically used when the server cannot find the requested resource or URL.

 - 400 - Bad Request:

Indicates that the server cannot process the request due to a client error.

 - 500 - Internal Server Error:

Indicates that the server encountered an unexpected condition that prevented it from fulfilling the request.


 # Types of Versioning <a name="types_versioning"></a>

### URI Versioning

 - Using the URI is the most straightforward approach (and most commonly used as well) though it does violate the principle that a URI should refer to a unique resource.

 ```bash 
  http://localhost:8000/api/product/v1

 http://localhost:8000/apiv1/product/v1

 ```
  - The version need not be numeric, nor specified using the “v[x]” syntax.

 - Alternatives include dates, project names, seasons, or other identifiers that are meaningful enough to the team producing the APIs and flexible enough to change as the versions change.

 ### Versioning using Custom Request Header

  - A custom header (e.g. Accept-version) allows you to preserve your URIs between versions though it is effectively a duplicate of the content negotiation behavior implemented by the existing Accept header.

 ```bash 
Accept-version: v1
Accept-version: v2

 ```


### Versioning using “Accept” header






 # Clear and consistent naming convention <a name="naming_convention"></a>

Here are some important guidelines to follow when designing the naming conventions of your REST API:

 - Use resource nouns: Focus on the resources you express and their relationships rather than specific activities. Use plural nouns (eg, /products, /users) to represent collections of resources and avoid using verbs (eg, /getProducts, /createUser).
 - Keep URLs simple and predictable: Design URLs that are intuitive and easily understood by clients, using resource hierarchies to express relationships (eg, /users/{id}/orders).
 
 - Plural Nouns for Collections: Use plural nouns to show collection of resources. Example, /users NOT  /user.
- Use lowercase letters
- Nest resource if appropriate
- Use hyphens to separate words
- Avoid unnecessary abbreviations


 # Stateless Communications <a name="stateless_communications"></a>

Server endpoints created from customer designs promote stateless communication by ensuring that they are independent of any client context. This makes it easy to scale web services and handle growing requests.


 # Layered systems <a name="layered_systems"></a>

A layered system architecture separates concerns into different layers, such as the user interface, business logic, and data access layers in a typical N-tier web application.



 # Cacheability systems <a name="cacheability_systems"></a>

Caching is the ability to store copies of frequently accessed data in several places along the request-response path.

```php

use App\Models\Product;
use Illuminate\Support\Facades\Cache;

....

    public function index(){
       return Cache::remember('cases', 60, function(){
        return Product::all();
       });
    }
```