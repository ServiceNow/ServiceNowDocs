---
title: Restricted Caller Access for Localization Workspace
description: Give Localization Workspace access to your content by setting Restricted Caller Access privileges. Setting these privileges is required only when target tables or scripts are restricted.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Restricted Caller Access for Localization Workspace

Give Localization Workspace access to your content by setting Restricted Caller Access privileges. Setting these privileges is required only when target tables or scripts are restricted.

## Before you begin

Set your application scope to Global.

Role required: admin. The localization\_admin role can't complete this procedure.

## About this task

Localization Workspace uses artifact records in the \[sn\_lf\_config\] table to make content types available for translation. If your target resources have Caller Restriction set, you must configure Restricted Caller Access to allow access from Localization Workspace.

Each artifact record contains two resources that might have Caller Access set to Caller Restriction:

-   a target table where translatable content is stored
-   a Processor script which retrieves the translatable content

If you create a new \(or custom\) artifact but the target resource has Caller Restriction set, that artifact's content type is unavailable for selection in a Translation Request. Check whether Caller Restriction is set by querying the appropriate table, as follows.

|Resource|Location to check|
|--------|-----------------|
|Artifact's table|Navigate to **System Definition** &gt; **Tables**\[sys\_db\_object\] and search for your artifact table's name or label.|
|Artifact's processor script|Navigate to **System Definition** &gt; **Script Includes**\[sys\_script\_include\] and search for the script's name.|

In the list view of **Tables** or **Script Includes**:

The following procedure is needed only when the **Caller Access** column has a value of `Caller Restriction`.

![List view of the sys_db_object table, with an example target resource (To-do Content) displaying 'Caller Restriction' in the Caller Access column.](../image/lw-restricted-caller-access-dbo-table.png)

For further information see **Related Content** on this page.

## Procedure

1.  Set your application scope to Global, then navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access** \[sys\_restricted\_caller\_access\].

2.  In the list view of the **Restricted Caller Access Privileges** \[sys\_restricted\_caller\_access\] table, open **Show/hide filter** using the icon![](../../../use/using-lists/image/show-hide-filters.png).

3.  Add the following conditions to the filter:

    -   `Source Scope is Localization Workspace`
    -   `Target Scope is same as Application`
    -   `Status is Requested`
4.  Select **Run** to execute the query.![The list view of Restricted Caller Access Privileges table, displaying three rows having a Source Scope of Localization Workspace.](../image/lw-restricted-caller-access1.png)

5.  In the list of results, open any record by selecting the value in the first column \(by default the first column is Operation\).

6.  In the record's form, change the **Status** field from `Requested` to `Allowed`, then select **Update**.

    **Note:** Because most records are not in the Global application scope, you must select the link in the banner **To edit this record click here**.

    ![The form view of a Restricted Caller Access Privilege record. The current Status is Requested, but the option to change the Status to Allowed is highlighted.](../image/lw-restricted-caller-access2.png)

7.  Repeat this procedure so that all records in the list of results have a status of `Allowed`.


## What to do next

Continue with setup of Localization Workspace. See [Configuring Localization Workspace](../concept/configuring-localization-workspace.md).

**Parent Topic:**[Configuring Localization Workspace](../concept/configuring-localization-workspace.md)

**Related topics**  


[Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US)

[Artifact configurations](../../localization-framework/concept/framework-configuration.md)

[Restricted caller access privilege settings](https://www.servicenow.com/docs/access?context=restricted-caller-access-privilege&version=australia&pubname=australia-application-development&ft:locale=en-US)

