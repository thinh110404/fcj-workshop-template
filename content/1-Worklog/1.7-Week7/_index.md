---
title: "Worklog Week 7"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Design the data structure for the Event Management module (EventTable in DynamoDB).
* Initialize storage infrastructure for event banners/posters (S3 Bucket).
* Prepare the project framework for Event-CRUD-Lambda.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Analyze the requirements of the Event Management module. <br> - Identify the necessary attributes for EventTable: EventId, Title, Description, Location, StartTime, EndTime, TotalSlots, AvailableSlots, BannerUrl, Status, CreatedAt, UpdatedAt | 01/06/2026 | 01/06/2026 | https://cloudjourney.awsstudygroup.com/ |
| 3 | - Learn about DynamoDB: Partition Key, Sort Key, Data Types. <br> - Design the EventTable schema in DynamoDB. <br> - Define Status values: Draft/Active/Ended/Cancelled | 02/06/2026 | 02/06/2026 | <https://docs.aws.amazon.com/dynamodb/> |
| 4 | - **Practice:** Create the EventTable on the AWS Console. <br>&emsp; + Configure Partition Key = EventId <br>&emsp; + Configure capacity mode (On-demand) <br> - Insert sample data to test the schema | 03/06/2026 | 03/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/> |
| 5 | - Learn about Amazon S3: Bucket, Object, Permission, Presigned URL. <br> - Design the storage structure for banners/posters (naming convention, folder by EventId) | 04/06/2026 | 04/06/2026 | <https://docs.aws.amazon.com/s3/> |
| 6 | - **Practice:** <br>&emsp; + Create the S3 Bucket "event-assets" <br>&emsp; + Configure access permissions (Bucket Policy, CORS) <br>&emsp; + Upload a test image and retrieve a public URL <br> - Record the data structure to align with the team (EventDto) | 05/06/2026 | 05/06/2026 | <https://docs.aws.amazon.com/s3/> |

### Week 7 Achievements:

* Completed the EventTable schema design on DynamoDB with the required attributes:
  * EventId (Partition Key)
  * Title, Description, Location
  * StartTime, EndTime
  * TotalSlots, AvailableSlots
  * BannerUrl
  * Status (Draft/Active/Ended/Cancelled)
  * CreatedAt, UpdatedAt

* Successfully created the EventTable on AWS DynamoDB and verified read/write operations with sample data.

* Created a dedicated S3 Bucket for storing event banners/posters, with access permissions and CORS configured appropriately for frontend upload.

* Defined the rule that when a new event is created, AvailableSlots is initialized to TotalSlots.

* Prepared the initial EventDto structure to align with the team for the Registration and Auth modules.

* Built the initial project framework for Event-CRUD-Lambda, ready for API logic implementation in the following week.
