# Understanding System Design
System design is a step-by-step process of defining a particular software's architecture, modules, components, etc. It is a base concept in software engineering and is vital in building scalable and reliable software.
##   Need for the System Design
System design is needed to prepare the architecture for the application according to the user requirements. 
# Exploring Essential Design Methods in System Design
Here are some of the system design methods commonly used by developers.
1. **Architectural Design**  
The architectural design is the base of the system design. It describes the infrastructure, model, view, components, and interaction.
1. **ERD Diagram**   
The ERD diagram is an acronym for the entity-relationship diagram. The ERD diagram is mainly used in designing the application's database structure.
1. **UML Diagram**  
The UML stands for the unified modeling language. It is used to prepare modeling software systems.
1. **Class Diagrams**  
The class diagrams are used to represent the classes. The class diagram can also contain the class's attributes, methods, and relationships between multiple classes.
1. **Sequence Diagrams**  
The sequence diagrams represent the interaction between the various components of the system. It is used to model the behavior of the system.
#  System Design Concepts
### 1. Performance vs Scalability  
**Performance:** When you visit any particular website, some website takes more time to load, and others get loaded in a fraction of a second. To solve slow loading various mechanisms like caching can be used to increase the application's performance and serve resources faster.  
**Scalability:**  You can scale your application by distributing the load across multiple servers or increasing the single server's capacity.  
### 2. Latency vs Throughput  
**Latency:** The latency is a measurement of the time delay to complete a single request or data operation.  
**Throughput:** On the other hand, throughput is the number of operations the system can handle in a particular time or the number of data passed via network request in a given time.
### 3. Consistency Patterns and Availability Patterns  
**Consistency:** Consistency ensures that all nodes in the system read the same data at a particular time.  
**Availability:** The system's availability ensures that each request receives a response either with fresh or old data.   
### Consistency Patterns  
* **Strong consistency:** Strong consistency ensures that each request should get the most recent data.   
* **Eventual Consistency:** Eventual consistency allows temporary inconsistencies to be resolved soon.  
* **Weak Consistency:** In the weak consistency pattern, the user may get fresh data after writing the data.
### Availability Patterns
* **Load Balancing:** The upcoming request can be distributed across multiple servers to achieve high availability.   
* **Retry and timeout strategies:** You can implement the retry mechanism to process the request after every interval if the system fails or is not available.
# Advanced Concepts in System Design  
## 1. CDN   
CDN stands for the content delivery network. The CDN is a distributed server network located at different geo-locations. The CDN is used to deliver content like images, various data, etc., from the server.

The CDN delivers the resource faster, decreases latency (network delay), and improves the application's performance.  
## 2. DNS
The DNS stands for the domain name system.  
The DNS system allows users to access the website and its resources using the domain name.  
## 3. Caching
Caching is a mechanism to serve resources faster. It is also called high-speed storage. It works between the web application and the source of the data.  
## 4. Proxies
The proxy server works between the client of the application and the internet.   
The proxy servers are used for the caching.  
# Components of System Design
## 1. Microservices and Service Discovery  
 The microservices break down complex applications into small services, such that each service works independently and accomplishes specific tasks.   
### The concepts below are related to the microservices.

* **Service Identification:** Every microservice has a unique ID and name for its identification.
* **Dynamic Service Discovery:** Each microservice can dynamically find other services located in the same network. So, scaling and load balancing become easy.
## 2. Database Systems: RDBMS and NoSQL
### RDBMS
The RDBMS stands for the relational database management system. The SQL databases are built on the top of the RDBMS.  
 It makes it easier to access the data from the database and connect it with other data as they are stored in the table format.  
#### Here are the characteristics of the RDBMS database.

* It stores the data in the table format.
* You can’t scale the RDBMS database horizontally, but you can scale it vertically.
* SQL is a query language for the RDBMS databases.
* Accessing data from the RDBMS database is slow.
###  NoSQL
The NoSQL database means a non-SQL database. It stores the data in the key-value pair instead of in table format.It stores unstructured data in the database.

#### Here are the characteristics of the NoSQL database.

