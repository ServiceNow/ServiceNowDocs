---
title: Create and manage cases for a consumer or household
description: Staff members with the location agent role can create and manage cases for consumers and households.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring households, Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Create and manage cases for a consumer or household

Staff members with the location agent role can create and manage cases for consumers and households.

## Before you begin

Role required: sn\_customerservice.svc\_location\_agent, sn\_customerservice.svc\_location\_consumer\_agent, sn\_customerservice.svc\_location\_manager

## About this task

Staff members at a business location who have either the location agent or consumer location agent role can create cases for households and consumers.

Staff members or internal users who have a relationship with a household \(based on the Relationship Manager responsibility\) can create cases for that household and its members. Users with relationships to a household are listed in the following locations:

-   The Household Team related list on the Household form.
-   The Household Team Members list.

Relationship managers can perform the following actions on the cases that they can access:

-   Add comments and work notes.
-   Add attachments.
-   Close cases.

When a consumer case is created or updated, the consumer receives an email notification. If a household is added to a case, the head of household is also notified when the case is created or updated.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Cases** and click **Create New**.

2.  Select the type of case that you want to create.

3.  Perform one of the following actions.

<table id="choicetable_cyw_rnc_gmb"><tbody><tr><td id="d162071e112">

**Add a consumer.**

</td><td>

Select a consumer in the **Consumer** field. -   If the consumer belongs to only one household, the **Household** field is automatically updated.
-   If the consumer belongs to more than one household, select a household from the households that a consumer belongs to in the **Household** field.
-   If the consumer does not belong to a household, you can leave the **Household** field empty.


</td></tr><tr><td id="d162071e145">

**Add a household.**

</td><td>

Select a household in the **Household** field. -   If the household only has only one current member, the **Consumer** field is automatically updated.
-   If the household has multiple current members, select a consumer from the household members in the **Consumer** field.


</td></tr></tbody>
</table>4.  Fill in the remaining fields on the [Case form](../reference/r_CustomerServiceCaseForm.md).

5.  If desired, add other members of the household to the watch list.

    If a user with a Relationship Manager relationship is creating a case for a household or household member, this user is automatically added to the watch list.

6.  Click **Submit**.

    The case is added to the Cases related list on the Household form.


**Related topics**  


[Service Model Foundation cases](../reference/industry-data-model-cases.md)

