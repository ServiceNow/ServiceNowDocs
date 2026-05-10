---
title: Create a de-duplication template
description: Create a de-duplication template that you can then run to apply pre-configured and consistent remediation to de-duplication tasks, in bulk. Organize your templates in libraries that make sense in your organization.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [CI de-duplication experience in a workspace, Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a de-duplication template

Create a de-duplication template that you can then run to apply pre-configured and consistent remediation to de-duplication tasks, in bulk. Organize your templates in libraries that make sense in your organization.

## Before you begin

Role required:

-   To access the [Management view in CMDB Workspace](../concept/cmdb-workspace-mangmnt-view.md) to perform de-duplication tasks, sn\_cmdb\_admin
-   To access the [Governance view in Service Graph Workspace](../concept/sg-workspace-governance-view.md) to perform de-duplication tasks: sn\_cmdb\_editor or sn\_cmdb\_admin
-   To perform this task: cmdb\_dedup\_admin or any role containing cmdb\_dedup\_admin \(such as sn\_cmdb\_admin\)

## About this task

By default, a newly created template is in draft mode. Therefor, after creating a template, you must publish the template to make it available for remediation.

## Procedure

1.  Navigate to either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Management** in the CMDB Workspace menu bar.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and then select the Governance icon in the navigation panel.
2.  Select the **De-duplication Template Library** link in Management tools, in the Manage section.

3.  Create a library for the new template.

    1.  On the De-duplication templates page, select **Create a library**.

    2.  In the Create new library dialog box, fill out the **Name** and the **Description** for the new library.

    3.  Select **Create**.

4.  On the De-duplication templates page, select **Create a template**.

    On the New template page, configure the different sections of the template by completing the rest of the steps.

5.  **General information**: Fill out the form and then select **Next**.

<table id="table_iqk_z4g_yyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the template.

</td></tr><tr><td>

Class

</td><td>

CMDB class that this template can be applied to.

</td></tr><tr><td>

Template library

</td><td>

Library that the de-duplication template belongs to. Select a library, or select the '+' icon to create a new library.

</td></tr></tbody>
</table><table id="table_lt5_nfr_yyb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automatically select all de-duplication tasks that match the selected class

</td><td>

Assign all de-duplication tasks that match the template class, to the template for remediation.

</td></tr><tr><td>

Add all child classes

</td><td>

Also assign all de-duplication tasks that match descending classes of the template class, to the template for remediation.

 This option is available only if the **Automatically select all de-duplication tasks that match the selected class** option is selected.

</td></tr></tbody>
</table>6.  **Create condition**: Use a condition builder or a custom script to narrow down the list of de-duplication tasks assigned to the template, and then select **Next**.

    **Use script** toggle options:

    -   Off: Specify conditions to filter on CIs from the template class. Only the de-duplication tasks containing CIs that match the filter will be assigned to the template.

    -   On: Enter a custom script that returns a valid array of de-duplication tasks sys\_ids \(from the Remediate Duplicate Task \[reconcile\_duplicate\_task\] table\), that are applicable to the template class. Those de-duplication tasks will then be assigned to the template.

        **Note:** Ensure that the script runtime doesn't exceed your intended runtime expectation and doesn't unexpectedly affect performance. Invalid values returned by the script are ignored.

7.  **Select main CI**: Select the method for choosing the main CI from the drop-down list and then select **Next**.

    |Option|Description|
    |------|-----------|
    |**Newest updated**|Most recently updated CI.|
    |**Most related items**|CI with most related items.|
    |**Oldest created**|Oldest CI.|
    |**Most relationships**|CI with most relationships.|
    |**Discovery source**|A duplicate CI must be associated with the selected discovery source to become the main CI.|
    |**Has asset**|A CI must have an asset to become the main CI.|
    |**Select main CI based on condition**|A duplicate CI must match a specified condition to become the main CI.|

    **Note:**

    -   Applying the chosen method to a set of duplicate CIs must result in exactly one CI. If during remediation, the chosen method yields no CIs or multiple CIs, then the **Newest updated** method is automatically applied regardless of your choice.
    -   After selecting the main CI out of the set of duplicate CIs, the main CI is separate from the rest of the duplicate CIs. From that point, 'duplicate CIs' refers to all of the initial duplicate CIs, aside from the selected main CI.
8.  **Merge attributes**: Configure merging attributes from duplicate CIs into the main CI, and then select **Next**.

    1.  Select the method to use for merging the attributes of duplicate CIs into the corresponding attributes of the main CI.

        For each method card on the left \(such as Use latest updated CI\), select attributes in the list on the right, that should be merged into the main CI using that method.

    2.  Select options as appropriate.

<table id="table_w1m_1hr_yyb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow null value updates from duplicate CIs to main CI

</td><td>

When merging duplicate CIs into the main CI, lets a null value from a duplicate CI to overwrite a non-null value in main CI.

</td></tr><tr><td>

Allow updates from duplicate CIs only when the main CI value is null

</td><td>

When merging duplicate CIs into the main CI:-   Prevents updates to main CI attributes that have non-null value.
-   Allows updates to main CI attributes that have a null value, with a non-null value.


</td></tr></tbody>
</table>9.  **Merge relationships**: Select an option for merging relationships from duplicate CIs into the main CI, and then select **Next**.

    |Choice|Description|
    |------|-----------|
    |**Merge all relationships**|Merge relationships from all duplicate CIs into the main CI.|
    |**Do not merge any relationships**|Don't merge any relationships from duplicate CIs into the main CI.|
    |**Merge relationships based on condition**|Merge relationships only if the main CI satisfies this condition.|

10. **Merge related items**: Select the method to use for merging related items associated with the duplicate CIs into the main CI, and then select **Next**.

<table id="choicetable_azk_5gj_yyb"><thead><tr><th align="left" id="d146478e580">

Choice

</th><th align="left" id="d146478e583">

Description

</th></tr></thead><tbody><tr><td id="d146478e589">

**Merge default related items**

</td><td>

Merge only related items in the default related items list, from duplicate CIs into the main CI.

</td></tr><tr><td id="d146478e598">

**Do not merge any related items**

</td><td>

Don't merge related items from any duplicate CI into the main CI.

</td></tr><tr><td id="d146478e607">

**Merge all available related items**

</td><td>

Merge all related items from all duplicate CIs into the main CI.

</td></tr><tr><td id="d146478e616">

**Merge related items based on condition**

</td><td>

Merge related items only if the main CI satisfies this condition. Related items are merged individually based on the main CI satisfying their respective condition. If there are two related items with two conditions and the main CI satisfies only one condition, then only one related item is merged.

 Select **Create a new condition** to build conditions.

</td></tr></tbody>
</table>    -   For information about the default list of related items used in de-duplication processes, see [Manage default related items list](manage-related-items-list.md).
    -   For information about setting related tables so that automated workflows that might be blocking remediation of related items \(such as business rules and errors\), are disabled, see [Turn off workflows of related tables during remediation](dedup-ci-disable-workflow.md).
11. **Duplicate CI actions**: Select what to do with the duplicate CIs after they’re merged into the main CI, according to the template settings, then select **Next**.

    |Choice|Description|
    |------|-----------|
    |**Delete**|Permanently delete all duplicate CIs in the set \(main CI remains the only active CI\).|
    |**Set attributes to custom values**|Set attributes of duplicate CIs to custom values. Configure the pairs of attribute/value with your custom settings.|

12. **Review and test**: Access the following tabs to complete the template by reviewing and testing it.

    1.  **Summary**: Review all template settings and select **Back** to modify any settings.

    2.  **Test**: Select a sample de-duplication task and then select **Save and Preview Results** to save and run the template.

    3.  Preview the results of the remediation test.

    4.  Select **Save &amp; Exit** to save the template and return to the De-duplication templates home page.


## Result

The new template is added to the specified library in draft mode and can be edited. However, a template in draft mode isn't available for remediation of de-duplication tasks until you publish it.

## What to do next

-   [Publish a de-duplication template](workspc-dedup-unpublish-template.md)
-   [Run a template to process de-duplication tasks](workspc-dedup-run-template.md)
-   [Remediate a single de-duplication task](workspc-dedup-remediate-single-task.md)

**Parent Topic:**[CI de-duplication experience in CMDB Workspace and in Service Graph Workspace](../concept/dedup-ci-exp-cmdb-workspace.md)

