---
title: System properties for configuring Email Interaction
description: You can manage certain workflows based on system properties, such as enabling or disabling the creation of email interactions for guest users. You can set an inactivity period after which email interactions are automatically closed. Configure the system to create single or multiple outbound email interactions when different agents contact the same customer, enable rerouting, and set reminder periods.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Email Interaction for CSM]
breadcrumb: [Email Interaction, Email channel, Enable communication channels, Configure, Customer Service Management]
---

# System properties for configuring Email Interaction

You can manage certain workflows based on system properties, such as enabling or disabling the creation of email interactions for guest users. You can set an inactivity period after which email interactions are automatically closed. Configure the system to create single or multiple outbound email interactions when different agents contact the same customer, enable rerouting, and set reminder periods.

Navigate to **All****&gt;System Properties****&gt;All Properties** .

Alternatively, in your instance, enter `sys_properties.list` in the filter navigator and customize the Email Interaction system properties.

<table id="table_qbv_3d4_pwb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_eaai\_csm.create\_interaction\_for\_non\_matched\_user**

</td><td>

Enable or disable interaction creation for a non-matched user.-   Type: Boolean \(true \| false\)
-   Default value: true
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

**sn\_eaai\_csm.period\_of\_customer\_inactivity\_to\_close\_interaction**

</td><td>

Set the inactivity period \(in days\) after which an interaction is closed if no email is received from the customer.-   Type: Integer
-   Default value: 5
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

**sn\_eaai\_csm.email\_addresses**

</td><td>

Specify the default email address for creating email interactions. This can contain a comma-separated list of email addresses. Emails sent to any of these addresses generate email interactions.-   Type: String
-   Default value: customerservice@example.com

**Note:** customerservice@example.com is a sample email address.

-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

**period\_for\_reminders\_to\_customers\_interaction**

</td><td>

Specify the number of days after which an automatic email reminder is sent to customers. This value determines how long the system waits after receiving the last email response from the customer before sending a reminder. Reminders are sent only on interactions that are on hold. **Note:** The value must be positive integer. If the value is set to zero or a negative number, the system defaults to 2 days.

-   Type: Integer
-   Default value: 2
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

sn\_eaai\_csm.email.reroute.enabled

</td><td>

Enable or disable the rerouting of interactions that are currently on hold.-   Type: Boolean \(true \| false\)
-   Default value: false
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

sn\_eaai\_core.create\_outbound\_interaction\_per\_agent.target\_tables

</td><td>

Specify a comma-separated list of target tables for which a new outbound interaction is created when different agents initiate outbound email drafts for the same customer. When a table is listed, a new outbound interaction is created for each outbound email initiated by different agents for the same customer. When a table isn’t listed, all agent drafts are consolidated into a single WIP interaction with ownership assigned to the first sending agent.-   Type: String
-   Default value: \(empty\)
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

sn\_eaai\_csm.email.reroute.enabled

</td><td>

Enable rerouting of On Hold email interactions to available agents when the assigned agent isn’t available to handle a customer response. When set to false, the interaction state is updated to Work in Progress without rerouting.-   Type: Boolean \(true \| false\)
-   Default value: false
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

period\_for\_reminders\_to\_customers\_interaction

</td><td>

Specify the time period \(in hours\) after which a reminder email is sent to customers who haven’t responded to an outbound interaction. The minimum value is 1 hour. The scheduled job for sending reminders runs every 24 hours. Only outbound interactions with at least one agent-initiated email are considered.-   Type: Integer
-   Default value: \(configurable\)
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr></tbody>
</table>**Related topics**  


[Display the most recent reply in the Activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-last-viewed-timestamps-activity-stream.md)

