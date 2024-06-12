# scheduler
This service provides the functionalities of scheduling the curriculum or syllabus or schedule or target plan. It is written in [Nest JS](https://github.com/nestjs/nest)

Database design

Schedule
| id    | title        | config         |   status     | start-date | end-date|
|-------|--------------|----------------|--------------|------------|---------|
|       |              |                |              |            |         |

Content

| id    |schedule-id| content  | content-detail | parent_id |order| duration | config  | context | context-id | prerequisite   | post-action | status   |
|-------|-----------|----------|----------------|-----------|------|---------|---------|---------|------------|----------------|-------------|----------|
|  1    |           |grammer   | Basic sentence | 0         |      | 1 week  | {JSON } |         |            | Letter knowing |assignment   |published |


subscription

| id    | schedule-id  | start-date     | end-date  | assignee | assigned_by  | self-assign | status |
|-------|--------------|----------------|-----------|----------|--------------|-------------|--------|
|       |              |                |           |          |              |             |        |

tracking

| id    | schedule-id  | content-id     | created-date  | start-date |completed-date| assignee | assigned_by  | self-assign | delay  | status |
|-------|--------------|----------------|---------------|------------|--------------|----------|--------------|-------------|--------|--------|
|       |              |                |               |            |              |          |              |             |        |        |



