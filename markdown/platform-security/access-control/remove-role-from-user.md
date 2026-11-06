---
title: Remove roles from users
description: Use the Simulate Remove Role for simulating the user's access changes for a resource \(tables\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/access-control/remove-role-from-user.html
release: zurich
product: Access Control
classification: access-control
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use the Access Simulator, Access Simulator, Access analyzer, Access Management]
---

# Remove roles from users

Use the **Simulate Remove Role** for simulating the user's access changes for a resource \(tables\).

## Before you begin

Role required: admin, access\_analyzer\_admin

The take actions must be enabled. For more information, see [Configure the Access Simulator \(Take actions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/access-control/configure-access-simulator.md).

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Access Simulator**.

2.  Select **Simulate** from the Remove a Role from the user section.

3.  Specify the following fields for your simulation criteria.

    |Field|Description|
    |-----|-----------|
    |Select user|Name of the user, selected from the list. In this example, **Abel Tuter**.|
    |Select role|Name of the role, selected from the list. In this example, **itil**.|
    |Rule type|Rule type is auto-populated.|
    |Select table|Name of the table, selected from the list. In this example, **Incident**.|
    |Select record|Name of the record, selected from the list.|
    |Select field|Name of the field, selected from the list. This field can be used to analyze permission even at a field level. For example, Active, Created By, and so on.|

    \[Omitted image "simulate-remove-criteria.png"\] Alt text: Remove a role - criteria

4.  Select **Next**.

5.  Preview the changes.

    The roles that are removed are simulated in the Preview changes. You can validate the roles and child roles that are being removed from the user before moving to the next step.

    \[Omitted image "simulate-remove-preview.png"\] Alt text: Preview changes

6.  Select **Next**.

7.  Validate the **Present status** and **Simulated status** to verify the access that is being **Passed** or **Blocked** to the simulated user.

    \[Omitted image "simulate-remove-results.png"\] Alt text: Results

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
    The roles are successfully removed from the user. You can verify the access using the Access Analyzer. For more information about how to verify the access of a user, see [Access analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/access-control/access-analyzer.md).


