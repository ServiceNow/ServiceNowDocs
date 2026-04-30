---
title: Status communication to Magnit
description: Understand how the status of user onboarding tasks are communicated from the ServiceNow instance to the Magnit application.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Explore HR Service Delivery Integration with Magnit, HR Service Delivery Integration with Magnit, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Status communication to Magnit

Understand how the status of user onboarding tasks are communicated from the ServiceNow® instance to the Magnit application.

## Flow

1.  Changing the status of an HR task to Work in progress, Ready, or Draft, automatically changes the status of its corresponding user onboarding item to Pending state in the User Onboarding Item \[sn\_hr\_magnit\_user\_onboarding\_item\] table. When the HR task is marked as Complete or Closed Incomplete or Cancelled, the status of its corresponding user onboarding item automatically changes to **Ready to Send** in the User Onboarding Item \[sn\_hr\_magnit\_user\_onboarding\_item\] table.
2.  The Synchronise attachments of onboarding items flow runs at a specific schedule and time, reads the User Onboarding Item \[sn\_hr\_magnit\_user\_onboarding\_item\] table to identify records with **Status** value = **Ready to Send**. The Send onboarding status action in Magnit spoke passes these details to the Magnit application, and a correlation ID is received for all the records that are sent to Magnit system. The records in User Onboarding Item \[sn\_hr\_magnit\_user\_onboarding\_item\] table are updated with Correlation\_ID, status\_sent\_at and status\_sent.

    **Note:**

    -   Closed and Closed Incomplete states are mapped to Completed in Magnit, and Cancelled is mapped to Rejected in Magnit.
    -   Attachments greater than 5 MB are discarded and not sent to Magnit application.
3.  The Synchronise Attachments of Onboarding Items flow reads the User Onboarding Item \[sn\_hr\_magnit\_user\_onboarding\_item\] table and identifies the last correlation ID and the Verify onboarding status action in Magnit spoke identifies the last status sent information. Once the response is identified as completed, the next batch of records \(if at all there are any changes in the status of the records\) are sent to Magnit application.

