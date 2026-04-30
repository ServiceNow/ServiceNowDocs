---
title: Remediate a de-duplication task \(manual\)
description: Remediate a single de-duplication task by using the Duplicate CI Remediator wizard. Use the wizard to guide you through the duplicate CI reconciliation process or to apply a custom workflow.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Remediate a de-duplication task \(manual\)

Remediate a single de-duplication task by using the Duplicate CI Remediator wizard. Use the wizard to guide you through the duplicate CI reconciliation process or to apply a custom workflow.

## Before you begin

Review the following topics to familiarize yourself with important concepts of duplicate CI remediation:

-   [Duplicate CIs remediation](../concept/de-duplication-tasks.md) to learn about general duplicate CI remediation concepts, restrictions, and special cases such as remediations that involve a large number of duplicate CIs.
-   [Properties related to remediation of duplicate CIs](../reference/properties-duplicate-ci.md) for information about important properties that affect processes of duplicate CI remediation. Including the glide.duplicate\_ci\_remediator.dry\_run property that determines if the Duplicate CI Remediator actually updates the CMDB or not.

Role required: itil to read, itil\_admin or cmdb\_dedup\_admin to write

## About this task

Instead of using the build of the Duplicate CI Remediator on Core UI, you can use the De-duplication dashboard, and de-duplication templates and libraries, available in [CMDB Workspace](../concept/cmdb-workspace.md)and in the [Service Graph Workspace store app](../concept/sg-workspace.md). Using de-duplication capabilities in CMDB Workspaceor in Service Graph Workspace is especially useful for bulk remediation of de-duplication tasks. These capabilities let you pre-configure a de-duplication template with remediation settings, which can then be applied in a consistent manner to multiple de-duplication tasks. For more information, see [CI de-duplication experience in CMDB Workspace and in Service Graph Workspace](../concept/dedup-ci-exp-cmdb-workspace.md).

-   Duplicate CI Remediator provides a remediation option that is based on the AI engine of the Now Assist for CMDB De-duplication task resolution assistant skill. This skill suggests remediation options, which are based on the AI analysis of CMDB data. Use the Now Assist option to bypass all the tabs in the Duplicate CI Remediator where you manually enter those selections, and go directly to the final review to initiate the remediation
-   Instead of using the build of the Duplicate CI Remediator on Core UI, you can use the De-duplication dashboard, and de-duplication templates and libraries, available in [CMDB Workspace](../concept/cmdb-workspace.md)and in the [Service Graph Workspace store app](../concept/sg-workspace.md). Using de-duplication capabilities in CMDB Workspaceor in Service Graph Workspace is especially useful for bulk remediation of de-duplication tasks. These capabilities let you pre-configure a de-duplication template with remediation settings, which can then be applied in a consistent manner to multiple de-duplication tasks. For more information, see [CI de-duplication experience in CMDB Workspace and in Service Graph Workspace](../concept/dedup-ci-exp-cmdb-workspace.md).

&gt;&gt;&gt;&gt;&gt;&gt;&gt; Stashed changes

As you progress through the tabs of the Duplicate CI Remediator, CIs are not updated. All updates are applied only in the final step, after you click **Remediate**.

