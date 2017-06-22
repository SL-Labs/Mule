# Implementing API-Led Connectivity with Anypoint Platform #

#### Introduction ####
---

* Use Mule Anypoint Platform to implement API Led connectivity and to take an API through its complete life cycle.

     ***API Complete Life cycle : design, build deploy manage & govern***

* Use Anypoint studio to build and debug integrations & API implementations 

* Use Dataweave to transform data (mules own powerfull transformation language)

![api objectives](https://user-images.githubusercontent.com/4846462/27419724-560c5c5a-571a-11e7-9581-343f58d96a3f.JPG)


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

#### Introducing APIs and web services ####
---

![what is api?](https://user-images.githubusercontent.com/4846462/27421270-97baa3b2-5721-11e7-9fbe-2aa82aff6357.JPG)

* API is similar to interface concept in java where you define the contract (available operations/methods, method signature like input, output, data type) and publish it to the outside world. so that at later point in time some other system can integrate and communicate with our application via API

* Pros of API is that its give you an abstraction layer and hides the internal logic. This allows us to change the underlying code in the future behind the scenes without changing how people call it.

* An API gateway can act as an proxy for the actual weservice and it controlls whats goes in & comes out. This helps us to provide or implemenmt some security features like restricted access and usage. 

#### Understanding web services ####
---

* A webservice is an actual implementation of an API.

![what is webservices ?](https://user-images.githubusercontent.com/4846462/27422212-3e4c16fe-5725-11e7-9a42-6a840e648175.JPG)

![rules of webservice communication](https://user-images.githubusercontent.com/4846462/27422308-8d85049c-5725-11e7-9ef9-961b902572d4.JPG)

![types of webservices](https://user-images.githubusercontent.com/4846462/27422400-ede596ee-5725-11e7-8753-28eb997d3452.JPG)


#### SOAP Webservices ####
---

* Provide a mechanism for system to interact with other system using interface or contract document (i.e, WSDL) using SOAP protocol.

* SOAP protocol is a XML based protocol that defines the message architecture, message format, Service transport protocol (like http, jms)

* SOAP messages are typically sent over http (other protocols can be used though) and soap request is sent as the body of an HTTP POST

* SOAP request and response is always in xml format 

* SOAP request and response are sent in SOAP Envelope
