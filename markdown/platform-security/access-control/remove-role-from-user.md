---
title: Removing Roles from users
description: Use the Simulate Remove Role for simulating the user's access changes for a resource \(tables\).
locale: en-US
release: zurich
product: Access Control
classification: access-control
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using the Access Simulator, Access Simulator, Access analyzer, Access Management]
---

# Removing Roles from users

Use the **Simulate Remove Role** for simulating the user's access changes for a resource \(tables\).

## Before you begin

Role required: admin, access\_analyzer\_admin

Enable the take actions. For more information, see [Configuring the Access Simulator \(Take actions\)](configure-access-simulator.md).

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Access Simulator**.

2.  Select **Simulate** from the Remove a Role from the user section.

3.  Specify the following fields for your simulation criteria:

    |Field|Description|
    |-----|-----------|
    |Select user \*|Specify a user name to select from the list. In this example, **Abel Tuter**.|
    |Select role \*|Specify a role to select from the list. In this example, **itil**.|
    |Rule type \*|Rule type is auto-populated and it can’t be changed.|
    |Select table \*|Specify a table name to select from the list. In this example, **Incident**.|
    |Select record|Specify a record name to select from the list.|
    |Select field|Specify a field name to select from the list. This field can be used to analyze permission even at a field level. For example, Active, Created By, and so on.|

    ![Remove a role - criteria](../images/simulate-remove-criteria.png)

4.  Select **Next**.

5.  Preview the changes.

    The roles that are removed are simulated in the Preview changes. You can validate the roles and child roles that are being removed to the user before moving to the next step.

    ![Preview changes](../images/simulate-remove-preview.png)

6.  Select **Next**.

7.  Validate the **Present status** and **Simulated status** to verify the access that is being **Passed** or **Blocked** to the simulated user.

    ![Results](../images/simulate-remove-results.png)

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
    The roles are successfully removed from the user. You can verify the access using the Access Analyzer. For more information about how to verify the access of a user, see [Access analyzer](../concept/access-analyzer.md).


