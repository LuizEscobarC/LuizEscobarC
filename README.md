<h3 align="center">A passionate Developer from Brazil</h3>


- 🔭 I’m currently working on **Super Heavy App** and **Face Before After App**

- 🌱 I’m currently learning **Devops and software architecture**

```

            +------------------------------------------------+
            |             Monolithic architecture            |
            |  +-----------+  +------------+  +-----------+  |
            |  |  Auth     |  |  Orders    |  |  Payments |  |
            |  +-----------+  +------------+  +-----------+  |
            |                                                |
            |  +-----------+  +------------+  +-----------+  |
            |  |  Web UI   |  |  Business   |  |   DB     |  |
            |  |           |  |  Logic      |  | Access  |  |
            |  +-----------+  +------------+  +-----------+  |
            +------------------------------------------------+


                              
                            
                        Microservices Architecture
                         +---------------------+
                         |     Frontend App    |
                         |  (React, Angular…)  |
                         +----------+----------+
                                    |
                                    v
                         +---------------------+
                         |     API Gateway     |
                         | (Routing/Auth Rate) |
                         +----------+----------+
                                    |
        +---------------------------+---------------------------+
        |                           |                           |
        v                           v                           v
+---------------+         +----------------+         +----------------+
|  Auth Service |         | Order Service  |         | Payment Service|
|   (Node.js)   |         |  (Java)        |         |   (Go)         |
+------+--------+         +--------+-------+         +--------+-------+
       |                          |                          |
       v                          v                          v
+---------------+         +----------------+         +----------------+
|  Auth DB      |         | Order Database |         | Payment DB     |
| (PostgreSQL)  |         |  (MongoDB)     |         |   (MySQL)      |
+---------------+         +----------------+         +----------------+

        +-----------------------------------------------------+
        |     Shared Infrastructure (Async Communication)     |
        |  +----------------+   +--------------------------+  |
        |  |   Message Bus  |   |   Service Discovery       | |
        |  |   (Kafka, SQS) |   |   (Consul, Eureka, etc.)  | |
        |  +----------------+   +--------------------------+  |
        +-----------------------------------------------------+


                            Hexagonal architecture
                         +-----------------------------+
                         |     External Interfaces     |
                         |  (Web, CLI, REST, Events)   |
                         +-------------+---------------+
                                       |
                                       v
                          +--------------------------+
                          |      Application Core     |
                          |   (Use Cases / Services)  |
                          +-------------+------------+
                                        |
         +------------------------------+------------------------------+
         |                             |                               |
         v                             v                               v
+----------------+        +-----------------------+       +-----------------------+
|  Input Adapter |        |   Output Adapter      |       |   Output Adapter      |
| (REST Controller)|      | (Repository, DB Port) |       | (Event Publisher)     |
+----------------+        +-----------------------+       +-----------------------+
                                |                               |
                                v                               v
                        +---------------+               +---------------+
                        |   Database    |               |  Message Bus  |
                        | (PostgreSQL)  |               |   (Kafka)     |
                        +---------------+               +---------------+

```
