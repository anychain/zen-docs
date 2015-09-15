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
  * List Jobs
  * Show Job execution history
* Delete Jobs
* Execute Jobs

### 2.2. Job Submitter
Submit the user job via the *Adapter Interface* to Spark, Hadoop, YARN ... when executing the job.

### 2.3. Job Tracker
**Note:** could be deferred to next release.
Tracking and monitoring the job status during the job executing, and push the messages to **Dispatcher Service**.

### 2.4. Adapter Interface / Adapters
* Common Interface for job submitting and tracking, to adapter the job server with Spark/Hadoop/YARN ... services.
* Adapters
  * Standalone Spark adapter
  * Spark on YARN adapter
  * Hadoop adapter (deferred)
  * Hadoop on YARN adapter (deferred)

### 2.5. Job Scheduler
Schedule the user job executing time.

### 2.6. Service Clients
* Keystone Client
* Multi-tenancy Service Client
* Dispatcher Service Client
* Encrypting Service Client

## 3. API
### 3.1. API Version
**GET**     /
* **Response Code:** 200 
* **Response Body:**
```
{
    "versions": [
        {
            "id": "v0.1",
            "links": [
                {
                    "href": "http://localhost:8081/v2/",
                    "rel": "self"
                }
            ],
            "status": "SUPPORTED",
            "version": "",
            "min_version": "",
            "updated": "2015-09-15T11:33:21Z"
        }
    ]
}
```

### 3.2. Job Create
**POST**    /v0.1/{tenant_id}/job
* **Request Body**
```
{
    "job": {
        "name": "job name",
        "desc": "job description",
        "dataflow": "dataflow descriptor id",
        "adapter": "job adapter",
        "schedule": ""
    }
}
```

* **Response Code:** 200, 400, 500
* **Response Body:**
```
{
    "job": {
        "id": "job_id",
    }
}
```

### 3.3. Job Describe
#### 3.3.1. List Job(s)
**GET**     /v0.1/{tenant_id}/jobs
**GET**     /v0.1/{tent_id}/jobs/{job_id}
* **Response Code:** 200, 400, 500
* **Response Body:**
```
{
    "jobs": [
        {
            "id": "job id",
            "status": "job status",
            "name": "job name",
            "desc": "job description",
            "dataflow": "dataflow descriptor id",
            "adapter": "job adapter",
            "schedule": "",
            "fee": ""
        },
        {
            "id": "job id",
            "status": "job status",
            "name": "job name",
            "desc": "job description",
            "dataflow": "dataflow descriptor id",
            "adapter": "job adapter",
            "schedule": "",
            "fee": ""
        }
    ]
}
```

#### 3.3.2. Show Job Executing History
**GET**     /v0.1/{tenant_id}/job/{job_id}/history
* **Response Code:** 200, 400, 500
* **Response Body:**
```
{
    "histroy": [
        {
            "id": "job executing id",
            "status": "job status",
            "start": "start time",
            "end": "end time",
            "fee": "fee"
        },
        {
            "id": "job executing id",
            "status": "job status",
            "start": "start time",
            "end": "end time",
            "fee": "fee"
        }
    ]
}
```

### 3.4. Job Delete

### 3.5. Job Execute
