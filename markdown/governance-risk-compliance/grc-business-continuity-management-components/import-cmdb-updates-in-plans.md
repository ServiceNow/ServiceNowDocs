---
title: Scheduling auto-update of related assets
description: You can schedule an auto-update of the related assets in the plans based on the source data and relationships in the CMDB. You can receive an email notification with details of the plan dependency updates from the BCM application. Dependencies are fetched from different sources such as BIA upstream dependency, BIA downstream dependencies, and CMDB.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Scheduling auto-update of related assets

You can schedule an auto-update of the related assets in the plans based on the source data and relationships in the CMDB. You can receive an email notification with details of the plan dependency updates from the BCM application. Dependencies are fetched from different sources such as BIA upstream dependency, BIA downstream dependencies, and CMDB.

## Scheduling an auto-update of the related assets

The BCM administrators can schedule an auto-update of the related assets in the plans in the Planning dependency update configuration module, based on the source data and relationships in the CMDB. You can access the auto-update configuration module by navigating to **Business Continuity Workspace** &gt; **General Administration** &gt; **Planning dependency update configuration**.

The Planning dependency update configuration module is shown in the following example.![Updating the BCP dependencies.](../image/plan-dep-update-config.png)

When the BCM administrators select the **Auto-update dependencies** option, the BCM application schedules an auto-update of the related assets in the plans. Similarly, when the **Send notification** option is selected, the BCM application sends automated emails to the plan owners about the dependency updates.

Planning dependencies are fetched from different sources such as BIA upstream dependency, BIA downstream dependencies, and CMDB.

**Note:** In the plans, the dependencies are fetched for all primary scope assets.

Setting up the Planning dependency update configuration module is a one-time activity. Once the sources are configured in the Planning dependency update configuration module, the updates are synchronized in the plan.

For more information on setting up the Planning dependency update configuration module, see [Configuring planning dependency updates](confi-planning-dep-updates.md).

## Using the updated dependencies with the Xanadu release

Beginning with the Xanadu release, you can use the updated dependencies from the latest BIA record to conduct a dependency assessment on an asset. Information from the columns labeled Related item BIA, Related item Recovery Time Objective \(RTO\), Related item Recovery Point Objective \(RPO\), and Related item Recovery Tier is used to ascertain the required recovery timeframe and data backup needs, which are then displayed in the Required Recovery Timeframe and Required Data Backup columns of the BIA record.

For more information on the source BIA records option in the Dependency configuration modules, see [Set up Planning dependency update configuration](../task/conf-plan-dep-update-confi-module.md).

**Note:** The filter condition in the Element definition is used to add specific configuration items \(CIs\) via the pop-up. The **Update dependencies** UI action also considers the element definition's filter and retrieves the related CIs of the configuration item listed in the **Applies to** field of the BIA. These relationships are retrieved from the CI Relationships table.

## Roles associated with the auto-update of the related assets in the plans

Users with the following roles typically update the related assets in the plans:

-   The BCM program managers, BCM planners, and BCM managers can update the related assets in the plans​.
-   BCM administrators can configure the Planning dependency update configuration module.

## Using the scheduled job to auto-update the dependencies

The **Update BCP dependencies snapshot** scheduled job is shipped as part of the base system. It runs at regular intervals and fetches the updated related assets in the plans. The scheduled job is shown in the following example.

![BCP scheduled job.](../image/bcp-scheduled-job.png)

The scheduled job is not marked as Active by default. To run the scheduled job at regular intervals, the system administrators can select the **Active** option and select **Execute now** to set up a schedule. The scheduled job then runs at regular intervals, scans the plan records for the changes, and fetches the updated related assets for the planning records. It creates a snapshot record for each planning record update.

The scheduled job processes a workflow to check for the changes in the relationships and save the dependency updates automatically as shown in the following example.

![Workflow for the scheduled job.](../image/workflow-for-sche-job-bia-plan.png)

