---
title: Create a group life service case
description: A processor or contributor can begin the change member info request process by creating a group life case on behalf of your customer.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Group Life Servicing, Group Life Servicing, Life Insurance Servicing, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Create a group life service case

A processor or contributor can begin the change member info request process by creating a group life case on behalf of your customer.

## Before you begin

Role required: sn\_ins\_group\_life.processor, sn\_ins\_group\_life.processor\_connector, or sn\_ins\_group\_life.contributor

**Note:** The applicable universal contributor role can also be assigned to create a case. For more information, see [User roles and FSO Business rules](../../fso-common/reference/fso-core-roles.md).

**Important:** For the agent connector or contributor role to work, they must be combined with one of the roles in CSM industry data model or Contributor users. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

Contributors and processors can submit group policy service requests for customers.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../../fso-card-operations/image/list-icon.png)\).

3.  Create a case from the group life service case list or an interaction record.

<table><thead><tr><th align="left" id="d38280e121">

Option

</th><th align="left" id="d38280e124">

Steps

</th></tr></thead><tbody><tr><td id="d38280e130">

**Group life case from the group life case list**

</td><td>

1.  In the **Lists** tab, under **Group life service cases**, click **All**.
2.  Select **New**.


</td></tr><tr><td id="d38280e160">

**Group life case from an interaction record**

</td><td>

1.  In the **Lists** tab, under **Interactions**, click **My Interactions**.
2.  Open the required interaction record for the customer.
3.  Select **Create Case**.
 For information on how to create an interaction, see [Create an interaction](https://www.servicenow.com/docs/access?context=create-interactions&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  In the Create a new case dialog box, select **Group life change member info**.

5.  Select **Create**.

6.  On the form, fill in the required fields and any other related information that you've gathered from the customer.

7.  Select **Save**.


## Result

Based on the request type, a policy service case is created in the New state. The case is assigned to an assignment group or a policy processor in the policy service department. The assignment group or user that the case is assigned to is based on the assignment rules.

