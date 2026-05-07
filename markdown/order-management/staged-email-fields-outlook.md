---
title: Staged Email table
description: Field descriptions for viewing email records linked to CRM entities in the Staged Email \[sys\_email\_staging\] table.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [staged email fields, CRM Outlook, email association]
breadcrumb: [Activity Management reference, Lead and opportunity management, Reference, Sales Customer Relationship Management]
---

# Staged Email table

Field descriptions for viewing email records linked to CRM entities in the Staged Email \[sys\_email\_staging\] table.

|Field|Description|
|-----|-----------|
|Receive type|Processing status of the email, such as New.|
|Target|CRM record the email is linked to, displayed as record type and number. For example, Lead: LEAD0000001.|
|User|Email address of the user who sent the email.|
|User ID|User ID of the user associated with the email, if one exists.|
|UID|Unique identifier for the email message.|
|Importance|Priority level of the email if specified by the sender.|
|Deleted|Indicates whether the email has been marked as deleted.|
|Target table|Database table of the linked CRM record, such as Lead \[sn\_lead\_mgmt\_core\_lead\].|
|Reply to|Email address specified for replies if different from the sender.|
|Recipients|Email addresses of all recipients, including the **To** and **CC** fields.|
|Subject|Subject line of the email.|
|Headers|Any headers embedded in the email, such as routing details, authentication results, and server timestamps.|
|Content type|The MIME \(Multipurpose Internet Mail Extension\) media type of the email content stored in this record. This value indicates how the email body should be interpreted and rendered by email clients, including the content format and character encoding. For example, `text/html; charset=utf-8`.|
|Body|HTML-formatted content of the email.|
|Body text|Plain text version of the email content.|

**Parent Topic:**[Activity Management reference](../concept/activity-management-reference.md)

**Related topics**  


[Track emails linked from Microsoft Outlook](../task/view-associated-emails-crm.md)