1.  The scheduled job runs weekly, checks the related assets configuration for each planning record, and fetches the related assets from the sources defined in the **Sources** tab of the Planning dependency update configuration module.
2.  The scheduled job refers to the filter condition that is set in the configuration \(Planning dependency update configuration module\). If the condition matches the planning record, the scheduled job fetches and stores the related assets for the plan in the snapshot record, according to the sources defined in the configuration. If the filter condition does not match the planning record, the application skips the record.
3.  When the **Send notification** option is set to **True** in the Planning dependency update configuration module, the users of the planning record set in the configuration are notified about the updated related assets through the scheduled job.
4.  When the **Auto-update dependencies** option is set to **True** in the Planning dependency update configuration module, the scheduled job automatically applies the Plan dependency snapshot to the planning record.
5.  As the final step, the scheduled job updates the planning record according to the fields to be updated in the configuration.

## Updating the dependencies manually

As the BCM application user, you can update the plan dependencies instantaneously by using the **Update dependencies** UI action. In this way, you can update the dependencies manually before the scheduled job runs as per the weekly schedule. The dependencies are then updated in the sources and a snapshot record of the planning record update is created.

See the following workflow for using the **Update dependencies** UI action and updating the planning dependencies manually:

![Workflow for updating the dependencies manually.](../image/bia-plan-update-dependencies.png)

1.  The BCM planner navigates to the planning record. The application fetches the dependencies of the primary scope assets defined in the plan.
2.  The BCM planner selects the **Update dependencies** UI action.
3.  If the snapshot record exists for the update, the BCM planner applies the planning dependencies through the snapshot and updates the plan according to the **Fields to be updated** in the configuration. The plan workflow then continues for the next steps such as requesting review and approval.

    If the snapshot record does not exist for the update, the BCM planner checks if the planning record matches any configuration filter:

    -   If the planning record matches any configuration filter, the application gets the dependencies in real time according to the sources in the configuration. Then, the BCM planner updates the planning record according to the **Fields to be updated** in the configuration. The plan workflow then continues for the next steps.
    -   If the planning record does not match the configuration filter, the plan workflow then continues for the next steps.

For more information on updating the planning dependencies manually, see [Update the planning dependencies](../task/import-cmdb-updates-in-bcp.md).

**Note:**

**Note:** The Planning dependency update configuration module is used for using the scheduled job and for updating the planning dependencies manually \(by using the **Update dependencies** UI action\).​

## Snapshot record of the plan

When the scheduled job runs at set intervals, it creates a snapshot record of each plan update in the application. The snapshot record contains the delta of the changes in the configuration such as new, updated, and deleted assets for the plan. The snapshot records are listed in the Pending updates module in the Planning list view in the Business Continuity Workspace. A snapshot record is shown in the following example.

![BCP snapshot record.](../image/bcp-snapshot-record.png)

When a snapshot record gets created, the application displays a UI message to inform the users about the planning dependency updates. The BCM application stores one active snapshot for a plan at a time. The snapshots that are in the **Completed** state and that have not been updated in six months are removed from the application automatically.

If the planning record does not have any changes in the dependencies, then a snapshot record is not created for that planning record.

## Data Relationships Framework

When you create a business continuity plan, you must update the related assets in the plans. Beginning with the Xanadu release, the Data Relationships Framework \(com.sn\_app\_grc\_relationship\_config\) application supports the BCM application with the underlying framework to fetch the related assets in the plans. The Data Relationships Framework application is installed with the BCM application by default.

For more information on the Data Relationships Framework, see [Data Relationships Framework](../../grc-common/concept/data-relationship-framework.md).

-   **[Update the planning dependencies](../task/import-cmdb-updates-in-bcp.md)**  
Update the plan dependencies manually from the snapshot if the scheduled job is not activated in the Planning dependency update configuration module. You can update the dependencies in an active plan.

**Parent Topic:**[Structured workflows for BCPs](bcp-tasks-performed-by-bcp-owner.md)

