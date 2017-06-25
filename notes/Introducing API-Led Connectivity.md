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


![introduction to api-led connectivity](https://user-images.githubusercontent.com/4846462/27516148-ac55bc80-59ab-11e7-99af-859543ae3bb0.gif)



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


     ***API Complete Life cycle : design, build, deploy, manage & govern***

![API development lifecycle](https://user-images.githubusercontent.com/4846462/27511202-0410e49e-5917-11e7-91d2-ee89915b4eed.JPG)


---
#### What is Anypoint platform ####
---

* It is a collection of runtime, framework tools, integration platform & web application.


![Anypoint Platform](https://user-images.githubusercontent.com/4846462/27511410-4a92d6da-591b-11e7-8b98-2a77b2f8178b.JPG)


![API  Development Cycle](https://user-images.githubusercontent.com/4846462/27512218-7720a36a-5931-11e7-830d-b17907065a5b.gif)


***API Development cycle : API Definition***

* **API Designer** : Its an web based IDE to build RAML (RESTful Application Modelling Language) files a.k.a API Spec

* **Mocking Services & API Console** : This component is used to stimulate our API design by using the RAML file

* **API Portal & Exchange** : Other developer discovers the API, learns about it and gives reviews / feedbac 
