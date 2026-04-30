---
title: Configure an email notification for an exposure notice
description: Configure an email notification to use in the Emergency Outreach to send to potentially exposed contacts in an exposure case to notify them of potential exposure from an affected employee.
locale: en-US
release: xanadu
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure an email notification for an exposure notice

Configure an email notification to use in the Emergency Outreach to send to potentially exposed contacts in an exposure case to notify them of potential exposure from an affected employee.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notifications** &gt; **Email** &gt; **Notifications**.

2.  Review the existing **Notify Exposed Contact** email notification to familiarize yourself with the script and other settings.

3.  Click **New**.

4.  In the **Table** field, select the Exposure Notice \[sn\_imt\_tracing\_exposure\_notice\] table.

5.  On the **When to send** tab, complete the following settings.

    1.  In the **Send when** field, select **Record inserted or updated**.

    2.  Set the **Conditions** criteria to **\[User.Active\]\[is\]\[true\]** and **\[Notification count\]\[changes\]**.

    3.  In the **Advanced condition** field, enter the following code:

        ```
        var exposedContactNotificationSysId = '<your-sys_id>';
        answer = current.outreach.notification == exposedContactNotificationSysId;
        
        ```

        Replace the &lt;your-sys\_id&gt; variable with the sys\_id notification that you're adding by right-clicking in the header, selecting the **Copy sys\_id** option, and pasting the sys\_id into the code line.

6.  On the **Who will receive** tab, open **Users/Groups in fields** and select **Assigned to**.

7.  Complete the remaining information on the **What it will contain** tab.

8.  Click **Submit**.

9.  In the Notifications list, open the notification that you added and click **Preview Notification**.

10. Review the notification and make any changes required.

11. Click **Update**.


## What to do next

[Configure an Emergency Outreach notification for the exposure notice](configure-outreach-notify-exp-contact.md).

**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)

