# scheduler
This service provides the functionalities of scheduling the curriculum or syllabus or schedule or target plan. It is written in [Nest JS](https://github.com/nestjs/nest)


Database design

Schedule
| id        | title        | config         |   status     | start-date         | end-date       |
|-----------|--------------|----------------|--------------|--------------------|----------------|
|primary key|Scedule name  |Metadata        |scedulestatus |expected-start-date |scedule-end-date|

Example values
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


Content (This table will be used to add schedule details)

| id        |schedule-id| content            | content-detail       | parent_id                  |order   | duration   | config  | context | context-id   | prerequisite   | post-action | status   |
|-----------|-----------|--------------------|----------------------|----------------------------|------  |---------   |---------|--------- |------------ |----------------|-------------|----------|
|primary key|foreign key|Topic or agenda item| cotent details, urls | To decide topic or subtopic|ordering| Ideal time |metadate |related to|related to id| prerequisite   |post-action   |published |


subscription

| id    | schedule-id  | start-date     | end-date  | assignee | assigned_by  | self-assign | status |
|-------|--------------|----------------|-----------|----------|--------------|-------------|--------|
|       |              |                |           |          |              |             |        |

tracking

| id    | schedule-id  | content-id     | created-date  | start-date |completed-date| assignee | assigned_by  | self-assign | delay  | status |
|-------|--------------|----------------|---------------|------------|--------------|----------|--------------|-------------|--------|--------|
|       |              |                |               |            |              |          |              |             |        |        |



