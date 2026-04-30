---
title: Removing users from Groups
description: Use the Simulate Remove from Group for simulating the user's access changes for a resource \(tables\) when the user is removed from a group.
locale: en-US
release: zurich
product: Access Control
classification: access-control
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using the Access Simulator, Access Simulator, Access analyzer, Access Management]
---

# Removing users from Groups

Use the **Simulate Remove from Group** for simulating the user's access changes for a resource \(tables\) when the user is removed from a group.

## Before you begin

Role required: admin, access\_analyzer\_admin

Enable the take actions. For more information, see [Configuring the Access Simulator \(Take actions\)](configure-access-simulator.md).

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Access Simulator**.

2.  Select **Simulate** from the Remove the user from a Group section.

3.  Specify the following fields for your simulation criteria:

    |Field|Description|
    |-----|-----------|
    |Select user \*|Specify a user name to select from the list. In this example, **ITIL User**.|
    |Select group \*|Specify a group to select from the list. In this example, **Incident Management**.|
    |Rule type \*|Rule type is auto-populated and it can’t be changed.|
    |Select table \*|Specify a table name to select from the list. In this example, **Incident**.|
    |Select record|Specify a record name to select from the list.|
    |Select field|Specify a field name to select from the list. This field can be used to analyze permission even at a field level. For example, Active, Created By, and so on.|

    d![Remove the user from a group- criteria](../images/simulate-remove-group-criteria.png)

4.  Select **Next**.

5.  Preview the changes.

    The group from which the user is removed is simulated in the Preview changes. You can validate the changes before moving to the next step.

    ![Preview](../images/simulate-remove-group-preview.png)

6.  Select **Next**.

7.  Validate the **Present status** and **Simulated status** to verify the access that is being **Passed** or **Blocked** to the simulated user.

    ![Results](../images/simulate-remove-group-results.png)

    **Note:**

    -   If you want to know more about the ACL \(operations\), select the operation links for each record.
    -   If you want to start the simulation again for a different role, select **Start over**.
    -   If you want to exit the simulation, select **Exit**.
8.  Select **Next**.

9.  Select **Remove and complete**.

    **Note:**

    -   If the Access Simulator isn’t enabled, you can't complete the simulation. To enable, select **Enable actions** and accept the legal information.
    -   If you want to hide the simulation, select **Hide actions**. To unhide and enable actions, go to the settings. For more information, see [Configuring the Access Simulator \(Take actions\)](configure-access-simulator.md).
    -   If you want to exit the simulation, select **Skip and Exit**.
    The user is successfully removed from the user.


