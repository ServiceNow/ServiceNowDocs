---
title: Package Version form in RPA Hub
description: Use the Package Version form to view the code quality result.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [RPA Hub reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Package Version form in RPA Hub

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

This field is applicable only for **Unattended Template** and **Attended Template** package types. For more information about package types, see [Create a package to assign to a bot process](../task/create-package.md).

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
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

**Related topics**  


[View a package version in RPA Hub](../task/view-package-version.md)

[Create a package to assign to a bot process](../task/create-package.md)

