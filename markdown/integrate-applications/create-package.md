---
title: Create a package to assign to a bot process
description: Create an unattended or attended package in RPA Hub to assign it to a bot process to execute an automation.Use the Package Version form to view the code quality result.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Package and package version, Use, RPA Hub, Workflow Data Fabric]
---

# Create a package to assign to a bot process

Create an unattended or attended package in RPA Hub to assign it to a bot process to execute an automation.

## Before you begin

\(Optional\) Configure the system properties related to **Activity Stream**, to add or remove the fields. The changes to these fields are captured in the work notes. For more information, see [Configure the system properties for an activity stream in RPA Hub](configure-sys-properties-activity.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Packages**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the published package.

</td></tr><tr><td>

Package Type

</td><td>

Type of the package:-   **Unattended**: Unattended automation
-   **Attended**: Attended automation
-   **Skill**: Reusable automation
-   **Unattended Template**: Template for creating unattended automations in RPA Desktop Design Studio
-   **Attended Template**: Template for creating attended automations in RPA Desktop Design Studio


</td></tr><tr><td>

Application

</td><td>

\[Auto generated\] Application containing this record.Role required to view this field: admin.

</td></tr><tr><td>

Mark As Default

</td><td>

Option to enable this package as a default package for the current domain. Only one package can be selected as a default package for any domain.This field appears only when **Unattended Template** or **Attended Template** is selected from the Package Type field.

Roles required to edit this field: RPA admin.

</td></tr><tr><td>

Description

</td><td>

Description of the package.

</td></tr></tbody>
</table>6.  Select **Save**.

7.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


## Result

After a package is created, the RPA developer publishes an automation from RPA Desktop Design Studio. This process results in a new package version.

**Parent Topic:**[Package and package version in RPA Hub](../concept/package-version-rpa-hub.md)

**Related topics**  


[Retire a package in RPA Hub](retire-package.md)

[Download a package version in RPA Hub](download-package-version.md)

[View Audit History](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_HistorySets.md)

[Publish an automation project in RPA Desktop Design Studio](../../rpa-studio/task/publish-automation-project.md)

## Package Version form in RPA Hub

Use the Package Version form to view the code quality result.

<table id="table_ucf_k2x_2rb"><thead><tr><th>

Name of the rule

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Package

</td><td>

Associated package of the package version.

</td></tr><tr><td>

Version

</td><td>

Version number that identifies the set of components uploaded in a package

</td></tr><tr><td>

Application

</td><td>

Application that contains this record. This field is auto-generated.Role required to view this field: admin.

</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

Life-cycle stage statuses of a package version.

</td></tr><tr><td>

Active

</td><td>

Option to set this package version as active. The active version of the template is used when a template is selected for creating automation in RPA Desktop Design Studio. Only one package version can be set as active.

This field is applicable only for **Unattended Template** and **Attended Template** package types. For more information about package types, see [Create a package to assign to a bot process](create-package.md#).

Roles required to edit this field: RPA admin and RPA release manager.

</td></tr><tr><td>

Code Quality Result

</td><td>

Indicates if the **Code Quality Check** feature in RPA Desktop Design Studio has detected any errors, warnings, or information in the package.-   **Error** - If a package that is published from RPA Desktop Design Studio with the code quality check as error.

If a package has both error and warning, then the code quality check result is error.

If a package has both error and info, then the code quality check result is error.

-   **Warning** - If a package that is published from RPA Desktop Design Studio with the code quality check as warning.

If a package has both warning and info, then the code quality check result is warning.

-   **Pass** - If a package that is published from RPA Desktop Design Studio without any code quality check error or warning or info.

If the Code Quality Check feature is not enabled, then the value in this field is **Not Applicable**.

Code quality status of package versions are set with highest severity.

To review the error or warning, open the package version file in RPA Desktop Design Studio.

For more information about code quality check feature, see [Code quality check in RPA Hub](../concept/code-quality-check-rpa.md).

</td></tr><tr><td>

Comments

</td><td>

Brief description of the package version.

</td></tr></tbody>
</table>**Related topics**  


[View a package version in RPA Hub](view-package-version.md)

