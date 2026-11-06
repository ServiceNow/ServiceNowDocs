---
title: Remove users from groups
description: Use the Simulate Remove from Group for simulating the user's access changes for a resource \(tables\) when the user is removed from a group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/access-control/remove-user-from-group.html
release: zurich
product: Access Control
classification: access-control
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use the Access Simulator, Access Simulator, Access analyzer, Access Management]
---

# Remove users from groups

Use the **Simulate Remove from Group** for simulating the user's access changes for a resource \(tables\) when the user is removed from a group.

## Before you begin

Role required: admin, access\_analyzer\_admin

The take actions must be enabled. For more information, see [Configure the Access Simulator \(Take actions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/access-control/configure-access-simulator.md).

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Access Simulator**.

2.  Select **Simulate** from the Remove the user from a Group section.

3.  Specify the following fields for your simulation criteria.

    |Field|Description|
    |-----|-----------|
    |Select user|Name of the user, selected from the list. In this example, **ITIL User**.|
    |Select group|Name of the group, selected from the list. In this example, **Incident Management**.|
    |Rule type|Rule type is auto-populated.|
    |Select table|Name of the table, selected from the list. In this example, **Incident**.|
    |Select record|Name of the record, selected from the list.|
    |Select field|Name of the field, selected from the list. This field can be used to analyze permission even at a field level. For example, Active, Created By, and so on.|

    \[Omitted image "simulate-remove-group-criteria.png"\] Alt text: Remove the user from a group criteria

4.  Select **Next**.

5.  Preview the changes.

    The group from which the user is removed is simulated in the Preview changes. You can validate the changes before moving to the next step.

    \[Omitted image "simulate-remove-group-preview.png"\] Alt text: Preview

6.  Select **Next**.

7.  Validate the **Present status** and **Simulated status** to verify the access that is being **Passed** or **Blocked** to the simulated user.

    \[Omitted image "simulate-remove-group-results.png"\] Alt text: Results

    **Note:**

    -   To learn more about the ACL \(operations\), select the operation links for each record.
    -   To start the simulation again for a different role, select **Start over**.
    -   To exit the simulation, select **Exit**.
8.  Select **Next**.

9.  Select **Remove and complete**.

    **Note:**

    -   If the Access Simulator isn’t enabled, you can't complete the simulation. To enable, select **Enable actions** and accept the legal information.
    -   To hide the simulation, select **Hide actions**. To unhide and enable actions, go to the settings. For more information, see [Configure the Access Simulator \(Take actions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/access-control/configure-access-simulator.md).
    -   To exit the simulation, select **Skip and Exit**.
    The user is successfully removed from the group.


