---
title: Register other applications to request policy exceptions
description: Enable other applications to request policy exception from any table such as Problem or Incident and so on. The applications must be added and configured in the Integration Registry.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Allow policy exception requests from other applications, Policy and Compliance Management enhancement steps, Implementing Policy and Compliance Management, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Register other applications to request policy exceptions

Enable other applications to request policy exception from any table such as Problem or Incident and so on. The applications must be added and configured in the Integration Registry.

## Before you begin

Role required: sn\_compliance.manager

The GRC business user \(sn\_grc.business\_user\) or business user – lite \(sn\_grc.business\_user\_lite\) is the minimum required role to raise a policy exception from an upstream application.

## About this task

Starting with the New York release, users from any ServiceNow application can request for policy exceptions using \(GRC\)’s policy exception management capability. For example, users can request policy exception for a problem related to a group of incidents that cannot be resolved for a specific duration. To be able to request policy exception, you must register the application for policy exception and create a UI action for requesting policy exception, unless one is provided with the ServiceNow application.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policy Exceptions** &gt; **Integration Registry**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_yxw_n1t_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name of the registry entry.

</td></tr><tr><td>

Policy exception target table

</td><td>

Select the table on which a policy exception will be applied.

</td></tr><tr><td>

Exception applied on

</td><td>

Target record on which the exception is applied. The options are:-   One target record: Specific target record on which the exception is applied. Select the assessed object in the Compliance data source registry.
-   All target records: All target records on which the exception is applied. Select the policy exception target table on which the exception is applied.


</td></tr><tr><td>

Source type

</td><td>

Auto-populates **Controls** if the **Exception applied on** is **One target record**. Auto-populates **Control objective** if the **Exception applied on** is **All target records**.

</td></tr><tr><td>

Policy categories

</td><td>

Select one or more categories for filtering policies. For example, if you select the Vulnerability Response category, and are requesting an exception using that application, the list of all policies is filtered by that category, saving you time. For more information, see [Define policy categories](define-policy-categories.md).

</td></tr><tr><td class="sub-head" colspan="2">

**Entity Mapping**

</td></tr><tr><td>

Relationship

</td><td>

Select **Reference field** when the entity is a field in the Policy Exception \[sn\_compliance\_policy\_exception\] table. Select **Related list** when the entity is in a related list of the Policy Exception table.

</td></tr><tr><td>

Entity field

</td><td>

Enter the name of the field that points to the Entity \[sn\_grc\_profile\] table. This field displays only if you selected **Reference field** as the **Relationship**.

</td></tr><tr><td>

Mapping table

</td><td>

Select the table that establishes a relationship between the Policy Exception table and the Entity table. This field displays only if you selected **Related list** as the **Relationship**.

</td></tr><tr><td>

Policy exception target field

</td><td>

Select the field in the mapping table that points to the Policy Exception table. This field displays only if you selected **Related list** as the **Relationship**.

</td></tr><tr><td>

Entity field

</td><td>

Enter the name of the field in the mapping table that points to the Entity table.

</td></tr><tr><td class="sub-head" colspan="2">

**Request Source** **Note:** The fields in this section are needed only if you are requesting a policy exception from a table other than the Policy Exception Target table.

</td></tr><tr><td>

Table

</td><td>

Select the table that contains the records from which the policy exception will be requested.

</td></tr><tr><td>

Relationship

</td><td>

Select **Reference field** when the entity is a field in the Policy Exception \[sn\_compliance\_policy\_exception\] table. Select **Related list** when the entity is in a related list of the Policy Exception table

</td></tr><tr><td>

Request source field

</td><td>

Select the field that points to the request source table. This field displays only if you selected **Reference field** as the **Relationship** field in the **Request Source** section.

</td></tr><tr><td>

Mapping table

</td><td>

Select the table that establishes a relationship between the Policy Exception table and the Entity table. This field displays only if you selected **Related list** in the **Relationship** field in the **Request Source** section.

</td></tr><tr><td>

Policy exception target field

</td><td>

Select the field in the mapping table that points to the Policy Exception table. This field displays only if you selected **Related list** in the **Relationship** field in the **Request Source** section.

</td></tr><tr><td>

Request source field

</td><td>

Select the field in the mapping table that points to the request source table. This field displays only if you selected **Related list** in the **Relationship** field in the **Request Source** section.

</td></tr><tr><td class="sub-head" colspan="2">

**Questionnaire Details**

</td></tr><tr><td>

Exception questionnaire

</td><td>

Select a questionnaire template to generate a questionnaire for the requested policy exception. For more information, see [Create an exception questionnaire](create-except-quest.md).

</td></tr></tbody>
</table>4.  Save the record.

    The Reason Choices related list appears.

    **Note:** The Reason Choices are available to the person who requests a policy exception to explain the purpose of the request. So define reasons that apply to your specific situation. For more information, see [Define policy exception reason choices](define-reason-choices.md).


**Parent Topic:**[Allow policy exception requests from other applications](../concept/allow-other-app-policy-except.md)