**Note:** Remediation behaves differently when remediation involves a large number of duplicate CIs or where the duplicates are serial numbers. For information about special cases in remediation, see [Duplicate CIs remediation](../concept/de-duplication-tasks.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **De-duplication Tasks**.

2.  Open the de-duplication task that you want to remediate.

3.  On the task form, select **Remediate**.

4.  In the Remediate dialog box, select either of the following options:

    -   **Use the Duplicate CI Remediator \(Recommended\)**: Use the wizard to consolidate duplicate CIs according to your configurations and settings. Follow the Duplicate CI Remediator tabs to configure the reconciliation.

        **Note:** This option is not available with non-CMDB tables.

    -   **Use a custom remediation workflow**: Use an existing CMDB remediation rule or select **Add New** to [create a new one](t_CreateCMDBRemediationRule.md).

        -   On the CMDB Remediation Rule form, set **Task type** to `Remediate Duplicate Task` and select **Active**.
        -   On the Workflow form, set **Table** to Remediate Duplicate Task \[reconcile\_duplicate\_task\] and **If condition matches** to `None`.
        -   Ensure that the associated workflow remediates duplicate CIs.
        In the Remediate dialog box, select **Next** to start the workflow and to exit the Duplicate CI Remediator. The Remediate Duplicate Task form appears, where you can update the **State** of the task.

    -   **Use the Duplicate CI Remediator \(Restricted Mode\)**: Appears only if the **glide.duplicate\_ci\_remediator.enable\_restricted\_mode** system property is set to **true**. You might need to use this option if remediation is blocked because loading the de-duplication task times out. This option might be relevant when there is a large number of related items associated with a de-duplication task, allowing remediation to continue with the limited features in a restricted mode. For more information about using this option to restrict the use of related items in de-duplication remediation and allow remediation to proceed, see [Using restricted mode within the Duplicate CI Remediator \[KB1542272\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB1542272).
5.  On the **Select Main CI** tab in the Duplicate CI Remediator:

    1.  Select the main CI for this reconciliation using either of the following lists of duplicate CIs. For any CI, you can click the **Name** link to display the CI's attributes, or click the **Related Items** link to display the number of related items.

        -   **Recommended**: A subset of the **All** list, containing only system recommended main CIs. System recommendations are based on checking the duplicate CIs for the following criteria:
            -   CI with most related items.
            -   CI with most relationships.
            -   Newest discovered CI.
            -   Newest updated CI.
            -   Oldest created CI.
            -   Previous main CI, if one was previously selected.
        -   **All**: All duplicate CIs for the de-duplication task.
        Either option lets you review a summary of the remediation settings before starting the remediation.

    2.  Select one of the following options to choose whether to consolidate any attribute values, relationships, or related items from any of the duplicate CIs into the main CI:

        -   **Remediate Manually**: Lets you specify which attribute values, relationships, and related items from duplicate CIs to consolidate into the main CI.
        -   **Use Main CI**: Retains main CI attribute values, merges relationships, and merges only the default related items.

            Skip to step number 7 as this selection skips all configurations other than choosing the action for the duplicate CIs on the **Determine Duplicate CI Actions** page.

6.  On the **Merge Attribute Values** tab review inconsistent values of each attribute. For each attribute, choose to retain the main CI's value, or choose a value from a duplicate CI for the main CI to be set with.

7.  Select **Next**.

    |Column|Description|
    |------|-----------|
    |Attribute|Attribute for which there are different values.|
    |Main CI Value|**Attribute** value in the main CI.|
    |Other Values|The number of unique **Attribute** values within the duplicate CIs.|

    To override the main CI attribute value with a duplicate CI value:

    1.  Click the **Other Values** link.

    2.  In the attribute dialog box, click **Unique Values** to display only unique attribute values, or **All** to display all attribute values including identical values.

    3.  Select a value for the main CI **Attribute** to be set with.

        You can click **Reset to Original** to undo the selection of a different attribute value for the main CI.

    4.  Click **Select**.

    **Note:** Attributes, such as system fields, discovery fields \(**discovery\_source**, **last\_discovered**, **first\_discovered**\), and read-only fields \(such as the asset field\) do not appear in the list.

8.  On the **Merge Relationships and Related Items** tab:

    1.  In the Merge Relationships section, select whether to merge all relationships from all duplicate CIs into the main CI. Click **View all relationships** to display all the relationships in which a duplicate CI is a parent or a child. You can click a **Parent** or a **Child** link to display more details. Orphan and duplicate relationships of duplicate CIs are deleted if you choose to merge relationships. For more information about the CMDB Health relationship KPI, see [CMDB Health KPIs and metrics](../reference/r_CMDBHealthMetrics.md).

    2.  In the Merge Related Items section use the list collector to select related items to be merged into the main CI. Click **View all related items** to display all related tables \(items\) and the count of references in each table to one of the duplicate CIs. You can click the links in **Main CI Related Items** and **Duplicate CIs Related Items** to display details about the related items.

        Related items in the list collector have the following format:![Details of related items in thee list collector.](../image/RelatedItemRemediator.png)

        -   By default, all items in the default related items list are selected to be merged.
        -   Related items \(tables\) that have no references to a duplicate CI are not listed, unless that table is included in the default related items list.
        -   Since asset related tables are part of the exclusion list, they are not available for merge.
        See [Manage default related items list](manage-related-items-list.md) for more information about configuring a default list of related items.

    3.  Click **Next**.

9.  On the **Determine Duplicate CI Actions** tab, choose one of the following actions to perform after completing the reconciliation. Then click **Next**.

    -   **Set attributes to custom values** \(recommended\): Retain all duplicate CIs. Mark the duplicate CIs as invalid by setting a specific **Attribute** to a specific **Value** for all duplicate CIs. For example, set **Operational Status** to `Retired` to retire the duplicate CIs.

        The **duplicate\_of** attribute of the duplicate CIs is automatically set to the appropriate main CI. Also, the duplicate CIs will not be added to any de-duplication task after this task is remediated. If the identification engine is not configured to [skip duplication](../concept/id-detect-dup-ci.md), ensure that identification inclusion rules are configured to exclude the duplicate CIs during identification. This configuration prevents new de-duplication tasks with the same duplicate CIs from being created after remediation.

        **Note:** Discovery fields, system fields, read only fields, and date fields are excluded from the attributes list.

    -   **Delete**: Delete all duplicate CIs \(only the main CI remains\).

        **Note:** Review [Roll back and delete recovery](https://www.servicenow.com/docs/access?context=rollback-delete-recovery&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for information about reverting the deletion of CIs and related records.

10. On the **Review and Confirm** tab:

    1.  Review the summary of the expected updates for this duplicate CIs reconciliation. Updates are based on your selections and therefore the summary includes only the details that are applicable. This summary can include details of the relationships and related items that will be merged to the main CI, the attribute values that the main CI will be set with, and the number of CIs that will be deleted. Click **Attributes**, **Relationships**, **Related Items**, or **Duplicate CI Actions** if applicable, to display further details such as changes to attribute values.

    2.  Click **Remediate** to complete the reconciliation according to your reconciliation settings.

        Once complete, the task **State** is set to **Closed Complete**.


## Result

The following relationships are deleted without being merged to the main CI:

-   Relationships in which the type, child, or parent field is empty.
-   Relationships for which merging to the main CI will result in cyclic relationships.
-   Relationship for which merging to the main CI will result in duplicate relationships.

## What to do next

The reconciliation process runs in the background and may take a while to complete. Upon completion, the system sends a confirmation notice to the remediator of the task. Meanwhile, you can:

-   **Review Identification Rules**: Review identification and inclusion rules and make any necessary updates to reduce CI duplication.
-   **Check Progress**: View the task activities that are logged as the remediation progresses.
-   **View Main CI**: View the main CI for this reconciliation process.

**Parent Topic:**[Duplicate CIs remediation](../concept/de-duplication-tasks.md)

