---
title: Code quality check in RPA Hub
description: A code quality check refers to the process of evaluating the automation file or script to assess its adherence to coding standards, best practices, maintainability, and overall quality.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, RPA Hub, Workflow Data Fabric]
---

# Code quality check in RPA Hub

A code quality check refers to the process of evaluating the automation file or script to assess its adherence to coding standards, best practices, maintainability, and overall quality.

## Code quality check overview

Code quality checks are essential in RPA development life cycle, to ensure that the automation file is robust, efficient, and free from common issues that could lead to errors or difficulties in the future.

RPA release managers or RPA admins select code quality check rules from a pre-defined set of rules in the RPA Hub instance.

Then, the RPA Desktop Design Studio performs an in-built code quality check before publishing a package. RPA developers can also perform pro-active code quality check on a package in the RPA Desktop Design Studio by inspecting an activity or a complete automation project for any issues, using the **Code Quality Check** feature.

The issues and their details are displayed in the **Code Quality Check Results** window. Double-click an individual entry to view the component that has displayed an error or a warning. Troubleshoot the issues before you publish the automation project to RPA Hub. For more information on how to perform Code Quality Check in RPA Desktop Design Studio, see [Code quality check in RPA Desktop Design Studio](../../rpa-studio/concept/code-quality-check-studio.md).

If an error or a warning occurs in the automation, a decision is derived if the package can be published successfully or not, based on the [system property](../reference/rpahub-sys-properties.md) \[**sn\_rpa\_fdn.restrict\_package\_by\_severity**\] configuration \(error, warning, or no restrictions\). For more information about compliance rules for RPA Desktop Design Studio, see [Code quality check compliance for RPA Desktop Design Studio](../reference/cqc-publish-studio.md).

If a package version is marked with code quality result as error or warning, a decision is derived if the bot process can be published successfully or not, based on the [system property](../reference/rpahub-sys-properties.md) \[**sn\_rpa\_fdn.restrict\_package\_by\_severity**\] configuration \(error, warning, or no restrictions\). For more information about compliance rules for RPA Hub, see [Code quality check compliance for RPA Hub](../reference/cqc-publish-rpa-hub.md).

View a list of the pre-defined code quality rules in the RPA Hub instance. For more information, see [Code quality rules list in RPA Hub](../reference/cqr-list-rpa.md).

View a code quality rule form along with the type and description. For more information, see [Code quality rule form in RPA Hub](../task/edit-cqr-rpa.md#).

In the code quality rule form, RPA release managers and admins can edit the **Severity**, **Regular Expression**, **Active**, and **Value** fields.

View the result of the code quality check, in the **Code Quality Result** field of an associated package version in RPA Hub. For more information, see [Package Version form in RPA Hub](../task/create-package.md#).

## Configuration

To enable the code quality check at the instance level, ensure that you mark the new system property **sn\_rpa\_fdn.enable\_code\_quality\_check** as true.

Additionally, configure the following system properties:

-   **sn\_rpa\_fdn.restrict\_package\_by\_severity** - To set a restriction on publishing a package from RPA Desktop Design Studio and publishing a bot process in RPA Hub.
-   **sn\_rpa\_fdn.code\_quality\_check\_timeout** - To enter a maximum duration, in minutes, for the completion of the code quality check.

These system properties are effective only when code quality check feature **sn\_rpa\_fdn.enable\_code\_quality\_check** is enabled. For more information about these properties and values, see [Configure RPA Hub properties](../reference/rpahub-sys-properties.md).

-   **[Code quality rules list in RPA Hub](../reference/cqr-list-rpa.md)**  
View a list of pre-defined rules that RPA admins can set for the RPA developers to follow as a code quality standard.
-   **[Code quality check compliance for RPA Desktop Design Studio](../reference/cqc-publish-studio.md)**  
View a list of compliance rules that the Code Quality Check feature follows if a package is published from RPA Desktop Design Studio.
-   **[Code quality check compliance for RPA Hub](../reference/cqc-publish-rpa-hub.md)**  
View a list of compliance rules that the Code Quality Check feature follows if a bot process is published from RPA Hub.
-   **[View the code quality rules list in RPA Hub](../task/view-cqr-rpa.md)**  
View a list of the pre-defined code quality check rules along with their active status and severity.
-   **[Update a code quality rules form in RPA Hub](../task/edit-cqr-rpa.md#)**  
Update few fields in the code quality rule form to set the code quality check standard.

**Parent Topic:**[Using RPA Hub](managing-rpa-hub.md)

