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

# Job Server

## 1. Overview

  ![Overview](/design/_static/fw-job-server.png)

## 2. Modules

### 2.1. Job Management

* Create Job
* Describe Jobs
* Delete Job
* Execute Job

### 2.2. Job Submitter
Submit the user job via the *Adapter Interface* to Spark, Hadoop, YARN ... when executing the job.

### 2.3. Job Tracker
**Note:** could be deferred to next release.
Tracking and monitoring the job status during the job executing, and push the messages to **Dispatcher Service**.

### 2.4. Adapter Interface / Adapters
* Common Interface for job submitting and tracking, to adapter the job server with Spark/Hadoop/YARN ... services.
* Adapters
..* Standalone Spark adapter
..* Spark on YARN adapter
..* Hadoop adapter (deferred)
..* Hadoop on YARN adapter (deferred)

### 2.5. Job Scheduler
Schedule the user job executing time.

### 2.6. Service Clients
* Keystone Client
* Multi-tenancy Service Client
* Dispatcher Service Client
* Encrypting Service Client
