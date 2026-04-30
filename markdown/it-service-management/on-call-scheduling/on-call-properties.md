---
title: System properties for On-Call Scheduling
description: The property settings configure On-Call Scheduling operations.
locale: en-US
release: zurich
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, On-Call Scheduling, IT Service Management]
---

# System properties for On-Call Scheduling

The property settings configure On-Call Scheduling operations.

## Setting properties from the UI

You can set most property values from the On-Call Properties page at **On-Call Scheduling** &gt; **Administration** &gt; **On-Call Properties**.

<table id="table_yrn_sy2_q5"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.on\_call\_rotation.calendar\_macro

</td><td>

The name of the macro that provides a calendar functionality for On-Call shift. The default uses DHTMLX scheduler. Fullcalendar is set by ocf\_calendar.xml.

</td></tr><tr><td>

com.snc.on\_call\_rotation.support\_legacy\_spans

</td><td>

Used to search for override or time-off records that may have been generated as cmn\_schedule\_span records and not the standard roster\_schedule\_span table.

</td></tr><tr><td>

com.snc.on\_call\_rotation.pto.approval.required

</td><td>

Configuration to determine if PTO requests need approval.

</td></tr><tr><td>

com.snc.on\_call\_rotation.factor\_daily\_rotation\_interval\_all\_day

</td><td>

If true, mandates daily rotation to occur at midnight. If false, then use the time that is specified for the roster start time for the next day. Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.log.level

</td><td>

Enable logs for debugging.Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.log\_escalations

</td><td>

Enable logging of escalations. See [View details in an escalation log](../task/view-escalation-logs-oncall.md).Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.calendar\_macro

</td><td>

The name of the macro that provides a calendar for On-Call shift. The default uses DHTMLX scheduler. Fullcalendar is set by **ocf\_calendar.xml**.Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.support\_legacy\_spans

</td><td>

Used to search for override or time-off records that may have been generated as records in the cmn\_schedule\_span table and not in the standard roster\_schedule\_span table.Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.pto.approval.required

</td><td>

Configuration to determine whether PTO requests require approval.Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.contrast

</td><td>

Sets text color to either white or black depending on which has the highest contrast with the background color on the calendar. The following algorithms determine text color: -   ContrastYIQ
-   ContrastPercent
-   ContrastLuminance

 **Note:** ContrastYIQ is used if the property is not enabled.

 Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.access.debug

</td><td>

If true, enable general On-Call logs for debugging.Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.reminders.showtz

</td><td>

Include a user's time zone in On-Call Shift Reminder notification emails.Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.show\_legacy\_calendar

</td><td>

Show the legacy On-Call calendar.Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.calendar\_read\_roles

</td><td>

Comma-separated list of roles that can read the calendar.Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.cover.color

</td><td>

Sets the color of the span for On-Call coverage for another roster member.Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.timeoff.color

</td><td>

Sets the color of the span when the type is time-off.Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.on\_call\_rotation.landing\_page.group\_limit

</td><td>

The number of On-Call schedules loaded per batch on the client side. Default: 20.

</td></tr><tr><td>

com.snc.on\_call\_rotation.landing\_page.max\_groups

</td><td>

The maximum number of On-Call schedules that can be loaded on the client side. Default: 300.**Note:** The default value is chosen as the limit of acceptable client performance.

</td></tr><tr><td>

com.snc.on\_call\_rotation.landing\_page.pinned\_notification

</td><td>

Displays a message when any schedule is pinned successfully.

</td></tr><tr><td>

com.snc.on\_call\_rotation.landing\_page.notification\_timeout

</td><td>

Specifies the time \(in milliseconds\) until the message for successful pinned scheduled is displayed.

</td></tr><tr><td>

com.snc.on\_call\_rotation.landing\_page.show\_wizard\_btn

</td><td>

Displays the **New** button to open the On-Call schedule wizard.

</td></tr><tr><td>

com.snc.iam.conference\_call\_follow\_on\_call\_escalation

</td><td>

If selected, On-Call the escalation path is followed when a user group is added to a conference call.This property is added when the Incident Communications Management \(com.snc.iam\) plugin is activated.

