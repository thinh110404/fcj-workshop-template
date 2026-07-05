---
title: "Worklog Week 11"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Build the Admin interface for creating events.
* Build the Admin interface for editing/canceling events.
* Handle form validation, banner upload, loading/error states, and success notifications.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Design the wireframe for the Admin event creation form. <br> - Define the fields: Title, Description, Location, StartTime, EndTime, TotalSlots, Status, and banner upload. | 29/06/2026 | 29/06/2026 | https://cloudjourney.awsstudygroup.com/ |
| 3 | - Build the event creation form. <br> - Implement form validation (required fields, StartTime < EndTime, TotalSlots > 0). <br> - Handle banner selection and preview before upload. | 30/06/2026 | 30/06/2026 | https://cloudjourney.awsstudygroup.com/ |
| 4 | - Connect the form to the API POST /events. <br> - Handle banner upload together with the event creation request. <br> - **Practice:** Test successful and failed event creation and display notifications. | 01/07/2026 | 01/07/2026 | https://cloudjourney.awsstudygroup.com/ |
| 5 | - Build the Admin Edit Event interface: load existing data into the form, allow updates, and change the banner. <br> - Implement logic to change the Status: Draft/Active/Ended/Cancelled. | 02/07/2026 | 02/07/2026 | https://cloudjourney.awsstudygroup.com/ |
| 6 | - Connect to the APIs PUT /events/{id} and DELETE /events/{id}. <br> - **Practice:** <br>&emsp; + Test updates, status changes, and event cancellation <br>&emsp; + Handle loading/error/success notifications for the entire Admin form | 03/07/2026 | 03/07/2026 | https://cloudjourney.awsstudygroup.com/ |

### Week 11 Achievements:

* Completed the Admin interface for creating events: users can enter the full information, upload a banner/poster, and validate the form before submission.

* Completed the Admin interface for editing/canceling events: users can update information, change the status, and manage the event lifecycle.

* Successfully connected the interface to the APIs POST /events, PUT /events/{id}, and DELETE /events/{id}.

* Handled loading states, API errors, form validation, and success notifications.

* The Admin can manage the full event lifecycle from the interface, with data synchronized correctly with EventTable and S3.

* Completed the Admin portion of the Event Management module.
