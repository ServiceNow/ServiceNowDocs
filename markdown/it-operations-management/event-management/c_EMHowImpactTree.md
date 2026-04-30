---
title: How alerts work with CIs in maintenance
description: When a CI is in maintenance, the impact tree, the service map, and Alerts tab are updated based on various factors.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# How alerts work with CIs in maintenance

When a CI is in maintenance, the impact tree, the service map, and Alerts tab are updated based on various factors.

Event Management Part 2 \| Impact TreeWatch this brief video to learn about how alerts work with CIs.

A CI is in maintenance when:

-   A change request is scheduled for the CI.
-   The **Install Status** field on the CI record is set to **In Maintenance**.

**Note:** To customize how alerts work with CIs in maintenance, see [Create maintenance rules](../task/create-maintenance-rule.md).

<table><thead><tr><th>

How CIs in Maintenance appear in Event Management

</th><th>

Description and the optimal time to resolve the alert

</th></tr></thead><tbody><tr><td>

![Event Management impact](../image/EMImpactTreeCR.png "CI with an active change request")

 If an active change request is scheduled for the CI or if the **Install Status** of the CI is **In Maintenance**, all alerts on the affected CI are excluded from impact calculation. The Alerts tab also temporarily hides all corresponding alerts. The impact tree shows the CI in green with a note of **\(In Maintenance\)**. The impact tree and the service map temporarily show CIs in green.

 For a service, all alerts on CIs in the service are also hidden from the Alerts tab. The entire service is shown in green on the impact tree. For a host with an active change request, the host applications are considered as one unit. All child applications are treated in the same manner as the host until the change request is no longer active.

</td><td>

An active change request has the following values: -   The **State** is **Scheduled** or **Implement**.
-   The current time is between the Planned start date and Planned end date on the change request.

OR

-   The current time is between the Actual start date and Actual end date on the change request.

 You can monitor the progress of the change request. Wait until the change request moves to the **Review** or **Closed** state. Then you can address all alerts for the affected CI and any alerts that generated between start and end dates. Use the impact tree, topology, and Alerts tab to show the calculated impact severity.

**Note:**

The [**Maintenance**](../task/t_EMViewAlertmaintenance.md) check box for an alert is selected when the **Install Status** field on the CI record is **In Maintenance**. This **Maintenance** check box indicates that the alert must be hidden from the **Alerts** tab.

</td></tr><tr><td>

![Event Management map](../image/EMImpactTreeNoCR.png "CI with no active change request and not in maintenance")

 When there is no active change request for a CI and when the CI is not in maintenance, impact calculation resumes. The impact tree, the service map, and Alerts tab show the calculated impact severity for alerts.

</td><td>

An inactive change request has the following values: -   The **State** is **New**, **Assess**, **Authorize**, **Review**, **Close**, or has no changes at all.
-   The **State** is **Scheduled** or **Implement**. However, the current time is before or after the planned or actual date ranges on the change request.

 You can monitor the progress of the change request. When a CI has an inactive change request, you can address the corresponding alerts as appropriate.

</td></tr><tr><td>

![Event Management impact](../image/EMImpactTreeCR.png "CI with no active change request and in maintenance")

 If no active change request is scheduled for the CI and if the **Install Status** of the CI is **In Maintenance**, all alerts on this CI are excluded from impact calculation. The impact tree shows the CI in green with a note of **\(In Maintenance\)**. The impact tree and the service map temporarily show CIs in green.

</td><td>

All alerts on a CI with an inactive change request and **In Maintenance** has no impact calculation.

</td></tr></tbody>
</table>**Parent Topic:**[Manage and monitor alerts](c_EMAlert.md)

**Related topics**  


[Create maintenance rules](../task/create-maintenance-rule.md)