</td></tr><tr><td>

com.snc.iam.conference\_call\_escalation\_workflow

</td><td>

If selected, custom escalation hierarchy is applicable in On-Call Scheduling workflows.This property is added when the Incident Communications Management \(com.snc.iam\) plugin is activated.

</td></tr><tr><td>

com.snc.on\_call\_rotation.landing\_page.show\_pending\_actions

</td><td>

If true, displays the pending actions on the On-Call Schedules landing page.

</td></tr><tr><td>

com.snc.on\_call\_rotation.allow\_rota\_overlap

</td><td>

If true, overlapping shifts are allowed for a user group.

</td></tr><tr><td>

com.snc.on\_call\_rotation.escalation\_rule\_rota\_overlap

</td><td>

Escalation rule that applies for shift overlap. Options:-   Escalate to outgoing Shift
-   Escalate to incoming Shift
-   Escalate to all Shifts

</td></tr><tr><td>

com.snc.on\_call\_rotation.pto.configuration

</td><td>

Specifies how a roster member can create vacation time \(PTO\). Options:-   With approval
-   Without approval
-   Not allowed

</td></tr><tr><td>

com.snc.notify.default.conference\_call\_follow\_on\_call\_escalation

</td><td>

If true, the On-Call escalation path is followed when a user group is added to a conference call. However, the time between reminders is set to 60 secs. Users can create properties for required task types such as incident. Example: For Incident, the property key would be **com.snc.notify.incident.conference\_call\_follow\_on\_call\_escalation**.**Note:** The property is enabled only when the [Notify](https://www.servicenow.com/docs/access?context=t_ActivateNotify&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) plugin \(com.snc.notify\) is active.

</td></tr><tr><td>

com.snc.notify.default.on\_call\_escalation\_level

</td><td>

Fetches the number of users from the group escalation plan. A value of **-1** fetches all users from the plan. A value of 1 fetches only the first level of users, and so on. **Note:**

-   This is the default property that is used until the specific property for the task type is configured. To use different workflows for different task types \(such as incident or problem\), create a new property by replacing the word `default` in the key with the task type.
-   This property is used only when the **com.snc.notify.default.conference\_call\_follow\_on\_call\_escalation** sys property is false.
-   The property is enabled only when the [Notify](https://www.servicenow.com/docs/access?context=t_ActivateNotify&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) plugin \(com.snc.notify\) is active.

</td></tr><tr><td>

com.snc.notify.default.conference\_call\_escalation\_workflow

</td><td>

The sys\_id of the default workflow that must be attached when escalating a conference call.**Note:**

-   This is the default property that is used until the specific property for the task type is configured. To use different workflows for different task types \(such as incident or problem\), create a new property by replacing the word `default` in the key with the task type. Example: For Incident, the property key would be **com.snc.notify.incident.conference\_call\_escalation\_workflow**.
-   The property is enabled only when the [Notify](https://www.servicenow.com/docs/access?context=t_ActivateNotify&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) plugin \(com.snc.notify\) is active.

</td></tr><tr><td>

com.snc.on\_call\_rotation.use\_slack\_for\_dm

</td><td>

If false, disables direct messaging via Slack on all On-Call Scheduling pages.

</td></tr><tr><td>

com.snc.on\_call\_rotation.use\_msteams\_for\_dm

</td><td>

If false, disables direct messaging via Microsoft Teams on all On-Call Scheduling pages.

</td></tr><tr><td>

com.snc.on\_call.announcement\_message

</td><td>

If false, removes the banner of SOW announcement from on\_call\_calendar page.

</td></tr><tr><td>

com.snc.on\_call\_rotation.new\_trigger\_engine

</td><td>

If true, a new on-call trigger engine is activated which enables on-call subflows get triggered via flow runner queue. As the on-call subflows are marked as high priority they get processed faster via flow runner queue compared to the traditional event queue especially when multiple events are triggered at the same time and are in the process queue.

</td></tr></tbody>
</table>**Parent Topic:**[Reference for on-call scheduling](../../user-administration/concept/reference-for-on-call-scheduling.md)

