---
title: Adding Roles to users
description: Use the Simulate Add Role for simulating the user's access changes for a resource \(table\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/access-control/add-role-to-user.html
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using the Access Simulator, Access simulator, Access Analyzer, Access Management]
---

# Adding Roles to users

Use the **Simulate Add Role** for simulating the user's access changes for a resource \(table\).

## Before you begin

Role required: access\_analyzer\_admin

Enable Take actions. For more information, see [Configuring the Access Simulator \(Take actions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/configure-access-simulator.md).

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Access Simulator**.

2.  Select **Simulate** from the **Add a Role to the user** section.

3.  In the **Simulation criteria** view, configure the following fields:

    |Field|Description|
    |-----|-----------|
    |Select user \*|Specify a user name to select from the list. In this example, **Abel Tuter**.|
    |Select role \*|Specify a role to select from the list. In this example, **itil\_admin**.|
    |Rule type \*|Rule type is auto-populated and it can’t be changed.|
    |Select table \*|Specify a table name to select from the list. In this example, **Incident**.|
    |Select record|Specify a record name to select from the list \(Optional\).|
    |Select field|Specify a field name to select from the list. This field can be used to analyze permissions at the field level. For example, **Active**, **Created By**, and so on.|

    \[Omitted image "simulate-add-criteria.png"\] Alt text: Add a role to a user - criteria

4.  Click **Next**.

5.  Preview the changes.

    Use the **Preview changes** view to see a simulation of your configured choices. Validate the roles and child roles that have been added to the user before moving to the next step.

    \[Omitted image "simulate-add-preview.png"\] Alt text: Preview changes

    In this example, you can see the new child roles that have been added in this simulation \(highlighted in green, as **Role or Group being added**\) as part of the **itil\_admin** role, along with the user's currently assigned roles \(Role or group being unchanged\).

6.  Click **Next**.

7.  In the **Simulated results** view, check the **Present status** and **Simulated status** to validate that access is **Passed** or **Blocked** to the simulated user as intended.

    \[Omitted image "simulate-add-results.png"\] Alt text: Results

    In this example, adding the **itil\_admin** role enables the user to perform delete operations on the table \(Incident\).

    **Note:**

    -   To know more about an ACL \(operation\) in the **Simulated results** view, click its operation link.
    -   To start the simulation again for a different role, click **Start over**.
    -   To exit the simulation, click **Exit**.
8.  Click **Next**.

9.  To apply the simulated changes, on the **Take action** view, click **Add and complete** .

    \[Omitted image "simulate-add-actions.png"\] Alt text: Actions

    **Note:**

    -   If Access Simulator isn’t enabled, you can't complete the simulation. To enable it, select **Enable actions** and accept the legal information.
    -   To hide the simulation, select **Hide actions**. To unhide and enable actions, go to **Settings**. For more information, see [Configuring the Access Simulator \(Take actions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/configure-access-simulator.md).
    -   To exit the simulation without applying the simulated changes, select **Skip and Exit**.
    If you clicked **Add and complete**, the simulated roles are successfully added to the user. You can verify the access again by using the Access Analyzer. For more information about how to verify access of a user, see [Access Analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-analyzer.md).


