---
title: Scheduling auto-update of dependencies
description: You can schedule an auto-update of the dependencies in the business impact analysis based on the source data and relationships in the CMDB. You can receive an email notification with details of the BIA dependency updates from the BCM application.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Scheduling auto-update of dependencies

You can schedule an auto-update of the dependencies in the business impact analysis based on the source data and relationships in the CMDB. You can receive an email notification with details of the BIA dependency updates from the BCM application.

## Scheduling an auto-update of the dependencies

The BCM administrators can schedule an auto-update of the BIA dependencies in the Impact analysis dependency update configuration module, based on the source data and relationships in the CMDB. You can access the auto-update configuration module by navigating to **Business Continuity Workspace** &gt; **General Administration** &gt; **Impact analysis dependency update configuration**.

The Impact analysis dependency update configuration module is shown in the following example.

![Updating the BIA dependencies.](../image/impact-ana-dep-update-config.png)

When the BCM administrators select the **Auto-update dependencies** option, the BCM application schedules an auto-update of the dependencies in the BIAs. Similarly, when the **Send notification** option is selected, the BCM application sends automated emails to the BIA owners about the dependency updates.

The source for the BIA dependencies is CMDB.

**Note:** The dependencies are fetched for the BIA that is listed in the **Applies to** field of the BIA record such as HR Application BIA, Accounts Receivable BIA.

Setting up the Impact analysis dependency update configuration module is a one-time activity. Once the sources are configured in the Impact analysis dependency update configuration module, the dependency updates are synchronized in the BIA.

For more information on setting up the Impact analysis dependency update configuration module, see [Configuring impact analysis dependency updates](imp-ana-dep-update-config-module.md).

## Using the updated dependencies with the Xanadu release

Beginning with the Xanadu release, you can use the updated dependencies from the latest BIA record to conduct a dependency assessment on an asset. Information from the columns labeled Related item BIA, Related item Recovery Time Objective \(RTO\), Related item Recovery Point Objective \(RPO\), and Related item Recovery Tier is used to ascertain the required recovery timeframe and data backup needs, which are then displayed in the Required Recovery Timeframe and Required Data Backup columns of the BIA record.

For more information on the source BIA records option in the Dependency configuration modules, see [Set up Planning dependency update configuration](../task/conf-plan-dep-update-confi-module.md).

## Using the scheduled job to auto-update the dependencies

The **Update BIA dependencies snapshot** scheduled job is shipped as part of the base system. It runs at regular intervals and fetches the dependency updates. The scheduled job is shown in the following example.

![Scheduled job.](../image/bia-scheduled-job.png)

The scheduled job is not marked as Active by default. To run the scheduled job at regular intervals, the system administrators can select the **Active** option and select **Execute now** to set up a schedule. The scheduled job then runs at regular intervals, scans the BIA records for the changes, and fetches the dependency updates for the updated BIA records. It creates a snapshot record for each BIA update.

The scheduled job processes a workflow to check for the changes in the relationships and save the dependency updates automatically as shown in the following example.

![Workflow for the scheduled job.](../image/workflow-for-sche-job-bia-plan.png)

1.  The scheduled job runs weekly, checks the dependency configuration for each BIA record, and fetches the BIA dependencies from CMDB as defined in the **Sources** tab of the Impact analysis dependency update configuration module. It generates a list of all active BIAs and the primary and dependent assets of each BIA. If any new dependencies are added, updated, or deleted for a BIA, the scheduled job creates a snapshot record for the BIA that displays the changes for the user.

    **Note:** By default, the scheduled job checks all the BIA records that are not in the **Archived** state for any updated dependencies.

2.  The scheduled job refers to the filter condition that is set in the configuration \(Impact analysis dependency update configuration module\). If the condition matches the BIA record, the scheduled job fetches and stores the dependencies for the BIA in the snapshot record, according to the sources defined in the configuration. If the filter condition does not match the BIA record, the application skips the record.
3.  The application combines the assets list into a single list that is based on the priority defined in the Impact analysis dependency update configuration module. The application compares the asset list with the existing asset list and assigns either the **Added**, **Updated**, or **Deleted** state to each asset.
4.  The application also compares the new assets to the assets listed in the Element definition and verifies the element definition condition. The application creates a snapshot of the asset and auto-completes the dependency updates in the Dependency snapshot record.
5.  When the **Send notification** option is set to **True** in the Impact analysis dependency update configuration module, the users of the BIA record set in the configuration are notified about the dependency updates through the scheduled job.
6.  When the **Auto-update dependencies** option is set to **True** in the Impact analysis dependency update configuration module, the scheduled job automatically applies the dependencies snapshot to the BIA record.
7.  As the final step, the scheduled job updates the BIA record according to the fields to be updated in the configuration.

