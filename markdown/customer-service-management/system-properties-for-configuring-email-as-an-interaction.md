---
title: System properties for configuring Email Interaction
description: You can manage certain workflows based on the system properties, such as enabling or disabling the creation of email interactions for guest users. You can set an inactivity period after which email interactions are automatically closed.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Email Interaction for CSM]
breadcrumb: [Email Interaction, Email channel, Configure, Enable communication channels, Configure, Customer Service Management]
---

# System properties for configuring Email Interaction

You can manage certain workflows based on the system properties, such as enabling or disabling the creation of email interactions for guest users. You can set an inactivity period after which email interactions are automatically closed.

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

Specify the number of days after which an automatic email reminder is sent to customers. This value determines how long the system waits after receiving the last email response from the customer before sending a reminder. Reminders are sent only on interactions that are on hold. **Note:** The value must be positive integer. If the value is set to 0 or a negative number, the system defaults to 2 days.

-   Type: Integer
-   Default value: 2
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

sn\_eaai\_csm.email.reroute.enabled

</td><td>

Enable or disable the rerouting of interactions that are currently on hold.-   Type: Boolean \(true \| false\)
-   Default value: false
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr></tbody>
</table>**Related topics**  


[Display the most recent reply in the Activity stream](https://www.servicenow.com/docs/access?context=configure-last-viewed-timestamps-activity-stream&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

