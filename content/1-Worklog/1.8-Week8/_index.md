---
title: "Worklog Week 8"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Build Event-CRUD-Lambda to handle event data operations.
* Implement the API GET /events (public event list, prioritizing Active events).
* Implement the API GET /events/{id} (event detail).
* Connect API Gateway with Lambda and test through Postman.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn about AWS Lambda: runtime, handler, event object, and context object. <br> - Learn how Lambda connects to DynamoDB via SDK (boto3/AWS SDK for JS). | 08/06/2026 | 08/06/2026 | <https://docs.aws.amazon.com/lambda/> |
| 3 | - Initialize the Event-CRUD-Lambda project. <br> - Configure the Lambda IAM role (read/write DynamoDB permissions). <br> - Write functions to scan/query event data from EventTable. | 09/06/2026 | 09/06/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/> |
| 4 | - Write the API GET /events logic: <br>&emsp; + Filter and prioritize events with Status = Active <br>&emsp; + Format the response according to EventDto <br> - **Practice:** Deploy Lambda and test it via AWS Console (Test Event). | 10/06/2026 | 10/06/2026 | <https://docs.aws.amazon.com/apigateway/> |
| 5 | - Write the API GET /events/{id} logic: <br>&emsp; + Get the EventId from the path parameter <br>&emsp; + Query DynamoDB by Partition Key <br>&emsp; + Handle the case where the event is not found (404). | 11/06/2026 | 11/06/2026 | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/> |
| 6 | - **Practice:** <br>&emsp; + Create API Gateway, configure routes GET /events and GET /events/{id} <br>&emsp; + Connect the routes to Lambda (Lambda Proxy Integration) <br>&emsp; + Test the API via Postman <br> - Record logs and handle basic exceptions. | 12/06/2026 | 12/06/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/> |

### Week 8 Achievements:

* Completed Event-CRUD-Lambda with the ability to connect to and query data from EventTable.

* Successfully implemented API GET /events:
  * Return the list of events.
  * Prioritize events with Status = Active.
  * Return data in the EventDto format aligned with the team.

* Successfully implemented API GET /events/{id}:
  * Return full event details by EventId.
  * Handle the case where the event does not exist (return a 404 response).

* Successfully configured API Gateway to connect with Lambda through Lambda Proxy Integration.

* Tested the GET /events and GET /events/{id} APIs successfully through Postman, with the expected data returned.

* Learned basic error handling (try/catch, response status codes) in Lambda.

* Prepared for the implementation of write APIs (POST/PUT/DELETE) in the following week.