## Updating the dependencies manually

As the BCM application user, you can update the BIA dependencies instantaneously by using the **Update dependencies** UI action. In this way, you can update the dependencies manually before the scheduled job runs as per the weekly schedule. The **Update dependencies** UI action is listed in the Dependency assessment of the BIA. The dependencies are then updated in the sources and a snapshot record of the BIA update is created.

See the following workflow for using the **Update dependencies** UI action and updating the dependencies manually:

![Workflow for updating the dependencies manually.](../image/bia-plan-update-dependencies.png)

1.  The BCM planner navigates to a BIA record. The application fetches the dependencies of the asset defined in the **Applies to** field of the BIA.
2.  The BCM planner selects the **Update dependencies** UI action that is listed in the Dependency assessment of the BIA.
3.  If the snapshot record exists for the BIA update, the system applies the dependencies through the snapshot and updates the BIA according to the **Fields to be updated** in the configuration. The BIA workflow then continues for the next steps such as requesting review and approval.

    If the snapshot record does not exist for the BIA update, the BCM planner checks if the BIA record matches any configuration filter:

    -   If the BIA record matches any configuration filter, the application gets the dependencies in real time according to the sources in the configuration. Then, update the BIA record according to the **Fields to be updated** in the configuration. The BIA workflow then continues for the next steps.
    -   If the BIA record does not match the configuration filter, the BIA workflow then continues for the next steps.

For more information on updating the dependencies manually, see [Update the BIA dependencies](../task/imp-analysis-dep-update-config.md).

**Note:**

**Note:** The Impact analysis dependency update configuration module is used for using the scheduled job and for updating the dependencies manually \(by using the **Update dependencies** UI action\).​

## Snapshot records of the BIA

A snapshot record is created for each BIA update either with the scheduled job or with the **Update dependencies** manual UI action. If any new dependencies are added, updated, or deleted for a BIA, the snapshot record displays the delta of the changes. The snapshot records are listed in the Pending updates module in the Business Impact Analysis list view of the Business Continuity Workspace. A snapshot record is shown in the following example.

![Snapshot record.](../image/snapshot-record.png)

When a snapshot record gets created, the application displays the following UI message in the Dependency assessment of the BIA to inform the users about the dependency updates: `The dependencies have been updated in the sources. To review and apply the changes, select here - <link>.` The UI message is shown in the following example.

![Snapshot UI message.](../image/bia-update-ui-message.png)

The snapshot records are used for record keeping purposes. The BCM application stores one active snapshot for each BIA at a time. Whenever the dependencies are updated, a snapshot is always created first. As the system processes all the records one by one, the snapshot records are auto-committed one by one in the system.

The snapshots that are in the **Completed** state and that have not been updated for a few months are removed from the application automatically.

If the BIA record does not have any changes in the dependencies, then a snapshot record is not created for that BIA record.

## Roles associated with BIA dependency updates

Users with the following roles typically check for the dependency updates in a BIA:

-   The BCM program managers, BCM planners, and BCM managers can update the latest dependencies​.
-   BCM administrators can configure the Impact analysis dependency update configuration module.

A user who can update the dependency assessment can import the dependency updates for a BIA.

## Data Relationships Framework

When you perform a business impact analysis \(BIA\) on an asset, you must evaluate the dependencies of the BIA by performing a dependency assessment. If the dependencies in the CMDB are updated, importing them manually in a BIA can be a tedious activity. Beginning with the Xanadu release, the Data Relationships Framework application \(com.sn\_app\_grc\_relationship\_config\) supports the BCM application with the underlying framework to fetch the dependencies in the BIA. The Data Relationships Framework application is installed with the BCM application by default.

For more information on the Data Relationships Framework, see [Data Relationships Framework](../../grc-common/concept/data-relationship-framework.md).

-   **[Update the BIA dependencies](../task/imp-analysis-dep-update-config.md)**  
Update the business impact analysis \(BIA\) dependencies manually from the snapshot if the scheduled job is not activated in the Impact analysis dependency update configuration module. You can update the dependencies in an active BIA.

**Parent Topic:**[Structured workflows for BIAs](bia-tasks-performed-by-bia-owner.md)

