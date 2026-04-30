---
title: View alert information
description: View a list of all alerts for application services s, and then manage individual alerts as necessary.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View alert information

View a list of all alerts for application services s, and then manage individual alerts as necessary.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

Multiple related events may correlate into a single alert. Event Management only creates alerts when one or more events meet the conditions defined in event rules, alert action rules, and alert configuration settings.

When updating an alert, empty field values do not override values inherited from the alert's event.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

    ![Message to try Express list for visualization and management of alerts.](../image/em-express-list-msg.png)

    **Note:** To stop the message from appearing, set the **show\_sow\_enhanced\_experience\_message** property in the \[sys\_properties\] table to false.

2.  To view or manage an alert, click the alert number.

3.  Review the information on the Alert form.

    You can click tabs on the form for further information.

    -   To view flapping information, click the **Flapping** tab.
    -   To view alert history, click the **History** tab.
<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

If an alert was created as a result of the event, this field contains the unique ID that Event Management generates to identify the alert.

</td></tr><tr><td>

Source

</td><td>

Event monitoring software that generated the event, such as SolarWinds or SCOM. Maximum length: 100 characters.

</td></tr><tr><td>

Node

</td><td>

Node name, fully qualified domain name \(FQDN\), IP address, or MAC address that is associated with the event, such as IBM-ASSET. Maximum length: 100 characters.

</td></tr><tr><td>

Type

</td><td>

The metric type to which the event is related, such as Disk or CPU, which is used to identify an event record from which alerts are created. Maximum length: 100 characters.

</td></tr><tr><td>

Resource

</td><td>

Node resource that is relevant to the event. For example, Disk C, CPU-1, the name of a process, or service. Maximum length: 100 characters.

</td></tr><tr><td>

Configuration item

</td><td>

