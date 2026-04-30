---
title: Create an individual life service case
description: A processor or contributor can begin the policy request process by creating an individual life case on behalf of your customer.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Individual Life Servicing, Life Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Create an individual life service case

A processor or contributor can begin the policy request process by creating an individual life case on behalf of your customer.

## Before you begin

Role required: sn\_ins\_indiv\_life.processor, sn\_ins\_indiv\_life.processor\_connector, or sn\_ins\_indiv\_life.contributor

**Note:** The applicable universal contributor role can also be assigned to create a case. For more information, see [User roles and FSO Business rules](../../fso-common/reference/fso-core-roles.md).

**Important:** For the agent connector or contributor role to work, they must be combined with one of the roles in CSM industry data model or Contributor users. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

Contributors and processors can submit individual policy service requests for customers from their workspace.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  Create a case from the individual life service case list or an interaction record.

<table id="choicetable_z4t_j3h_gmb"><thead><tr><th align="left" id="d52980e124">

Option

</th><th align="left" id="d52980e127">

Steps

</th></tr></thead><tbody><tr><td id="d52980e133">

**Individual life case from the individual life case list**

</td><td>

1.  In the **Lists** tab, under **Individual life service cases**, click **All**.
2.  Select **New**.


</td></tr><tr><td id="d52980e163">

**Individual life case from an interaction record**

</td><td>

1.  In the **Lists** tab, under **Interactions**, select **My Interactions**.
2.  Open the required interaction record for the customer.
3.  Select **Create Case**.
 For information on how to create an interaction, see [Create an interaction](https://www.servicenow.com/docs/access?context=create-interactions&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  In the Create a new case dialog box, select the individual life service that you want to create a case for.

    -   **Add/Change beneficiary**
    -   **Increase coverage**
    -   **Decrease coverage**
    -   **Convert term to perm**
    -   **Cancel policy**
5.  Select **Create**.

6.  On the form, fill in the required fields and any other related information that you've gathered from the customer.

7.  Select **Save**.


## Result

Based on the request type, a policy service case is created in the New state. The case is assigned to an assignment group or a policy processor in the policy service department. The assignment group or user that the case is assigned to is based on the assignment rules.

