---
title: Create a renewal notification for MS Teams
description: Create your notification for Microsoft Teams.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "0256-02-16"
reading_time_minutes: 1
breadcrumb: [Configure for MS Teams Integration, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Create a renewal notification for MS Teams

Create your notification for Microsoft Teams.

## Before you begin

Make sure you configured your SN platform for MS Teams. For more info, [Configure for MS Teams Integration](cim-ms-teams-integration.md).

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Shecduled Jobs**.

2.  Select the table, **Certificate Notification**

3.  Fill out the following fields

<table><tbody><tr><td id="d259403e89">

**Field**

</td><td>

Value

</td></tr><tr><td id="d259403e98">

**Name**

</td><td>

Name of your notification

</td></tr><tr><td id="d259403e107">

**Active**

</td><td>

Enabled \| Disabled

</td></tr><tr><td id="d259403e116">

**Application**

</td><td>

Certificate Inventory and Management

</td></tr><tr><td id="d259403e126">

**Conditional**

</td><td>

Enabled \| Disabled

</td></tr><tr><td id="d259403e136">

**Run**

</td><td>

Daily \| Weekly \| Monthly

</td></tr><tr><td id="d259403e145">

**Time Zone**

</td><td>

If you need to run inside a certain time zone, specifiy here.

</td></tr><tr><td id="d259403e154">

**Time**

</td><td>

Time the notification will run

</td></tr><tr><td id="d259403e163">

**Advanced**

</td><td>

Enabled \| Disabled

</td></tr><tr><td id="d259403e172">

**Starting**

</td><td>

Date and time the notification begins

</td></tr><tr><td id="d259403e181">

**Ending**

</td><td>

Date and time the notification ends

</td></tr><tr><td id="d259403e191">

**Repeat Every**

</td><td>

Every N Days \| Weeks \| Months the notification is sent

</td></tr></tbody>
</table>4.  Select **Update**.

    **Note:** By selecting **Execute Now**, you are testing the notification.


## Result

At the requested times, your Certificate Inventory and Management application automatically sends a message to your Microsoft Teams Channel that a certificate has expired or is about to expire.

