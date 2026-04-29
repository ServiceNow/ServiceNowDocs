---
title: Removing users from Groups
description: Use the Simulate Remove from Group for simulating the user's access changes for a resource \(table\).
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using the Access Simulator, Access simulator, Access Analyzer, Access Management]
---

# Removing users from Groups

Use the **Simulate Remove from Group** for simulating the user's access changes for a resource \(table\).

## Before you begin

Role required: access\_analyzer\_admin

Enable Take actions. For more information, see [Configuring the Access Simulator \(Take actions\)](configure-access-simulator.md).

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Access Simulator**.

2.  Select **Simulate** from the **Remove the user from a Group** section.

3.  In the **Simulation criteria** view, configure the following fields:

    |Field|Description|
    |-----|-----------|
    |Select user \*|Specify a user name and select from the list. In this example, **ITIL User**.|
    |Select group \*|Specify a group and select from the list. In this example, **Incident Management**.|
    |Rule type \*|Rule type is auto-populated and can’t be changed.|
    |Select table \*|Specify a table name and select from the list. In this example, **Incident**.|
    |Select record|Specify a record name and select from the list.|
    |Select field|Specify a field name to select from the list. This field can be used to analyze permissions at the field level. For example, **Active**, **Created By**, and so on.|

    d![Remove the user from a group- criteria](../images/simulate-remove-group-criteria.png)

4.  Select **Next**.

5.  Preview the changes.

    Use the **Preview changes** view to see a simulation of your configured choices. Validate the group that has been removed from the user before moving to the next step.

    ![Preview](../images/simulate-remove-group-preview.png)

6.  Click **Next**.

7.  In the **Simulated results** view, check the **Present status** and **Simulated status** to validate that access is **Passed** or **Blocked** to the simulated user as intended.

    ![Results](../images/simulate-remove-group-results.png)

    **Note:**

    -   To know more about an ACL \(operation\) in the **Simulated results** view, click its operation link.
    -   To start the simulation again for a different role, click **Start over**.
    -   To exit the simulation, click **Exit**.
8.  Click **Next**.

9.  To apply the simulated changes, on the **Take action** view, click **Remove and complete**.

    **Note:**

    -   If Access Simulator isn’t enabled, you can't complete the simulation. To enable it, select **Enable actions** and accept the legal information.
    -   To hide the simulation, select **Hide actions**. To unhide and enable actions, go to **Settings**. For more information, see [Configuring the Access Simulator \(Take actions\)](configure-access-simulator.md).
    -   To exit the simulation without applying the simulated changes, select **Skip and Exit**.
    If you clicked **Remove and complete**, the simulated group is successfully removed from the user. You can verify the access again by using the Access Analyzer. For more information about how to verify access of a user, see [Access Analyzer](../concept/access-analyzer.md).


