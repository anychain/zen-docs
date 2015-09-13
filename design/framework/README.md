<!--
        Licensed Materials - Property of esse.io

        (C) Copyright esse.io Inc. 2015 All Rights Reserved

        Licensed under the Apache License, Version 2.0 (the "License");
        you may not use this file except in compliance with the License.
        You may obtain a copy of the License at

           http://www.apache.org/licenses/LICENSE-2.0

        Unless required by applicable law or agreed to in writing, software
        distributed under the License is distributed on an "AS IS" BASIS,
        WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
        See the License for the specific language governing permissions and
        limitations under the License.
-->

# Zen Services/Components

===

**Note:** The content of **Arhant release** mark with **(A)**.

===

## Identiry Service **(A)**
### User Authentication **(A)**
### Service Registry **(A)**
A Registry service to register and lookup the Zen Services endpoint internally.
*Reference:* [Keystone](https://wiki.openstack.org/wiki/Keystone)

## Messaging Service **(A)**

* [ZeroMQ](http://zeromq.org) 

## Data Connector **(A)**
**Note:** For Arhant, just keep it as simple, let user input a URL to download the file.

### SDK
### Controller
### Event Handler
### Data Transport
The data transport need to handle the data transfer over *internet*, so **transfer resuming** and **data encryption** are required.
..* Messaging Queue
..* Data Encryption

### Data Sources **(A)**
#### Flat File **(A)**
#### MySQL

## Data Server **(A)**
### Controller
### Event Handler
### Data Transport
#### Adapters
..* HDFS Adapter **(A)**
..* Kafka Adapter
### API Service

## Multi-tenancy **(A)**
### Controller **(A)**
### API Service **(A)**
### Resource Management **(A)**
#### Data **(A)**
* [Multitenancy for Hadoop: Namespaces](http://blog.cask.co/2015/04/multitenancy-for-hadoop-namespaces/)
* [Multi-Tenancy in HDP 2.0: Capacity Scheduler and YARN](http://hortonworks.com/blog/multi-tenancy-in-hdp-2-0-capacity-scheduler-and-yarn/)

#### Workload(CPU/Memory/IO)
#### Cluster 

## Data Flow Engine **(A)**
### Engine and SDK **(A)**
* [Google Cloud Data Flow](https://cloud.google.com/dataflow/)
* [Spark Data Flow](https://github.com/cloudera/spark-dataflow)
### Modeling **(A)**
### JSON Store

## Job Management/Scheduler **(A)**
### Job Server **(A)**
### Scheduler **(A)**

## API Service/Client **(A)**
### API Server **(A)**
### Python Client ✦ User Dashboard **(A)**