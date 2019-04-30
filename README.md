# SmartProxy
a new approach to improve overall performance and usability of databases. Results of the analysis will be based on repeatable and verifiable observation of REST-based interactions with three products: MongoDB, MySQL DB and Microsoft SQL Server.

1.3 Proposed System and Advantages
This project is an approach to create a generic solution to improve performance and usability of database systems by creating the Smart proxy based on REST API

Advantages
•	Generic solution across various models of the database
•	Improves the performance of the database system
•	Improves the usability of the database system
•	Ensures the data is available to the data owners at any instance of the time.
•	Added security model across the database systems


![](https://github.com/NagachandraKambathalliParswanatha/SmartProxy/blob/master/Picture1.png)



Objectives and Methodology
Objectives
•	To design and implement the SmartProxy architecture
•	To improve the database performance regardless of its type
•	To improve the database usability and availability regardless of its type
•	To ensure that the data upload and retrieval to the cloud is available to the data owners at any instance of the time.
•	To implement a light weight computationally efficient security algorithm for securing the data stored across the database systems.

Methodology
Figure below presents a high level design of a proxy which is a middleware based on REST principles. The solution presented in this paper has a HTTP/JSON-based API and it can act as a transparent and the Smart proxy. The transparent mode works as an intermediary system that sits between an application and a database. When an application sends a request to a database, proxy intercepts it and asynchronously performs various actions including redirection and collecting data
 
The Smart proxy mode is being used when a user wants to improve overall experience while interacting with a database. In this mode when an application makes a request to the database, proxy extends its functionality and acts as an another level of abstraction. 
Our prototype implementation also provides new features, like benchmarking, tuning, caching and a way to set constraints on a model. The proxy can validate data, change response details and dynamically create a model based on the requests.
The main aim of the Smart proxy architecture design is to be a generic solution. Authors have decoupled core logic from the services. It is easy to create plugins and extend capabilities of the proxy. Currently, we can use database optimization, scaling, hinting, data modeling, validation and logging plugins.


To improve database performance, we can use query planners. Analyzing execution plans lead authors to a conclusion that additional statistics must be retrieved from a request and a response. To store meaningful data, authors have built a generic query parser. Query parser takes a request and asynchronously starts parsing it. In the same time, it sends intercepted query to the database to reduce delays. Parser starts from checking which query language has been used. Then it creates an abstract syntax tree and performs semantic check. This plugin can store queries, execution times, responses and database configuration.

