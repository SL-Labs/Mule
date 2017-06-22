Mule Reference Notes
====================

**API Complete Life cycle : design, build deploy manage & govern**

* Use Mule Anypoint Platform to implement API Led connectivity and to take an API through its complete life cycle.

* Use Anypoint studio to build and debug integrations & API implementations 

* Use Dataweave to transform data (mules own powerfull transformation language)

![API Objectives] (Mule/screenshot/API Objectives.JPG?raw=true "API Objectives")

API Led Connectivity
--------------------

* API Led Connectivity is similar to Microservices architecture where you isolate or separate each layers of your application as API so that they can be re used.

* Microservices is like building services around a specific entity or object. A single service with multiple opearations as long as all these operations can be grouped together either fuctionally or logically. Example Cutomer Microservices. All operation relating to customer can be exposed as one single service which can bring data about customer along from various systems. 

* Cons : Loosely Coupled, Resuable Components as API & Services for accessing data & Resources.


SOAP Webservices 
-----------------

* Provide a mechanism for system to interact with other system using some interface or contract (WSDL) using SOAP protocol.

* SOAP protocol is a XML based protocol that defines the message architecture, message format, Service transport protocol like http, jms

* SOAP messages are typically sent over http (other protocols can be used though) and soap request is sent as the body of an HTTP POST

* SOAP request and response is always in xml format 

* SOAP request and response are sent in SOAP Envelope
