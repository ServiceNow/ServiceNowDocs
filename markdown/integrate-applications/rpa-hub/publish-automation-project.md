---
title: Publish an automation project in RPA Desktop Design Studio
description: Publish an automation project to RPA Hub from RPA Desktop Design Studio as a package or as a template. After publication, you can quickly deploy automation solutions in the RPA platforms by using the packages or by using a template as a framework to create automations.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Publish an automation project in RPA Desktop Design Studio

Publish an automation project to RPA Hub from RPA Desktop Design Studio as a package or as a template. After publication, you can quickly deploy automation solutions in the RPA platforms by using the packages or by using a template as a framework to create automations.

## Before you begin

Ensure that the automation project file is open in RPA Desktop Design Studio. For more information, see [Open a local automation project in RPA Desktop Design Studio](open-project-rpa-studio.md).

Ensure that the automation project file is in a separate folder. All the files and folders in the current project file location are published to the RPA Hub.

Verify the connection manager setup in the RPA Desktop Design Studio. For more information, see [Set up RPA Desktop Design Studio](set-up-rpa-studio.md).

Role required: sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin

## About this task

Publishing an automation project as a package enables the RPA Hub to execute a process job that executes the workflow in the automation project. You can publish an automation project as a new package or as the version of an existing package.

Publishing an automation project as a template makes it the framework for creating automation projects later. You can publish an automation project as a new template or as the version of an existing template.

## Procedure

1.  In the RPA Desktop Design Studio, open the automation project that you want to publish.

2.  On the **Design** tab, select **Publish**.

    **Important:**

    -   If the Code quality check feature is enabled from your RPA Hub instance and your automation project has Code quality check issues, the Code Quality Check Results window displays an error message.

        ![Code quality check performed during publishing of a project.](../image/cqc-results.png)

        You can publish a package with errors or with both errors and warnings only if the property **sn\_rpa\_fdn.restrict\_package\_by\_severity** is set as **No restriction** in RPA Hub. For more information, see [Configure RPA Hub properties](../../rpa-hub/reference/rpahub-sys-properties.md). As shown in the following example, these packages are highlighted with the message `Automation contains one or more errors or warnings` when you begin to publish a project.

        ![Error displayed when you're publishing a project with errors or warnings.](../image/cqc-publish-error2.png "Error displayed when you're publishing a project with errors or warnings")

        For more information on the compliance rules that the Code quality check follows when a package is published from RPA Desktop Design Studio, see [Code quality check compliance for RPA Desktop Design Studio](../../rpa-hub/reference/cqc-publish-studio.md).

    -   When you enable the **sn\_rpa\_fdn.code\_signing\_required** system property on the instance, it impacts the existing bot processes that are associated with the packages on the same instance because you didn't enable code signing on them earlier while you were publishing from RPA Desktop Design Studio to RPA Hub. As a result, the automations that corresponded to these bot processes failed. To run the failed automation successfully, you must publish the package again with the code signing from RPA Desktop Design Studio to RPA Hub.
3.  Publish an automation project as a package or template.

<table><thead><tr><th align="left" id="d198893e251">

Option

</th><th align="left" id="d198893e254">

Action

</th></tr></thead><tbody><tr><td id="d198893e260">

**Publish the automation project as a package**

</td><td>

1.  In the Publish project window, ensure that **Package** is selected in the **Publish project as** field.

**Note:** **Package** is the default option.

2.  In the Publish package as list, select **New Package** or **New version \(to existing package\)**.
    -   Publish the automation project as a new package by ensuring that **New Package** is selected.

**Note:** **New Package** is the default selection.

    -   Publish the automation project as a version to an existing project by selecting **New version \(to existing package\)**.
3.  Publish the package as a new package by entering the package name in the **Name** field or by retaining the default name.

**Note:** By default, the automation project name is the default package name.

4.  Publish the package as a new version to an existing package by selecting the package name from the Select Package list.
5.  In the **Comments** field, enter a comment.
6.  Select **Publish**.
7.  Select **OK**.


</td></tr><tr><td id="d198893e342">

**Publish the automation project as a template**

</td><td>

1.  In the Publish project window, in the **Publish project as** field, select **Template**.
2.  In the Publish template as list, select **New template** or **New version \(to existing template\)**.
    -   Publish the automation project as a new template by selecting **New template**.
    -   Publish the automation project as a version to an existing template by selecting **New version \(to existing template\)**.
3.  Publish the automation project as a new template by entering the template name in the **Name** field or by retaining the default name.

**Note:** By default, the automation project name is the default template name.

4.  Publish the automation project as a version to an existing template by selecting **New Version \(to existing template\)**.
5.  Publish the template as a new version to an existing template by selecting the package name from the **Template** list.
6.  In the **Comments** field, enter a comment.
7.  Select **Publish**.
8.  Select **OK**.


</td></tr></tbody>
</table>4.  If code signing is mandated by your organization and you’re publishing the automation project as a package, do the following actions:

    1.  In the **Certificate location** field, select either **File** or **Cert Store** as the location of the certificate.

    2.  Select the three-dot menu \(![Three-dot menu.](../../rpa-runtime/image/rpa-runtime-run-three-dot-menu.png)\) next to the **Certificate** field.

    3.  Select the installed code signing certificate.

        **Note:** You can only select a certificate that has the intended purpose as code signing. If you select a certificate with any other intended purpose, an error is displayed.

    4.  Select **OK**.

    **Note:** This step is applicable only if you’re publishing the automation project as a package.


**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

