---
title: Code quality check in RPA Desktop Design Studio
description: You can use code quality check in RPA Desktop Design Studio to proactively find the issues in an automation activity or the complete automation project. When you publish an automation project, an in-built code quality check is also performed. Code quality check enables you to reduce the number of errors and prevent potential issues that may hinder your automation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Code quality check in RPA Desktop Design Studio

You can use code quality check in RPA Desktop Design Studio to proactively find the issues in an automation activity or the complete automation project. When you publish an automation project, an in-built code quality check is also performed. Code quality check enables you to reduce the number of errors and prevent potential issues that may hinder your automation.

## Code quality check overview

Code quality check in RPA Desktop Design Studio is based on the pre-defined set of rules that are enabled from the RPA Hub instance. You must connect to the instance that has Code quality check to RPA Desktop Design Studio before you start using Code quality check. For more information on how to configure Code quality check from RPA Hub, see [Code quality check in RPA Hub](../../rpa-hub/concept/code-quality-check-rpa.md) RPA Desktop Design Studio. For more information on the pre-defined set of rules, see [Code quality rules list in RPA Hub](../../rpa-hub/reference/cqr-list-rpa.md).

When you check an activity or the complete automation project by using Code quality check, the issue results and details are displayed as a list of entries in the Code Quality Check Results window. The following example shows the window.

![Code Quality Check Results window where you can see the results of the check.](../image/cqc-results.png "Code Quality Check Results window")

You can double-click the result entries for components in the Code Quality Check Results window for the following scenarios:

-   If an affected component is in the current activity, it’s highlighted in the current activity.
-   If the affected component is in a different activity, you can navigate to the activity. The component gets highlighted. See the following example to see the component highlight in RPA Desktop Design Studio.

![Component highlighted in RPA Desktop Design Studio after the result entry is double-clicked from the Code Quality Check Results window.](../image/cqc-error-highlight.png "Component highlight in RPA Desktop Design Studio")

## Code quality check in publishing an automation project

Code quality check is automatically performed when you publish the automation project. If your project has code quality check issues, the Code Quality Check Results window is displayed with the result entries. For more information on how to publish an automation project, see [Publish an automation project in RPA Desktop Design Studio](../task/publish-automation-project.md) in RPA Desktop Design Studio.

**Note:** You can publish a package with errors or a combination of errors and warnings only if the property **sn\_rpa\_fdn.restrict\_package\_by\_severity** is set as **No restriction** in RPA Hub. For more information on this property, see [Configure RPA Hub properties](../../rpa-hub/reference/rpahub-sys-properties.md). For more information on the compliance rules that the Code Quality Check feature follows if a package is published from RPA Desktop Design Studio, see [Code quality check compliance for RPA Desktop Design Studio](../../rpa-hub/reference/cqc-publish-studio.md) in RPA Desktop Design Studio.

You can view the list of active and inactive rules from the View Rules window. You can filter the rules by their severity level from this window.

-   **[Fix automation issues with Code quality check in RPA Desktop Design Studio](../task/use-cqc-rpa-stduio.md)**  
Fix the automation issues in your automation activity or complete an automation project proactively by using the Code quality check feature in RPA Desktop Design Studio.

**Parent Topic:**[Using automations](rpa-studio-use.md)

