# scheduler
This service provides the functionalities of scheduling the curriculum, syllabus, schedule, or target plan. It is written in [Nest JS](https://github.com/nestjs/nest)

## Features
* CRUD APIs to create schedule and schedule details
* CRUD APIs to subscribe to schedule and track schedule completion

## Installation steps
[In progress]
  
## Database design

### Schedule
| id        | title        | config         |   status     | start-date         | end-date       |
|-----------|--------------|----------------|--------------|--------------------|----------------|
|primary key|Scedule name  |Metadata        |scedulestatus |expected-start-date |scedule-end-date|

#### Example values
title - English semester exam syllabus
config - `{
        "board": [
            "CBSE"
        ],
        "medium": [
            "English"
        ],
        "subject": [
            "English"
        ],
        "framework": [
            "pratham"
        ],
        "gradeLevel": [
            "Class 10"
        ],
        "frameworkObj": {
            "code": "pratham",
            "name": "SSC",
            "type": "",
            "identifier": "pratham"
        }
    }`
status - active
start-date - 2024-02-06T11:56:27.259Z
end-date - 2024-08-06T11:56:27.259Z


### Content (This table will be used to add schedule details)

| id        |schedule-id| content            | content-detail       | parent_id                  |order   | duration   | config  | context | context-id   | prerequisite   | post-action | status   |
|-----------|-----------|--------------------|----------------------|----------------------------|------  |---------   |---------|--------- |------------ |----------------|-------------|----------|
|primary key|foreign key|Topic or agenda item| cotent details, urls | To decide topic or subtopic|ordering| Ideal time |metadate |related to|related to id| prerequisite   |post-action   |published |


### subscription

| id         | schedule-id  | start-date     | end-date  | assignee    | assigned_by        | self-assign  | status |
|------------|--------------|----------------|-----------|----------   |--------------      |------------- |--------|
| primary key|foreign key   |                |           |SubscriberId |if assigned by other|If yes 1 or 0 |active  |

### tracking

| id        | schedule-id  | content-id | created-date  | start-date |completed-date       | created_by | delay  | status |
|-----------|--------------|------------|---------------|------------|---------------------|------------|--------|--------|
|primary key|foreign key   |foreign key |               |            |topic completion date|            |        |        |

## Postman Collection
Find [here](https://vowelapis.postman.co/workspace/My-Workspace~039146b2-42d9-4179-8f8c-ea9a86983438/collection/548641-348fc27a-b57c-4f60-a04a-9e371b998a5d?action=share&creator=548641)


