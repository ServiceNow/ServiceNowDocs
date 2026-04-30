---
title: Create a card dispute service case
description: An agent can begin the card dispute or report a dispute by creating a dispute case on behalf of a customer.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing dispute service requests, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Create a card dispute service case

An agent can begin the card dispute or report a dispute by creating a dispute case on behalf of a customer.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent, sn\_bom\_credit\_card.dispute\_agent\_connector, or sn\_bom\_credit\_card.contributor

**Note:** The applicable universal contributor role can also be assigned to create a case. For more information, see [User roles and FSO Business rules](../../fso-common/reference/fso-core-roles.md).

**Important:** For the agent connector or contributor role to work, they must be combined with one of the roles in CSM industry data model or Contributor users. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon.

3.  Create a case from the dispute service case list or an interaction record.

<table id="choicetable_z4t_j3h_gmb"><thead><tr><th align="left" id="d89333e106">

Option

</th><th align="left" id="d89333e109">

Steps

</th></tr></thead><tbody><tr><td id="d89333e115">

**Dispute case from the dispute case list**

</td><td>

1.  In the **Lists** tab, under **Card disputes service cases**, click **All**.
2.  Select **New**.


</td></tr><tr><td id="d89333e145">

**Dispute case from an interaction record**

</td><td>

1.  In the **Lists** tab, under **Interactions**, click **My Interactions**.
2.  Open the required interaction record for the customer.
3.  Select **Create Case**.
 For information on how to create an interaction, see [Create an interaction](https://www.servicenow.com/docs/access?context=create-interactions&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  In the Create a new case dialog box, select **Card disputes services** from the category list.

5.  From the Select service list, select **Dispute card transactions**.

6.  Select **Create**.


## Result

-   A dispute service case is created in the New state.
-   The dispute agent can continue working through the Initiate phase of the case. See [Initiate a dispute](initiating-dispute.md).

**Parent Topic:**[Managing dispute service requests](../concept/managing-card-disputes.md)

