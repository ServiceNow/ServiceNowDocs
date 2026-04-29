---
title: Create a technology product support case from the Customer Service Portal
description: Customers can create a technology product case to report an issue about the service from the Customer Service Portal.
locale: en-US
release: australia
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Technology Product Support Case, Use, Product Support for Technology]
---

# Create a technology product support case from the Customer Service Portal

Customers can create a technology product case to report an issue about the service from the Customer Service Portal.

## Before you begin

Role required: sn\_tech\_support.agent

## Procedure

1.  Go to the Customer Service Portal by accessing your instance URL and adding a /csm suffix.

2.  On the home page, select **Get help**.

3.  In the **Categories**, select a **Support** category from the list.

4.  Select **Create a Technology Product Case**.

    Case form as been created using a record producer. For more information about how to create record producer, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

5.  On the form, fill in the fields.

    ![technology product case.](../image/create-tech-product-case.png)

<table id="table_bw4_flz_pfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Issue Type

</td><td>

Select the type of issue for the case:-   Performance Issue
-   Question
-   Service Request
-   Something is Broken


</td></tr><tr><td>

Account

</td><td>

This account is default to logged-in user account

</td></tr><tr><td>

Contact

</td><td>

Auto-filled with the name of the logged-in user.

</td></tr><tr><td>

Sold Product

</td><td>

Select a product from the list of available products. This list includes the sold products for the logged-in user.

</td></tr><tr><td>

Affected Instances

</td><td>

Add the affected instances to this list.

</td></tr><tr><td>

Short description

</td><td>

Description of the issue or problem.

</td></tr><tr><td>

Business Impact

</td><td>

Impact that this issue is having on your business.

</td></tr><tr><td>

Steps to reproduce

</td><td>

Add the steps to reproduce the issue.

</td></tr><tr><td>

Contact Timezone

</td><td>

Displays the time zone of the user in the Contact field.

</td></tr></tbody>
</table>6.  Select **Submit**.

    When the service problem case is submitted, the stage is automatically set to **Verify** and state as **New**.


