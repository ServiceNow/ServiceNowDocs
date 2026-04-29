---
title: Submit a policy service request
description: Help your customers by submitting a policy service request for them.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Commercial Lines Servicing, Property and Casualty Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Submit a policy service request

Help your customers by submitting a policy service request for them.

## Before you begin

Role required: sn\_ins\_policy\_b2b.contributor

**Note:** The applicable universal contributor role can also be assigned to create a case. For more information, see [User roles and FSO Business rules](../../fso-common/reference/fso-core-roles.md).

**Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

Requestors, contributors, and processors can submit policy service requests for customers.

Customers can submit policy service requests from the Consumer Service Portal or another self-service portal. They can select a service catalog item, fill out the necessary form, and then submit a form.

**Note:** Before your customers can submit a request using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  Create a policy service request from the customer record or an interaction record.

<table id="choicetable_z4t_j3h_gmb"><thead><tr><th align="left" id="d60430e127">

Option

</th><th align="left" id="d60430e130">

Steps

</th></tr></thead><tbody><tr><td id="d60430e136">

**Policy service request from a customer record**

</td><td>

1.  In the **Lists** tab, under **Customer**, click **Consumers**.
2.  Click the customer record that you want to open.


</td></tr><tr><td id="d60430e163">

**Policy service request from an interaction record**

</td><td>

1.  In the **Lists** tab, under **Interactions**, click **My Interactions**.
2.  Click the interaction record for the customer that you want to open.
 For information on how to create an interaction, see [Create an interaction](https://www.servicenow.com/docs/access?context=create-interactions&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Click **Create Policy Request**.

5.  From the Catalogs list, select **Financial Services**.

6.  Under **Categories**, click **Insurance Policy Service**.

7.  Click a policy service that you want to submit a request for.

8.  Fill in any necessary information that is related to the request.

    **Note:** Each policy service request form has a different set of fields that are based on the policy service.

9.  Click **Submit**.


## Result

Based on the request type, a policy service case is created in the New state. The case is assigned to an assignment group or a policy processor in the policy service department. The assignment group or user that the case is assigned to is based on the assignment rules.

## What to do next

-   Click **View Details** to open the policy service case and view its details. You can also add additional information in the **Comments** field that can help the policy processor in resolving the case.
-   A policy processor can start working on the case and its tasks.

**Parent Topic:**[Using Commercial Lines Servicing](../concept/using-financial-services-commercial-lines-servicing.md)

