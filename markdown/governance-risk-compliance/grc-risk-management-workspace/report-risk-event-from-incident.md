---
title: Report a risk event from an incident
description: If risk event integration is configured, users can report risk events from any upstream application such as IT Incidents. This ability to report risk events saves the time of users and helps to prevent losses for organizations.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use Risk Events, Use, Risk Management, Governance, Risk, and Compliance]
---

# Report a risk event from an incident

If risk event integration is configured, users can report risk events from any upstream application such as IT Incidents. This ability to report risk events saves the time of users and helps to prevent losses for organizations.

## Before you begin

Role required: sn\_risk.user

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **All**.

2.  Open the incident for which you want to report a risk event.

3.  Select **Report Risk Event**.

    The availability of the **Report Risk Event** button on the incident record is determined by the filter conditions specified in the Risk Event Integration Configuration record. For more information, see [Configure risk event integration](configure-risk-event-integration.md).

4.  On the form, fill in the fields.

<table id="table_hwl_c3b_clb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the incident.

</td></tr><tr><td>

Date of discovery

</td><td>

The date the incident was created.

</td></tr><tr><td>

Entity

</td><td>

The entity to which the incident belongs.

</td></tr><tr><td>

Event type

</td><td>

Type of event. The choices are:-   Financial impact
-   Non financial impact


</td></tr><tr><td>

Currency

</td><td>

Currency in which the amount of loss is reported. This field appears if **Financial impact** is selected from **Event type**.

</td></tr><tr><td>

Expected Loss

</td><td>

Expected amount of monetary loss. This field appears if **Financial impact** is selected from **Event type**

</td></tr><tr><td>

Non Financial Impact

</td><td>

Impact of the incident. The choices are:-   Low
-   Medium
-   High


</td></tr><tr><td>

Description

</td><td>

A brief description of the incident.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

The risk event is created.

**Parent Topic:**[Use Risk Events](../concept/use-risk-events.md)

