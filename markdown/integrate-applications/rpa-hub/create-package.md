---
title: Create a package to assign to a bot process
description: Create an unattended or attended package in RPA Hub to assign it to a bot process to execute an automation.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Create a package to assign to a bot process

Create an unattended or attended package in RPA Hub to assign it to a bot process to execute an automation.

## Before you begin

\(Optional\) Configure the system properties related to **Activity Stream**, to add or remove the fields. The changes to these fields are captured in the work notes. For more information, see [Configure the system properties for an activity stream in RPA Hub](configure-sys-properties-activity.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, or sn\_rpa\_fdn.rpa\_admin

## About this task

A package refers to a set of workflows, scripts, configurations, and dependencies that are designed to automate specific tasks or processes. These packages can be published or imported onto the RPA platforms to quickly deploy automation solutions.

Packages are used to encapsulate functionalities, libraries, or applications, making it simpler for developers or RPA administrators to deploy software components.

You can create a package in two ways. Follow this procedure to create a package from RPA Hub.

To create a package from RPA Desktop Design Studio while you're publishing an automation file, follow the steps as mentioned in [Publish an automation project in RPA Desktop Design Studio](../../rpa-studio/task/publish-automation-project.md).

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

**Related topics**  


[Package Version form in RPA Hub](../reference/package-version-form-rpa.md)

[Retire an RPA Hub package](retire-package.md)

[Download a package version in RPA Hub](download-package-version.md)

[View Audit History](https://www.servicenow.com/docs/access?context=c_HistorySets&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

[Publish an automation project in RPA Desktop Design Studio](../../rpa-studio/task/publish-automation-project.md)