JSON string that represents a configuration item. For example, `{"name":"SAP ORA01","type":"Oracle"}`. The CI identifier that generated the event appears in the **Additional information** field. Maximum length: 1000 characters. Note: Reference pop-ups and click-throughs are hidden by default for read-only fields. For **Configuration item** and other read only fields, you can optionally change the read-only setting. For more information, see [Configure pop-ups on read-only fields](https://www.servicenow.com/docs/access?context=c_ReferenceIcon&version=yokohama&pubname=yokohama-platform-administration&section=t_ConfigPopupsOnReadOnlyFields&ft:locale=en-US) . Click ![Dependency view icon](../image/alert-dependency-view-icon.png) to open the alert in dependency view.

</td></tr><tr><td>

Task

</td><td>

The corresponding task for the alert, such as an incident, change, or problem.

</td></tr><tr><td>

Metric Name

</td><td>

Unique name that describes which metric data is collected.

</td></tr><tr><td>

Description

</td><td>

A description of the alert.

</td></tr><tr><td>

Message key

</td><td>

Unique event identifier to identify multiple events that relate to the same alert. If this value is empty, it is generated from the **Source**, **Node**, **Type**, **Resource**, and **Metric Name** field values. Maximum length: 1024 characters.

</td></tr><tr><td>

Severity

</td><td>

The severity of the event. The value for this field is copied from the event unless the event closes the alert, in which case the previous severity is retained for reporting. -   **Critical**: Immediate action is required. The resource is either not functional or critical problems are imminent.
-   **Major**: Major functionality is severely impaired or performance has degraded.
-   **Minor**: Partial, non-critical loss of functionality or performance degradation occurred.
-   **Warning**: Attention is required, even though the resource is still functional.
-   **OK**: An alert is created. The resource is still functional.
-   **Clear**: No action is required. An alert is not created from this event. Existing alerts are closed.


</td></tr><tr><td>

State

</td><td>

The state of the alert. -   **Open**: The alert requires user action.
-   **Reopen**: The previously closed alert requires additional user action.
-   **Flapping**: After the alert has been closed, it receives a high frequency of identical events from the same source that causes many alert reopenings. User action is required.
-   **Closed**: The alert is closed and no further user action is required.


</td></tr><tr><td>

Acknowledged

</td><td>

Select **Acknowledged** to indicate that a user has acknowledged the alert.

</td></tr><tr><td>

Maintenance

</td><td>

A check box that shows whether the resource that is affected by the alert is in maintenance.

</td></tr><tr><td>

Updated

</td><td>

The most recent time that the alert information was updated.

</td></tr><tr><td>

Parent

</td><td>

-   If this field is blank, you can specify an alert number. The current alert becomes a secondary alert to this parent alert.
-   If an alert number is displayed, then the current alert is already a secondary alert to this current alert, which is the parent alert.


</td></tr><tr><td>

Feedback

</td><td>

This field appears in alert forms only if the alert being modified is a parent alert. Your response provides feedback about the accuracy and usefulness of the group. Possible values are:-   None - No value was selected.
-   No Feedback - There is no feedback for this alert.
-   Yes - The alert group is accurate and useful.
-   No - The alert group is not accurate and not useful.
**Note:** Currently, the feedback option is available but does not trigger further actions after being logged.

</td></tr><tr><td>

Knowledge article

</td><td>

The knowledge article associated with the alert, if any.

</td></tr><tr><td>

Overall Event Count

</td><td>

The counter is increased every time an event is bound to the alert. The count value is kept even after the actual event has been purged. Primary alerts \(virtual alerts\) are updated based on their secondary alerts. The actual number of events that affected the alert is displayed. **Note:** Do not create an Alert Group based on Event Count. Where an Alert Group is based on Event Count, the impact of the group does not calculate properly because the Event Count field is not copied to the em\_alert\_history table for impact calculation.

</td></tr><tr><td>

Source instance

</td><td>

The name of the machine or software that generated the event. For example, SolarWinds on 10.22.33.44.

</td></tr><tr><td>

User name and role

</td><td>

The user and role of the person who made the most recent alert updates.

</td></tr><tr><td>

Acknowledged

</td><td>

The **Acknowledged** check box value after the most alert recent update.-   **True**: The **Acknowledged** is selected.
-   **False**: The **Acknowledged** check box is cleared.


</td></tr><tr><td>

**Correlated Alerts** section

</td><td>

The secondary alerts that are correlated with this alert, where this alert is the primary alert. For more information, see [Rule-based alert grouping](../concept/c_EMEventCorrelationRules.md).

</td></tr><tr><td>

**Primary Alerts** section

</td><td>

The primary alert that is correlated with this alert, where this alert is a secondary alert. For more information, see [Rule-based alert grouping](../concept/c_EMEventCorrelationRules.md).

</td></tr></tbody>
</table>    Additional tabs.

    |Field|Description|
    |-----|-----------|
    |Impacted Services tab|
    |Impacted Services|The impacted services that are related to this alert are listed. For more information, see [View the impact tree](t_EMViewImpactTree.md).|
    |Flapping tab|
    |Flap count|The number of times the alert has flapped—that is, has fluctuated between a closed and a non-closed state—within the flap interval since the start time in the **Flap start window**.|
    |Flap start window|The initial start time to measure the flapping occurrences.|
    |Flap last update time|The last time flapping occurred. This time is the platform processing time, not the source system time.|
    |Flap last state|The state before the alert entered the flapping state.|
    |History tab|
    |Initial event generation time|The time when the event that generated the alert first occurred. This time is the platform processing time, not the source system time.|
    |Last event generation time|The last time the event that is linked to the alert occurred. This time is the platform processing time, not the source system time.|
    |Created|The time that the alert was created.|
    |Work notes|The additional notes about the alert.|
    |Activities tab|
    |Activity|A record of the work that was performed. The text has a date and time stamp.|
    |More Information tab|
    |Priority Breakdown|Displays the computation of the alert priority score.|
    |Additional information|A JSON string that gives more information about the event. The JSON data is supported for String values only, other value types are not supported. You must convert numbers to String values by enclosing them in double quotes. For example, this value is not supported: \{"CPU":100 \} while this value is supported: \{"CPU":"100"\}. Another example of a valid JSON string is: \{"evtComponent":"Microsoft-Windows-WindowsUpdateClient","evtMessage":"Installation Failure: Windows failed. Error 0x80070490"\}. This information can be used for third-party integration or other post-alert processing. Values in the **Additional information** field of an Event that are not in JSON key/value format are normalized to JSON key/value format when the event is processed. For example, assume that the following plain text is in the **Additional information** field “Connection instance is successful”. When the event is processed, all this plain text becomes one JSON string and might not be useful within an alert. In the resultant alert, this string is in the **Additional information** field in JSON key/value format, containing the data: \{“additional\_content”: “Connection instance is successful"\}.|


## What to do next

You can respond to the alert in the following ways:

|Option|Description|
|------|-----------|
|Submit|Save the modifications that were made to the form and return to the **Alerts** list.|
|Acknowledge the alert.|Click **Acknowledge**. If the alert is reopened, this button reappears so you can reacknowledge the alert.|
|Create an incident.|Click **Create incident**. For more information, see [Create an incident or security incident from an alert](t_EMCreateIncidentfromAlert.md).|
|If Security Incident Response is activated, create a security incident response.|Click **Create Security Incident**.|
|Designate that the alert is in maintenance.|Select the **Maintenance** check box. For more information, see [View all alerts by the maintenance status](t_EMViewAlertmaintenance.md).|
|Close the alert.|Click **Close**. For more information, see [Close an alert](t_EMCloseAlert.md).|

-   **[Priority group](../concept/alert-priority-group.md)**  
For better triage and focus, alerts that have a higher priority are brought to the top of the alert list. This placement brings to your attention those alerts that require you to handle them at a higher priority than other alerts.
-   **[Alert execution information](../concept/alert-execution.md)**  
Alert execution information provides a reference to the actions that have been performed concerning the alert. Among the information presented is which alert management rules ran on the alert, incidents that were opened, and which remediation workflows ran.
-   **[View alerts in the flapping state](t_EMViewAlertFlapping.md)**  
You can view alerts that are specifically in the flapping state.
-   **[View all alerts by the maintenance status](t_EMViewAlertmaintenance.md)**  
The **Maintenance** status indicates that the CI is under maintenance. For example, there is a software upgrade, and the issues can result from that activity, therefore all maintenance alerts are discarded.
-   **[Collaborate from within an alert](em-collaborate-from-alert.md)**  
You can collaborate with colleagues and write work notes while working in an alert.
-   **[Create an incident or security incident from an alert](t_EMCreateIncidentfromAlert.md)**  
When an alert must be escalated and assigned to someone who can resolve the underlying issue, you can open an incident.
-   **[Place an alert into maintenance](t_EMPutAnAlertIntoMaintenance.md)**  
You can manually place any alert into maintenance to hide it from the Alerts list and Agent Workspace.
-   **[Alert insight information](../concept/alert-insight-information.md)**  
Alert insight aids faster alert triage, enabling a quicker way to find a solution and expose the probable root cause of the selected alert.
-   **[Apply a quick response in an alert](apply-quick-response-in-alert.md)**  
In an alert, use the `Quick Response` feature to apply remediation to the alert or to launch a web application.

**Parent Topic:**[Using Event Management](../concept/user-guide.md)

**Related topics**  


[Security incidents created from events and alerts](https://www.servicenow.com/docs/access?context=c_ScIncdUseAlrts&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)

