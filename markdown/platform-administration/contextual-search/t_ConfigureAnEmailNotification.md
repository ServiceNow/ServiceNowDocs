---
title: Edit an email notification for the search results
description: Include search results in an email notification sent to users.
locale: en-US
release: zurich
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, Contextual search, Search administration, Configure core features, Administer]
---

# Edit an email notification for the search results

Include search results in an email notification sent to users.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Open the email template that you want to modify to include search results.

3.  Select **What it will contain**.

4.  In the **Message HTML** field, add the following script:

    `${mail_script:cxs_EmailSearchResults}`

    ![Notification form's What it will contain section with script added to Message HTML field.](../image/edit-email-notification.png)

5.  Select and hold \(or right-click\) on the header form and click **Save**.


**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)

