---
title: Add a user to a group
description: Use the Simulate Add to Group for simulating the user's access changes for a resource \(tables\) when the user is added to a group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/access-control/add-user-to-group.html
release: zurich
product: Access Control
classification: access-control
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use the Access Simulator, Access Simulator, Access analyzer, Access Management]
---

# Add a user to a group

Use the **Simulate Add to Group** for simulating the user's access changes for a resource \(tables\) when the user is added to a group.

## Before you begin

Role required: admin, access\_analyzer\_admin

The take actions must be enabled. For more information, see [Configure the Access Simulator \(Take actions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/access-control/configure-access-simulator.md).

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Access Simulator**.

2.  Select **Simulate** from the Add the user to a Group section.

3.  Specify the following fields for your simulation criteria:

    |Field|Description|
    |-----|-----------|
    |Select user|Name of the user to select from the list. In this example, **Abel Tuter**.|
    |Select group|Group to select from the list. In this example, **Incident Management**.|
    |Rule type|Auto-populated rule type.|
    |Select table|Table name to select from the list. In this example, **Incident**.|
    |Select record|Record name to select from the list.|
    |Select field|Field name to select from the list. This field can be used to analyze permission even at a field level. For example, Active, Created By, and so on.|

    \[Omitted image "simulate-add-group-criteria.png"\] Alt text: Add the user to a group- criteria

4.  Select **Next**.

5.  Preview the changes.

    The group that the user is assigned is simulated in the Preview changes. You can validate the changes before moving to the next step.

    \[Omitted image "simulate-add-group-preview.png"\] Alt text: Preview changes

6.  Select **Next**.

7.  Validate the **Present status** and **Simulated status** to verify the access that is being **Passed** or **Blocked** to the simulated user.

    \[Omitted image "simulate-add-group-results.png"\] Alt text: Results

    **Note:**

    -   To learn more about the ACL \(operations\), select the operation links for each record.
    -   To start the simulation again for a different role, select **Start over**.
    -   To exit the simulation, select **Exit**.
8.  Select **Next**.

9.  Select **Add and complete**.

    **Note:**

    -   If the Access Simulator isn’t enabled, you can't complete the simulation. To enable, select **Enable actions** and accept the legal information.
    -   To hide the simulation, select **Hide actions**. To unhide and enable actions, go to the settings. For more information, see [Configure the Access Simulator \(Take actions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/access-control/configure-access-simulator.md).
    -   To exit the simulation, select **Skip and Exit**.
    The user is successfully added to the group.


