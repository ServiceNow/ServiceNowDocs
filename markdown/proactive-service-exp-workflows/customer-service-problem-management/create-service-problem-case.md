---
title: Create a service problem case from the workspace
description: Create a service problem case for a customer raised issue so that an agent can work on it and resolve the service-related problem.
locale: en-US
release: zurich
product: Customer Service Problem Management
classification: customer-service-problem-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Customer Service Problem Management]
---

# Create a service problem case from the workspace

Create a service problem case for a customer raised issue so that an agent can work on it and resolve the service-related problem.

## Before you begin

Role required: sn\_sprb\_mgmt.agent

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon.

3.  Navigate to **Service Problem Case** &gt; **All**.

4.  Select **New**.

5.  On the service definition page, select the **Telecom Services Support** from the list.

6.  Select the applicable service definitions from the list.

    **Note:** The fibre broadband service definition as been shipped as a part of the demo data.

    For more information about service definition, see [Service definitions](https://www.servicenow.com/docs/access?context=csm-service-definitions&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

7.  Select **Create case**.

    In service definition, when you select **Create case** a playbook record generator form appears. Fill the playbook record generator form. For more information about the playbook record generator, see [Set up a record generator for case type](https://www.servicenow.com/docs/access?context=setup-record-generator-for-case-type&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

8.  On the intake form of verify issue, fill in the fields.

    ![Create new service problem case.](../image/create-new-service-problem-case.png)

<table id="table_x4b_pvh_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

The name of the company associated with this case.If you select a contact in the Contact field, this field is auto-filled if the account information is available in the contact record.

</td></tr><tr><td>

Contact

</td><td>

Name of the customer contact for this case.

</td></tr><tr><td>

Service

</td><td>

Name of the affected service for this case.

</td></tr><tr><td>

Short description

</td><td>

Description of the customer issue or problem.

</td></tr><tr><td>

Actual start

</td><td>

Actual start date of the issue.

</td></tr><tr><td>

Issue type

</td><td>

Types of issues-   Question
-   Issue
-   Feature


</td></tr><tr><td>

Issue severity

</td><td>

Imported severity on the issue. Values 1–4.

</td></tr><tr><td>

Description

</td><td>

Brief description of the customer issue or problem.

</td></tr></tbody>
</table>9.  Select **Continue**.


