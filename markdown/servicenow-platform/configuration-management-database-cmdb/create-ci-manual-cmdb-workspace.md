---
title: Create a CI manually in CMDB Workspace
description: Create a new CI in CMDB Workspace, while applying Identification and Reconciliation Engine \(IRE\) processes and other requirements for the CI's class. IRE identification rules enforce the new CI to be unique and to comply with other class requirements.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CI manually in CMDB Workspace

Create a new CI in CMDB Workspace, while applying Identification and Reconciliation Engine \(IRE\) processes and other requirements for the CI's class. IRE identification rules enforce the new CI to be unique and to comply with other class requirements.

## About this task

Creating specialty CIs such as an application service, isn't supported in this Create CI experience. Typically, such CIs aren't discoverable and you must create them manually using specific wizards, such as the [Application service wizard](../../service-mapping/task/create-it-services.md).

You can access the Create CI experience in either of the following ways:

-   Selecting the **Create CI** quick link on the Home view of CMDB Workspace which lets you then select a class for the new CI.
-   Drilling down a class group bar in the CI Summary tab on the CI overview tile, in which case the class you are drilling down from becomes the class for the new CI. This option is available only if you drill down a class that isn't excluded for the Create CI experience. For information about excluding classes for the Create CI experience in CMDB Workspace, see [Limit the class list for new CIs created in a workspace](limit-class-create-ci-workspace.md).

As you progress through the procedure, fields appear dynamically according to your selections and entries on the current or previous pages.

To manually create a new CI without applying IRE processes \(Core UI\), see [Populating the CMDB](../concept/c_OptionsToPopulateCMDB.md). For more information about mandatory attributes, IRE processes, dependent CIs, and the CI relationship editor \(Core UI\), see:

-   [Set a CI attribute to be mandatory](t_SetCIFieldMandatory.md)
-   [Identification rules](../concept/c_IdentificationRules.md)
-   [CMDB classifications and class dependency](../concept/c_CMDBClassifications.md)
-   [CI relationship editor](../concept/c_RelationshipEditor.md)

## Before you begin

Configure any customizations to the create CI experience before creating new CIs:

-   Complete any request by an administrator for additional non-mandatory attributes. For information about how an administrator can use configuration identifiers to incorporate requests for attributes into the flow of creating a new CI, see [Request additional attributes for new CIs](additional-att-create-ci-workspace.md#).
-   Complete any settings for limiting the list of classes available to choose from, for a new CI. For information about how an administrator can use configuration identifiers to create a custom list of classes for a new CI, see [Limit the class list for new CIs created in a workspace](limit-class-create-ci-workspace.md).

If you want additional actions to be performed after creating a CI, such as creating a record that references the new CI, implement the ManualCreateCIExtPoint extension point:

-   In the getAppId\(\) function, add the sys\_id of the application containing the workspace from the UX Application \[sys\_ux\_page\_registry\] table.
-   In the postInsertCI\(\) function, define the additional actions you want to perform.

Your extension point implementation runs after a new CI is created in the application specified in getAppId\(\). You can create additional implementations as needed for additional applications. For more information about extension points, see [Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md).

Role required: cmdb\_manual\_ci\_ire\_access \(contained in the sn\_cmdb\_editor role by default\)

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  On the Home view of CMDB Workspace, use one of the following options:

    -   Select the **Create CI** quick link, and then:
        1.  On the **Select class** page, select the class for the new CI from the **Class** drop-down list. Classes without a valid identification rule are grayed out in the list and you can't select them.
        2.  Select **Continue**.
    -   On the CI overview tile, select the CI Summary tab, and then:
        1.  Select the group bar with the class that you want to create the new CI in.
        2.  Scroll down to the list view for the class group, and select the class in which you want to create the new CI.
        3.  On the class list view page, select the **Create CI** button.

            **Note:** If you selected a class that is excluded from the Create CI experience, the **New** button appears. Select **New** to manually create a new CI without applying IRE processes \(Core UI\).

    Continue to fill out the rest of the Create a new CI pages as described in the following steps.

3.  On the Home view of CMDB Workspace, select the **Create CI** quick link and then fill out all the Create a new CI pages as described in the following steps.

4.  **Select class**:

    Select the class for the new CI from the **Class** drop-down list. Classes without a valid identification rule are grayed out in the list and you can't select them.

    Select **Continue**.

5.  **Required attributes**:

    Configure attributes that are either mandatory for the new CI's class, or which the identification rule for the new CI's class requires. Also, if the new CI is a dependent CI, configure the dependency relationship.

    -   In the Dependent-upon CI section, select a CI that the new CI depends on.

        **Dependent-upon class**: Select the class of the dependent-upon CI.

        **Dependent-upon CI**: Select the search icon and in the Dependent-upon CI dialog box, select a CI by selecting its link in the Name column.

    -   In the Identifier entries section, select criterion attributes and set their values to uniquely identify the CI.

        **Criterion attributes**: In the drop-down list, select one or more criterion attributes sets. This drop-down list omits criterion attributes that are based on the **Product instance identifier** attribute.

    -   In the criterion attribute fields section scroll down the page if needed and enter values for the criterion attributes fields for the CI.

    Select **Continue**. If the new CI is detected as a duplicate of an existing CI, then the CI already exists dialog box appears. Select **Review existing CI** and then decide whether to change the existing or the new CI to prevent the duplication and to continue creating the CI.

6.  **Additional attributes**:

    Enter values for attributes, such as **Operational status**, that your administrator is requesting in addition to the required attributes from previous pages.

    Select **Continue**.

7.  **Relationship definition**:

    Review any existing relationships and decide whether to add a relationship for the new CI. For dependent CIs, a dependent relationship was already created in an earlier step.

    1.  Select **Add**.
    2.  On the Add relationships page, select a **Relationship type**.

        The Parent/Child notations in each relationship type denotes whether the new CI will have the role of a child or a parent in the new relationship.

    3.  In the Configuration Item list, select the CIs that the new CI will have the relationship with. Whichever parent/child role you selected for the new CI, the selected CIs will have the other role.
    4.  Select **Add**.
    **Note:** Creating relationships to the User and the Group tables is supported, however, those relationships aren't processed by IRE.

    On the Relationship definition page, select **Continue**.

8.  **Review**:

    Review all the details of the new CI. Select **Create** to approve and create the new CI, or **Back** to change definitions.

9.  In the New CI created dialog box, select **Done** to exit the operation, **Review new CI** to open the form view for the new CI, or **Create another CI**.


## Result

In the new CI:

-   **Discovery source** is set to **Manual via IRE**.
-   **Operational status** is set to **Design** until the new CI is fully configured and ready to be used. You can modify the CI's status, for example, to **Operational** if appropriate.

In the new CI, **Discovery source** is set to **Manual via IRE**.

## What to do next

You can view the new CI or other CIs, using CI Form in CMDB Workspace. For more information about using the CI Form, see [Manage CI details using CI Form in CMDB Workspace](../concept/ci-form-cmdb-workspace.md).

**Parent Topic:**[CMDB Workspace store app](../concept/cmdb-workspace.md)

