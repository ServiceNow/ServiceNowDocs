---
title: Create a user for Redox Inbound Integration
description: Create a user for the Redox Inbound Integration application to receive data from a Redox healthcare system.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Redox Inbound Integration, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Create a user for Redox Inbound Integration

Create a user for the Redox Inbound Integration application to receive data from a Redox healthcare system.

## Before you begin

**Important:**

Starting with the Yokohama release, Redox Inbound Integration is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  In the Users list, click **New**.

3.  On the User form, fill in the details of the user including ID, first and last names, calendar integration, and time zone.

4.  In the **Password** field, enter a password for the user.

    This password can be permanent or temporary.

5.  Enable the user to change the password during the first login by selecting the **Password needs reset** check box.

6.  Select the **Active** check box.

7.  To designate this user as a non-interactive user, select the **Web service access only** check box.

8.  Click **Submit**.


## What to do next

[Assign roles for Redox Inbound Integration users](hcls-redox-assign-roles.md).

**Related topics**  


[bundle-platadm.t_CreateAUser]

