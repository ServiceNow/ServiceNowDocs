---
title: Create a treasury service case
description: Begin the treasury service application process by creating a treasury case on behalf of your customer.
locale: en-US
release: australia
product: Financial Services Treasury Operations
classification: financial-services-treasury-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Treasury Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Create a treasury service case

Begin the treasury service application process by creating a treasury case on behalf of your customer.

## Before you begin

Role required: sn\_bom\_treasury.contributor or sn\_bom\_treasury.agent\_connector

**Note:** The applicable universal contributor role can also be assigned to create a case. For more information, see [User roles and FSO Business rules](../../fso-common/reference/fso-core-roles.md).

**Important:** For the agent connector or contributor role to work, they must be combined with one of the roles in CSM industry data model or Contributor users. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

A treasury agent can also create a treasury service case by navigating to **Treasury Service Cases** in the list view of the workspace and clicking **New**.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  Create a treasury case from the treasury case list or an interaction record.

<table id="choicetable_z4t_j3h_gmb"><thead><tr><th align="left" id="d130350e127">

Option

</th><th align="left" id="d130350e130">

Steps

</th></tr></thead><tbody><tr><td id="d130350e136">

**Treasury case from the treasury case list**

</td><td>

1.  In the **Lists** tab, under **Treasury Service Cases**, click **All**.
2.  Click **New**.


</td></tr><tr><td id="d130350e166">

**Treasury case from an interaction record**

</td><td>

1.  In the **Lists** tab, under **Interactions**, click **My Interactions**.
2.  Open the required interaction record for the customer.
3.  Click **Create Case**.
 For information on how to create an interaction, see [Create an interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/interaction-management/create-interactions.md).

</td></tr></tbody>
</table>4.  In the Create a new case dialog box, select the treasury service that you want to create a case for.

    -   **Onboard RDC service**.
    -   **Onboard Wire service**.
5.  Click **Create**.

6.  On the form, fill in the required fields and any other related information that you've gathered from the customer.

7.  Click **Save**.


## Result

-   A treasury service case is created in the New state and the workflow is triggered.
-   The case is assigned to an assignment group or an agent in the treasury service based on the defined assignment rules.

## What to do next

Collect all the required customer information and submit the application.

1.  In the **Playbook** tab, fill the data in the Initiate stage.​
2.  Submit the application to back-office agents for fulfilment.

**Parent Topic:**[Using Financial Services Treasury Operations](../concept/using-treasury-ops.md)

