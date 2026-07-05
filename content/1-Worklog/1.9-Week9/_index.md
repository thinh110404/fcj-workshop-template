---
title: "Worklog Week 9"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Implement the write APIs: POST /events, PUT /events/{id}, DELETE /events/{id}.
* Build the logic to upload event banners/posters to S3 and save BannerUrl to EventTable.
* Check and apply Admin authorization for the create/update/delete APIs.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Write the API POST /events logic: <br>&emsp; + Validate input data (Title, StartTime, EndTime, TotalSlots, etc.) <br>&emsp; + Initialize AvailableSlots = TotalSlots <br>&emsp; + Automatically assign CreatedAt/UpdatedAt | 15/06/2026 | 15/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/> |
| 3 | - Write the API PUT /events/{id} logic: <br>&emsp; + Update event information <br>&emsp; + Allow changes to Status: Draft/Active/Ended/Cancelled <br>&emsp; + Update UpdatedAt | 16/06/2026 | 16/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/> |
| 4 | - Write the API DELETE /events/{id} logic: <br>&emsp; + Delete permanently or change the status to Cancelled (soft delete) <br> - **Practice:** Test the three APIs via Postman for valid and invalid cases | 17/06/2026 | 17/06/2026 | <https://docs.aws.amazon.com/apigateway/> |
| 5 | - Learn about uploading files to S3 from Lambda (base64 or Presigned URL). <br> - Write the logic to handle banners/posters: upload the image to the Event Assets S3 Bucket, get the URL, and save it to BannerUrl in EventTable | 18/06/2026 | 18/06/2026 | <https://docs.aws.amazon.com/s3/> |
| 6 | - Learn about Cognito/JWT: how to validate tokens and decode claims. <br> - **Practice:** <br>&emsp; + Write middleware to check JWT and the Admin role <br>&emsp; + Apply the middleware to POST/PUT/DELETE <br>&emsp; + Test unauthorized cases (401/403) | 19/06/2026 | 19/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/> |

### Week 9 Achievements:

* Successfully implemented API POST /events to create a new event, automatically initialize AvailableSlots with TotalSlots, and store the data correctly in EventTable.

* Successfully implemented API PUT /events/{id} to update event information and change Status according to the Draft → Active → Ended/Cancelled lifecycle.

* Successfully implemented API DELETE /events/{id} to handle deletion or change the event status to Cancelled.

* Completed the logic to upload banners/posters to the Event Assets S3 Bucket and save BannerUrl correctly to EventTable.

* Successfully applied Admin authorization checks (JWT/Cognito) to the create/update/delete APIs and blocked invalid requests.

* Tested all 5 APIs (GET, GET/{id}, POST, PUT, DELETE) through Postman, ensuring the business logic worked correctly.

* Completed the Backend/Lambda portion of the Event Management module and prepared it for frontend development.
