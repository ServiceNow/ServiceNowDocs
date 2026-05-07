---
title: Configure for MS Teams Integration
description: Certificate Inventory and Management integrates with Microsoft Teams. You can receive message notifications when your certificate needs renewal and renew from the notification.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "0256-02-16"
reading_time_minutes: 1
breadcrumb: [Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Configure for MS Teams Integration

Certificate Inventory and Management integrates with Microsoft Teams. You can receive message notifications when your certificate needs renewal and renew from the notification.

## Before you begin

Download two dependent applications from the Servicenow store, sn\_msteams\_ahv2 and sn\_sow\_srm\_common. Make sure your MS Teams is configured, for more info, see [https://www.servicenow.com/docs/r/integrate-applications/integration-hub/set-up-msteams.html](https://www.servicenow.com/docs/r/integrate-applications/integration-hub/set-up-msteams.html).

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **sn\_disco\_certmgmt\_microsoft\_teams\_notifications.LIST**.

    **Note:** You will manually enter into the navigation search field sn\_disco\_certmgmt\_microsoft\_teams\_notifications.LIST

2.  Select **New**

3.  Fill out the following fields

<table><tbody><tr><td id="d100853e83">

**Field**

</td><td>

Value

</td></tr><tr><td id="d100853e92">

**Notification alias**

</td><td>

Name of your notification

</td></tr><tr><td id="d100853e101">

**Event**

</td><td>

Expiring \| Expired

</td></tr><tr><td id="d100853e110">

**Team**

</td><td>

The group in your organization creating the notification

</td></tr><tr><td id="d100853e119">

**Microsoft Teams Channel Link**

</td><td>

The URL link to your MS Teams channel **Note:** You can find this link on MS Teams while you are in the channel.

</td></tr><tr><td id="d100853e131">

**Microsoft Channel Name**

</td><td>

Name of your channel inside the team \(optional\)

</td></tr><tr><td id="d100853e140">

**Microsoft Team Name**

</td><td>

Name of the team \(optional\)

</td></tr></tbody>
</table>4.  Select **Update**.


## Result

Certificate notifications will appear as messages in the MS teams channel that you choose.

