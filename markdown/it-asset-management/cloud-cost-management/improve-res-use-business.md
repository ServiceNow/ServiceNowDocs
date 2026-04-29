---
title: Improve resource usage with Business hours
description: Improve resource usage and reduce your cloud spend by running resources during the specified business hours.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Improve resource usage with Business hours

Improve resource usage and reduce your cloud spend by running resources during the specified business hours.

Use the Business hours recommendation page to:

-   Manage Business hours processes.
-   [Configure Business hours operations](../task/bh-settings-config-cloudin.md) by selecting **Settings**.
-   [Define or update Business hours processes](../task/bh-policy-create-cloudin.md)

![Business hours recommendations in Cloud Cost Management Workspace.](../image/buis-hrs-rec-ws.png)

|Chart|Description|
|-----|-----------|
|Total potential savings by service category|Total savings to expect if all Business hours recommendations are applied by service category such as Compute and Database.|
|Total potential savings by change group|Total savings to expect if all Business hours recommendations are applied by change group such as Change Management and Application Development.|
|Business hr vs. Non-business hr spend|Spend for resources during business hours against non-business hours.|

<table id="table_uqn_1zb_wxb"><thead><tr><th>

Tab

</th><th>

Description

</th><th>

Available action on selected recommendations

</th></tr></thead><tbody><tr><td>

New

</td><td>

Resources that are candidates for applying Business hours processes.

</td><td>

Exclude

</td></tr><tr><td>

Scheduled

</td><td>

Resources that are tagged to have business hours enforced.

</td><td>

None

</td></tr><tr><td>

Declined

</td><td>

Resources for which owners \(or other approver\) didn’t want to enforce business hours \(rejected the change request\).

</td><td>

Exclude

</td></tr><tr><td>

Failed

</td><td>

Resources for which the attempt to enforce business hours failed.

</td><td>

Exclude

</td></tr><tr><td>

Report-only

</td><td>

Resources that match Report-only policies.

</td><td>

Exclude

</td></tr><tr><td>

Excluded

</td><td>

Resources that are configured not to be considered for business hours.**Important:** After an Unused resources job powers off a machine, the machine is added to the Excluded Resources list for Business Hours. This process ensures that the resource isn't started again in the future because it matches a Business hours policy. The exclusion reason on the Business hours **Excluded** tab indicates that the resource is an unused resource.

</td><td>

Remove from exclusion

</td></tr></tbody>
</table><table id="table_z3j_qjg_wxb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration item

</td><td>

Unique identifier of the resource.

</td></tr><tr><td>

Predicted monthly savings

</td><td>

Predicted savings if the Business hours recommendations are applied.

</td></tr><tr><td>

Provider

</td><td>

The provider that hosts the resource.

</td></tr><tr><td>

Service category

</td><td>

Lists all service categories from the instance sorted by name.

</td></tr><tr><td>

Cloud service

</td><td>

Lists all cloud categories sorted by  name.​

</td></tr><tr><td>

Policy

</td><td>

The Business hours policy that the resource matches to.

</td></tr><tr><td>

Policy type

</td><td>

Type of the Business hours policy that the resource matches to.

</td></tr><tr><td>

Change request

</td><td>

Change request that is associated with the recommendation.

</td></tr><tr><td>

Change Group

</td><td>

Change group for the resource.

</td></tr><tr><td>

Account

</td><td>

The service account that includes the resource. A service account represents a group of related regions in your provider account.

</td></tr><tr><td>

Region

</td><td>

If appropriate for the provider, region in the service account that hosts the resource.

</td></tr><tr><td>

Owned by

</td><td>

Owner of the resource.

</td></tr><tr><td>

Failure type

</td><td>

This column appears only for the Failed tab.Reason for which the change request wasn’t generated or the specified business hours weren’t applied to the resource.

</td></tr><tr><td>

Details

</td><td>

This column appears only for the Failed tab.Details of the failure type and the action that you must take to resolve the failure.

</td></tr></tbody>
</table>-   **[Configure Business hours operations](../task/bh-settings-config-cloudin.md)**  
You can choose to use or to disable Business Hours features and specify the amount of non-business hour spend that triggers notifications to users or groups. Controlling unnecessary resource use can help reduce costs.
-   **[Create Business hours schedule](../task/create-bh-schedule.md)**  
Create and apply a Business hours schedule to the cloud resources for enforcing the on/off schedule.
-   **[Define or update a Business hours policy](../task/bh-policy-create-cloudin.md)**  
A Business hours job applies policies to identify resources that are running when they should be powered off, reports them, and can start and stop them on a schedule that you specify. Running only during specified business hours can significantly reduce your cloud spend.

**Parent Topic:**[Using Cloud Cost Management](using-cloud-insights.md)

