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

## 1. Identiry Service **(A)**
### 1.1. User Authentication **(A)**
### 1.2. Service Registry **(A)**
A Registry service to register and lookup the Zen Services endpoint internally.
*Reference:* [Keystone](https://wiki.openstack.org/wiki/Keystone)

## 2. Messaging Service **(A)**

* [ZeroMQ](http://zeromq.org) 

## 3. Data Connector **(A)**
**Note:** For Arhant, just keep it as simple, let user input a URL to download the file.

### 3.1. SDK
### 3.2. Controller
### 3.3. Event Handler
### 3.4. Data Transport
The data transport need to handle the data transfer over *internet*, so **transfer resuming** and **data encryption** are required.
... Messaging Queue
... Data Encryption

### 3.5. Data Sources **(A)**
#### 3.5.1. Flat File **(A)**
#### 3.5.2. MySQL

## 4. Data Server **(A)**
### 4.1. Controller
### 4.2. Event Handler
### 4.3. Data Transport
#### 4.3.1. Adapters

* HDFS Adapter **(A)**
* Kafka Adapter

### 4.4. API Service

## 5. Multi-tenancy **(A)**
### 5.1. Controller **(A)**
### 5.2. API Service **(A)**
### 5.3. Resource Management **(A)**
#### 5.3.1. Data **(A)**
* [Multitenancy for Hadoop: Namespaces](http://blog.cask.co/2015/04/multitenancy-for-hadoop-namespaces/)
* [Multi-Tenancy in HDP 2.0: Capacity Scheduler and YARN](http://hortonworks.com/blog/multi-tenancy-in-hdp-2-0-capacity-scheduler-and-yarn/)

#### 5.3.2. Workload(CPU/Memory/IO)
#### 5.3.3. Cluster 

## 6. Data Flow Engine **(A)**
### 6.1. Engine and SDK **(A)**
* [Google Cloud Data Flow](https://cloud.google.com/dataflow/)
* [Spark Data Flow](https://github.com/cloudera/spark-dataflow)

### 6.2 Modeling **(A)**
### 6.3 JSON Store

## 7. Job Management/Scheduler **(A)**
### 7.1 Job Server **(A)**
### 7.2 Scheduler **(A)**

## 8. API Service/Client **(A)**
### 8.1. API Server **(A)**
### 8.2. Python Client ✦ User Dashboard **(A)**