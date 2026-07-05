---
title: "Worklog Week 12"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

* Integrate and test the full Event Management module (frontend + backend).
* Align EventDto and Status with Tâm for the Registration and Auth modules.
* Record results and capture screenshots/video for the workshop report.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Review the full flow from Event List → Event Detail → Admin Create/Update/Delete. <br> - Check data consistency between the Frontend, Lambda, and EventTable. | 06/07/2026 | 06/07/2026 | https://cloudjourney.awsstudygroup.com/ |
| 3 | - Meet with Tâm to align EventId, EventDto, and Status (Draft/Active/Ended/Cancelled) so the Registration module reads AvailableSlots correctly. <br> - Align the Admin authorization mechanism with the Auth module. | 07/07/2026 | 07/07/2026 | https://cloudjourney.awsstudygroup.com/ |
| 4 | - Fix issues that arise after alignment (if any field/format changes are needed). <br> - **Practice:** Re-test the full APIs and UI after the adjustments. | 08/07/2026 | 08/07/2026 | https://cloudjourney.awsstudygroup.com/ |
| 5 | - Run end-to-end tests: create event → display in public view → edit/cancel → verify updates on the frontend. <br> - Check banner upload/display on both the public and admin pages. | 09/07/2026 | 09/07/2026 | https://cloudjourney.awsstudygroup.com/ |
| 6 | - Capture screenshots of the main features. <br> - Record a short demo video: Event List, Event Detail, Admin create/edit/cancel event. <br> - Summarize the results of the Event Management module for the workshop report. | 10/07/2026 | 10/07/2026 | https://cloudjourney.awsstudygroup.com/ |

### Week 12 Achievements:

* Completed the integration of the full Event Management module: the frontend (public + admin) worked stably with the Backend Lambda and EventTable.

* Successfully aligned EventId, EventDto, and Status with Tâm, ensuring the Registration module read AvailableSlots correctly and only allowed registration for Active events.

* Successfully aligned the Admin authorization mechanism with the Auth module, ensuring security for the create/update/delete APIs.

* Event List and Event Detail ran stably on the frontend with real data from EventTable.

* The Admin could create/edit/cancel events successfully, with data synced correctly to EventTable and banners/posters stored properly in S3.

* Completed screenshots and a short demo video for the main features.

* Delivered the full results of the Event Management module for the workshop report.
