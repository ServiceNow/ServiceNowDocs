---
title: Create contact definition
description: Define the contact recipients of a particular plan to determine the target audience involved in each communication task and the responsibilities the recipients are expected to handle. A notification for a task is sent to all individuals specified for that task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/incident-communications-management/create-contact-definition-icm.html
release: zurich
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-11-11"
reading_time_minutes: 1
breadcrumb: [Communication contact definitions, Manage, Incident Communications Management, IT Service Management]
---

# Create contact definition

Define the contact recipients of a particular plan to determine the target audience involved in each communication task and the responsibilities the recipients are expected to handle. A notification for a task is sent to all individuals specified for that task.

## Before you begin

Role required: sn\_comm\_management.communication\_plan\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Incident Communication Management** &gt; **Contact Administration** &gt; **Contact Definitions**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_gqc_k2x_2lc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the contact definition.

</td></tr><tr><td>

Type

</td><td>

Type of contact such as user, group, or recipient list that you want to involve in the plan. The contact type is assigned dynamically at the time of the table execution. For information on recipient lists, see [Define a recipient list for communication contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/define-recipient-list-comm-contact.md). Available values:-   User
-   Group


</td></tr><tr><td>

Responsibility

</td><td>

Responsibility that the user, group, or individuals in the recipient list are expected to handle.

</td></tr><tr><td>

Source

</td><td>

Determines on how the user or group field is populated in the contact record. Possible values:-   Default Override
-   Form Field


</td></tr><tr><td>

Quantity

</td><td>

Minimum number of contacts associated with the contact records.

</td></tr><tr><td>

Active

</td><td>

Determines if the contact definition record is active.

</td></tr><tr><td>

Condition

</td><td>

Conditions to determine which records are applicable to the definition.

</td></tr></tbody>
</table>    For more information on creating a communication contact definition, see [Create communication contact definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/create-comm-contact-definition.md).

4.  Select **Submit**.

    **Note:** After the contact definition is created, the information is stored in the contact table. The **Classification** field in the contact table is read-only and has the following values:

    -   Manual - Added if the contact record is manually created.
    -   Definition \(default overrides\) - Added if you select the value in the **Source** field as **Default Override** and specify the users based on conditions.
    -   Definition \(source field\) - Added when you select the value in the **Source** field as **Form Field**.
    -   Communication Contact Definition - Added when the contact definition is created from the Contact definition related list in the Communication plan definition form.

**Parent Topic:**[Communication contact definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-communications-management/communication-contact-definition.md)

