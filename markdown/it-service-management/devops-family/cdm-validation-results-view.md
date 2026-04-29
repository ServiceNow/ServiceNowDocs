---
title: View the results of snapshot validation
description: View validation failures and warnings on the Validation results tab for the snapshot.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Validating and correcting configuration data, Using DevOps Config, DevOps Config, IT Service Management]
---

# View the results of snapshot validation

View validation failures and warnings on the **Validation results** tab for the snapshot.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: cdm\_viewer or cdm\_editor or cdm\_exporter\_editor or cdm\_policy\_editor or cdm\_admin

## Procedure

1.  On the **Snapshots** tab for an application, select the snapshot to open the **Validation results** tab.

2.  View failure and warning information on the **Validation results** tab for the snapshot.

    The **Policies** panel displays a card for each policy that is mapped to the associated deployable.

    ![Policies panel on the Validation results tab of the Snapshot form lists execution results.](../image/cdm-snapshot-policies-panel.png)

<table id="table_j2q_lj5_cqb"><thead><tr><th>

Card label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All Policies

</td><td>

The card displays the total number of failures and warnings for this validation run.

</td></tr><tr><td>

Name of the mapped policy

</td><td>

Each policy that has been executed for the deployable and its execution results with whether the snapshot is compliant with the policy. It also displays the following data:-   Failures: Number of failures in the current execution.
-   Warnings: Number of warnings in the current execution.
-   Dynamic mapping: Value is **true** if the policy is dynamically mapped, or else **false**.


</td></tr></tbody>
</table>    -   Select a card from the **Policies** panel to view the associated data in the **Failures and warnings** panel.
    -   Select the more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for a policy and select an action, as follows:

<table id="table_nbn_hwk_gqb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution record

</td><td>

View execution information for this policy run. See [View the execution record for a policy run](cdm-execution-record-policy-view.md) for details.

</td></tr><tr><td>

Open policy

</td><td>

Open the policy.

</td></tr><tr><td>

Open business condition

</td><td>

Opens the condition set on the CDM Deployable \[sn\_cdm\_deployable\] table based on which the policy was dynamically mapped to the deployable and executed.**Note:** This menu option is available only for the dynamically mapped policy.

For more information on conditions and dynamic mapping, see [Map PaCE policies using Dynamic Mapping](https://www.servicenow.com/docs/access?context=pace-validate-dynamic&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>    The **Failures and warnings** panel displays the list of all failures and warnings for the policy that is mapped to the associated deployable.

<table id="table_bjb_zvk_gqb"><thead><tr><th>

Column header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Text that provides information about the failure or warning result.

</td></tr><tr><td>

Type

</td><td>

Type of validation result:-   \(Empty\)
-   Information
-   Failure
-   Warning


</td></tr><tr><td>

Policy

</td><td>

Name of the policy that returned a failure or warning. Select to open the policy.

</td></tr><tr><td>

Impacted data

</td><td>

The CDI \(`name: value` pair\) that resulted in the failure or warning.

</td></tr><tr><td>

Path

</td><td>

Path to the node in the data tree that includes the impacted data.

</td></tr></tbody>
</table>
