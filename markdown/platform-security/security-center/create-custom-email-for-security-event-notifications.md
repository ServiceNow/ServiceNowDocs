---
title: Create a custom email for security event notifications
description: Create a custom email for security event notifications by configuring new notifications, setting triggers, defining recipients, and crafting email content with dynamic event fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/security-center/create-custom-email-for-security-event-notifications.html
release: brazil
product: Security Center
classification: security-center
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure policy preferences, Security Event Notifications, Security monitoring console, Security Center, Platform Security]
---

# Create a custom email for security event notifications

Create a custom email for security event notifications by configuring new notifications, setting triggers, defining recipients, and crafting email content with dynamic event fields.

## Before you begin

Role required: admin

## Procedure

1.  Select **system notifications** &gt; **notification**.

2.  Select **New**.

3.  In the **Name** field, enter a name for the notification.

4.  Select the field next to **Table** and enter security policy notification \(`sn_vsc_security_policy`\).

5.  Configure the new record.

    There are three tabs within the record that must be configured: **When to send**, **Who will receive**, and **What it will contain**.

<table id="table_inf_lxh_2cc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**When to send**

</td><td>

Select the field next to **Send when** label and select **Triggered**.

</td></tr><tr><td>

**Who will receive**

</td><td>

-   Select the local icon next to **Users/Groups in fields**, and select both **Users** and **Groups**. Select the Add Item \(&gt;\) icon to move the fields into the **Selected** text field.
-   Select and hold \(or right-click\) the record header banner and select **Save**.


</td></tr><tr><td>

**What it will contain**

</td><td>

Create an email template.For instructions on creating an email template, see [Create an email template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_CreateAnEmailTemplate.md).

Enter fields of the event into **Message HTML** by using the `${event_id.FIELD_NAME}`. Here's an example:

```

Role: ${event_id.role.URI_REF} 
Granted to: ${event_id.granted_to.URI_REF} 
Granted by: ${event_id.user.URI_REF} 
Logged at: ${event_id.sys_created_on} 
Security Center Notification: ${execution.policy.name}
```

</td></tr></tbody>
</table>6.  Select **Submit**.

7.  Add a custom notification to email template in security event notifications.

    1.  In Security Center, select **Notifications** &gt; **Policy settings**.

    2.  Navigate to the **Notifications** label.

    3.  Enter the name of the custom notification you created in the **Notification** field.


**Parent Topic:**[Configure preferences for security event notification policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/configure-preferences-for-security-event-notifications.md)

