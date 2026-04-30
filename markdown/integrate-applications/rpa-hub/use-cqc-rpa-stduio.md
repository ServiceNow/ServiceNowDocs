---
title: Fix automation issues with Code quality check in RPA Desktop Design Studio
description: Fix the automation issues in your automation activity or complete an automation project proactively by using the Code quality check feature in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Code quality check in RPA Desktop Design Studio, Using automations, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Fix automation issues with Code quality check in RPA Desktop Design Studio

Fix the automation issues in your automation activity or complete an automation project proactively by using the Code quality check feature in RPA Desktop Design Studio.

## Before you begin

Connect to the RPA Hub instance that has the Code quality check feature enabled. For more information on how to connect to an RPA Hub instance, see [Connect to an RPA Hub instance from RPA Desktop Design Studio](connect-studio-instance-rpa.md).

Role required: RPA Developer

## Procedure

1.  On the toolbar of the **Design** tab in RPA Desktop Design Studio, select **Code quality check**.

    The **Code quality check** options are displayed.

    ![Options for Code Quality Check in RPA Desktop Design Studio.](../image/cqc-options.png "Options for Code quality check")

    **Note:** If you aren't connected to an instance and you select the **Code quality check** option, the Connection Manager window is displayed. For more information on how to connect to an RPA Hub instance, see [Connect to an RPA Hub instance from RPA Desktop Design Studio](connect-studio-instance-rpa.md).

2.  Do Code quality check for the following options.

    |Code quality check option|Description|
    |-------------------------|-----------|
    |**Check complete project**|Performs code quality check for the complete automation project. Use this option if your automation project has multiple activities and you don’t want to do a Code quality check for each of them. The results are displayed in the Code Quality Check Results window.|
    |**__Check current activity__**|Performs Code quality check for the current activity.|

    The results are displayed in the Code Quality Check Results window.

    **Note:** If you select the option **Check complete project** or the option **Check current activity** and there’s a connectivity issue, a timeout error is displayed. Contact your RPA administrator for more information.

3.  In the Code Quality Check Results window, view the issue results and their details as a list.

    The results are classified as error, warning, and information based on the severity that is set by the RPA administrator or release manager. You can filter the results by the severity level by selecting the **All** button. The **Name** field indicates the type of issue that is based on the code quality rules configured in RPA Hub. For more information on the list of code quality rules, see [Code quality rules list in RPA Hub](../../rpa-hub/reference/cqr-list-rpa.md).

    ![Code Quality Check Results window](../image/cqc-results.png "Code Quality Check Results window")

    You can double-click the result entries for components in the Code Quality Check Results window for the following scenarios:

    -   If an affected component is in the current activity, it’s highlighted in the current activity.
    -   If the affected component is in a different activity, you can navigate to that activity. The affected component is highlighted.
    ![Highlighting of the affected component in the code quality check.](../image/cqc-error-highlight.png "Highlighting the affected component in code quality check")

4.  View the list of active and inactive rules that are configured from the RPA Hub instance by selecting **View Rules**.

    ![View Rules window for code quality check.](../image/cqc-view-rules.png "View Rules window for Code Quality Check")

5.  Fix the issues that pertain to the code quality check and your automation project is ready to be published.


## What to do next

The automation project is ready to be published. Code quality check is also performed automatically when you publish a project. For more information on how to publish a project, see [Publish an automation project in RPA Desktop Design Studio](publish-automation-project.md).

**Parent Topic:**[Code quality check in RPA Desktop Design Studio](../concept/code-quality-check-studio.md)

