# Implementing API-Led Connectivity with Anypoint Platform #


---
#### Introduction ####
---

* Use Mule Anypoint Platform to implement API Led connectivity and to take an API through its complete life cycle.

     ***API Complete Life cycle : design, build, deploy, manage & govern***

* Use Anypoint studio to build and debug integrations & API implementations 

* Use Dataweave to transform data (mules own powerfull transformation language)

![api objectives](https://user-images.githubusercontent.com/4846462/27419724-560c5c5a-571a-11e7-9581-343f58d96a3f.JPG)


---
#### Introduction to API-led Connectivity ####
---

![traditional integration project](https://user-images.githubusercontent.com/4846462/27420610-90881d16-571e-11e7-8741-7ef620aee595.JPG)


![traditional integration project pros cons](https://user-images.githubusercontent.com/4846462/27420671-e63f9c7a-571e-11e7-9d7c-73e8285b24d8.JPG)


![traditional integration project problem](https://user-images.githubusercontent.com/4846462/27420731-2bf02398-571f-11e7-84d7-26bb66b3276e.JPG)


![api led connectivity approach](https://user-images.githubusercontent.com/4846462/27420780-640a0406-571f-11e7-8adb-4c84c75f4957.JPG)


![api led connectivity led approach pros](https://user-images.githubusercontent.com/4846462/27420833-95d21398-571f-11e7-8007-9a71d728ccd9.JPG)


![api led connectivity future proof](https://user-images.githubusercontent.com/4846462/27420969-350c0a68-5720-11e7-87a4-7164a7e73a49.JPG)


![api led connectivity future proof](https://user-images.githubusercontent.com/4846462/27421026-6c6a401a-5720-11e7-9d1d-ba0310e5daea.JPG)


![api led connectivity future proof](https://user-images.githubusercontent.com/4846462/27421125-ea2f58c8-5720-11e7-8085-03ed04296000.JPG)


![api led connectivity future proof Building block of MSA](https://user-images.githubusercontent.com/4846462/27421153-1694bda4-5721-11e7-844c-66efebc1370d.JPG)


* API Led Connectivity is similar to Microservices architecture where you isolate or separate each layers of your application as API so that they can be re used.

* Microservices is like building services around a specific entity or object. A single service with multiple opearations as long as all these operations can be grouped together either fuctionally or logically. Example Cutomer Microservices. All operation relating to customer can be exposed as one single service which can bring data about customer along from various systems. 

* Cons : Loosely Coupled, Resuable Components as API & Services for accessing data & Resources.



---
#### Introducing to APIs and web services ####
---

![what is api?](https://user-images.githubusercontent.com/4846462/27421270-97baa3b2-5721-11e7-9fbe-2aa82aff6357.JPG)

* API is similar to interface concept in java where you define the contract (available operations/methods, method signature like input, output, data type) and publish it to the outside world. so that at later point in time some other system can integrate and communicate with our application via API

* Pros of API is that its give you an abstraction layer and hides the internal logic. This allows us to change the underlying code in the future behind the scenes without changing how people call it.

* An API gateway can act as an proxy for the actual weservice and it controlls whats goes in & comes out. This helps us to provide or implement some security features like restricted access and usage. 


---
#### Understanding web services ####
---

* A webservice is an actual implementation of an API.

![what is webservices ?](https://user-images.githubusercontent.com/4846462/27422212-3e4c16fe-5725-11e7-9a42-6a840e648175.JPG)

![rules of webservice communication](https://user-images.githubusercontent.com/4846462/27422308-8d85049c-5725-11e7-9ef9-961b902572d4.JPG)

![types of webservices](https://user-images.githubusercontent.com/4846462/27422400-ede596ee-5725-11e7-8753-28eb997d3452.JPG)


---
#### Introducing SOAP web services ####
---

* Provide a mechanism for system to interact with other system using interface or contract document (i.e, WSDL) using SOAP protocol.

* SOAP protocol is a XML based protocol that defines the message architecture, message format, Service transport protocol (like http, jms)

* SOAP request and response are sent in SOAP Envelope

* SOAP messages are typically sent over http (other protocols can be also used though like jms, udp) 

* SOAP request is sent as the body of an HTTP POST

* SOAP Webservice will support only xml format, hence the SOAP webservice request and response is always in xml format 


![soap webservices](https://user-images.githubusercontent.com/4846462/27507572-dd84637a-58c9-11e7-9b57-b0605828aad0.JPG)


![soap messages](https://user-images.githubusercontent.com/4846462/27507778-55ba6854-58ce-11e7-86fb-ef63967554fb.JPG)


---
#### Introducing RESTful web services ####
---

* REST is a modern or 2nd generation Webservice.

* REST is light weight and doesnot require any formal contract like wsdl in SOAP Webservice.

* REST supports only HTTP(S) and it will support all MIME (Multipurpose Internet Mail Extension) data format.

* REST (Representation State Transfer) is an architectural style where client & server exchnage representation of data & resources using HTTP(S) protocol.

* REST exposes data & resources to the external world using the uri and those uri are bounded to the standard HTTP methods. So each uri represents (created, accessed, modified) a state of that resource 



![RESTful webservice request](https://user-images.githubusercontent.com/4846462/27510801-aabd676a-5910-11e7-9b39-e1f835105229.JPG)

 ***Difference between PUT & PATCH***

| PUT | PATCH |
| --- | --- |
| PUT replaces an existing resource completely. If the resource doesnot exsist then a new resource is created. | PATCH partially updates a resource based on the submitted data. |
| PUT is like replace or create | PATCH is like update (updating just the delta information that has been submitted) |
| PUT is used to replace an exsisting resource and if not found then will create the resource | PATCH is used to update an already exsisting resource |

* If PATCH request submitted with 2 fields for a resource with 8 fields, then only those 2 fields are updated and for PUT request the 2 fields are updated and others are set to their default/existing values. 


![Example REStful Webservice calls](https://user-images.githubusercontent.com/4846462/27510916-6265918e-5912-11e7-8df3-1f03b2e29b21.JPG)


![making calls to RESTful API](https://user-images.githubusercontent.com/4846462/27511078-3db03c10-5915-11e7-8542-737cb686e8c1.JPG)


![getting response from REST Webservice](https://user-images.githubusercontent.com/4846462/27511090-79f80de2-5915-11e7-87a7-f1fdb8eeb337.JPG)


![common HTTP response codes](https://user-images.githubusercontent.com/4846462/27511099-a00959dc-5915-11e7-8d59-5f851638733c.JPG)


* A great resource to pick the correct HTTP error code for your API: http://racksburg.com/choosing-an-http-status-code/

