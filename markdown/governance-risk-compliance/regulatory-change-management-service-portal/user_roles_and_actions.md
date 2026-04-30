---
title: Types of alerts, user roles, and states of regulatory alerts
description: Different users perform various actions on the alert records based on the type of the alert.
locale: en-US
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Reference, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Types of alerts, user roles, and states of regulatory alerts

Different users perform various actions on the alert records based on the type of the alert.

You can view the following types of alerts under the Regulatory Alerts module:

-   All Assigned Alerts: Displays all assigned alerts in the instance where the **Coordinator** field is assigned to an appropriate user.
-   Unassigned Alerts: Displays the unassigned alerts in the instance where the **Coordinator** field is empty. Mark the Overall impact as No impact, Low, Medium, High, or Critical.
-   New Alerts: Displays new alerts in the instance where the **Coordinator** field is empty.
-   Deferred Alerts: Displays the deferred alerts where the **Coordinator** field is assigned to an appropriate user, the state is Deferred, and a reminder date is listed to perform the action post deferral.
-   Impact Assessment Alerts: Displays the alerts for regulatory events that are in Impact Assessment state.
-   In Progress Alerts: Displays the alerts that are in In Progress state.
-   Closed Alerts: Displays the alerts that are in Closed state.

The following table provides information on the user roles, the actions that these users can perform, and the description of these actions.

<table id="table_yqg_vnt_pnb"><thead><tr><th>

User roles

</th><th>

Actions

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="7">

-   sn\_grc\_reg\_change.manager
-   sn\_grc\_reg\_change.user
-   sn\_grc\_reg\_change.admin

</td><td>

Update

</td><td>

Updates the details of the alert.

</td></tr><tr><td>

Reassign

</td><td>

Reassigns the details of the alert.

</td></tr><tr><td>

Defer

</td><td>

Defers a regulatory alert to a future date.

</td></tr><tr><td>

Applicable

</td><td>

Marks the alert as applicable.

</td></tr><tr><td>

Initiate Impact Assessment

</td><td>

Initiates an impact assessment on the alert.

</td></tr><tr><td>

Not Applicable

</td><td>

Marks the alert as not applicable.

</td></tr><tr><td>

Cancel

</td><td>

Cancels the alert.

</td></tr></tbody>
</table>Managers can view all alerts. Users with the sn\_grc\_reg\_change.user role can view assigned alerts that are assigned to them, but they cannot view unassigned alerts or alerts that are assigned to other people.

See the following table for information on the states of regulatory alerts.

|State|Description|
|-----|-----------|
|New|Each incoming regulatory alert is by default assigned to a new state. Only the sn\_grc\_reg\_change.admin or the sn\_grc\_reg\_change.manager can assign an alert record.|
|Deferred|Some alerts do not require an immediate action and therefore, they are in the Deferred state and they are assigned to a later date.|
|Impact Assessment|The alert records that are of type regulatory event are assessed for applicability and are marked for an impact assessment. After an impact assessment, the alerts are marked as applicable or not applicable.|
|In Progress|Alerts with the In Progress state are being worked on. An sn\_grc\_reg\_change.user is assigned to each alert.|
|Closed|Alerts that are not relevant to an organization are in the Closed state. Alerts that have associated tasks that have been completed are also in the Closed state.|
|Cancelled|Alerts that are in Cancelled state.|

**Note:** The attributes on the alert record are part of the metadata that is given by the third-party regulatory intelligence provider. These attributes help in determining the applicability of the alert to the organization. These records are non-editable in the Regulatory Change Management application.

**Parent Topic:**[Regulatory Change Management reference](rcm-reference.md)

