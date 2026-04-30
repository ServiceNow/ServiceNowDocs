---
title: Send certification task reminders
description: The Certification Task Escalations workflow sends automatic email reminders.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Send certification task reminders

The Certification Task Escalations workflow sends automatic email reminders.

The Certification Task Escalations workflow sends automatic email reminders to the:

-   Certification task owner.
-   Assignment group, if the assignment group was specified on the Certification Task form.
-   Manager of the certification task owner, if necessary and if a manager was specified on the User form.

The reminders are based on the Complete by field on the certification task record. If the Complete by date is changed, the reminder schedule automatically adjusts to reflect the new date.

|Time elapsed to end date|Email reminder is sent to|Escalate field on task record reads|
|------------------------|-------------------------|-----------------------------------|
|50%|task owner and assignment group \(if specified\)|Moderate|
|75%|task owner, assignment group, and manager of the task owner|High|
|95%|task owner, assignment group, and manager of the task owner|High|
|100%|task owner, assignment group, and manager of the task owner|High|

To set reminders for different or more intervals, edit the workflow Certification Task Escalations. In addition to the email reminders sent automatically, users with the certification\_admin role can send email reminders manually at any time.