* It stores the data in the key-value pair format.
* NoSQL database is horizontally scalable, as you can add new key-value pairs for new attributes.
* Each record can contain different key-value pairs.
* It is faster than RDBMS databases.
* It supports frequent change.  
## 3. Communication Protocols
Protocols mean rules and communication protocols refer to the rules to communicate or exchange the data between two systems.  
#### various communication protocols  
* HTTP/HTTPS: The full form of the HTTP is a hypertext transfer protocol. HTTPS is a secure version of HTTP. They are used in web-based communication. It is a good idea to use HTTPS always for security reasons.
* TCP/IP: The TCP stands for the transmission control protocol. The TCP protocol is used to communicate over the internet.
* UDP – The UDP is an acronym for the user datagram protocol. It is mainly used for live streaming, video calls, etc., in which data loss can be tolerable.
* WebSockets: The web sockets are used for bi-directional duplex communication. It builds the connection between two web applications.
# Approaching System Design Interview Questions
## Step-by-step Guide
### 1. Requirements clarification
Before you prepare a system design for any software, it is important to know the requirements.  
#### There can be two types of requirements:
**Function requirements:** The functional requirements are the requirements in the application with which the user interacts.
**Non-function requirements:** The non-functional requirements are the requirements to improve the application's capabilities.   
### 2. Estimation of resources
The next step is deciding what kind of resources you should use to build the application. You are also required to decide how much data you require to store in the database.
### 3. System interface definition
The third step is designing the system interface. For example, defining the API endpoints and what to expect from each API endpoint.  
### 4. Defining Data model
The next important part is selecting a database for the application.

If you need to store the structured data and tables are pre-determined, you can use the relational database. For storing the unstructured data, you should use NoSQL databases like MongoDB.
### 5. High-level design
The next step is designing the high-level components. You can’t design the system for the whole application in a single go. So, you need to go step-by-step.

In this step, you need to decide how you will connect the components of the system with each other.  
### 6. Detailed design
After creating the basic design of the application, you need to improve the system design. You need to analyze the system to fulfill the non-functional requirements.

#### You can analyze it as given below.

*  How to use caching to improve the performance of the application?
* How do we scale the application via load balancing?
* Should you use the CDN for caching, or are cookies enough?
* How would you handle the failure of the application?
* Should you distribute the data across multiple databases?
* How will you replicate the database?
###  7. Identifying and resolving bottlenecks
At last, you should identify the bottlenecks in your system design and discuss the solutions to resolve them with the interviewer.

#### The sample bottlenecks can be shown below.

* Can the system fail in any scenario? If yes, how will you handle it?
* How do you monitor the performance of the system and issues in the system?
* Do you have enough replicas of the database to handle the failure?
# Sample System Design Interview Questions and Solutions

### 1. How would you design a URL Shortening service similar to TinyURL?
The URL shortening service allows users to shorten the long URLs. So users can use the short URL instead of the long URL.

#### Requirements clarification:

* When you give a long URL as an input, it should return the shortened URL.
* When you click the shortened URL, it should redirect to the original URL.
* Consider 500 requests per second, and make scalable accordingly.
* Delete the expired URLs.
* Track the number of clicks on the URL.
### Approach:

#### You can discuss the below stuff.

* How you will use the REST API to communicate with the server.
* How will you handle the 500 requests every second via load balancing?
* You can discuss using the relational database, as it doesn’t require horizontal scaling.
* You can discuss how you will prepare a table for relational database to map long URLs with short URLs.
* The critical point is how to shorten the long URL by providing a unique id to each shortened URL.
###  2. How would you design a Web Crawler?
The Web crawlers allow to extract the information from different web pages.

### Approach:

* You can discuss how you open multiple web pages in the web browser. Also, it is important to know how many browser windows you will open simultaneously to crawl multiple web pages.
* You can also discuss changing the web pages and domains dynamically.

###  3. How would you design Facebook and Instagram?
Here, you are required to build a social media application.

###  Requirements:

* User signup/sign-in
* Allowing users to publish posts and short videos
* Followers and following features
* Direct messaging
* Showing the latest posts from their followers
* Showing trending posts in the feed
### Approach:

* Talk about how you will handle the relationship between users in the database.
* Talk about how you will implement the chat features.You may talk about integrating third-party chatting applications.
*  Furthermore, you can discuss how you will implement the authentication.
* Discuss algorithms to show trending or latest posts.
* Talk about handling user’s data in the database, as users will publish multiple posts.
* Discuss database replication to handle failures.
*  Discuss data caching and load balancing.
### 4. How would you design the API rate limit?
The API rate limiter allows one to make a particular number of API requests in a specified time. If the API request increases, it blocks the request for some time.

### Approach:

* Talk about rate-limit matrics. How many maximum requests do you want to allow per second?
* Talk about how you will handle multiple requests simultaneously.
*  Talk about how you can keep count of requests. You may use the IP address received in the request header.
