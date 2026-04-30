---
title: Configure a resource generator for providing assignment group as an outcome
description: Configure a resource generator of type decision table that provides an assignment group for a given router model and associated issue.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Example: Recommend an assignment group for a router issue, Example configurations, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Configure a resource generator for providing assignment group as an outcome

Configure a resource generator of type decision table that provides an assignment group for a given router model and associated issue.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, sn\_nb\_action.resource\_generator\_author, admin

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Resource Generators**.

2.  Select **New** from the Resource Generators list.

3.  In the **Name** field, enter `Assignment group for router issue RG`.

4.  In the **Context** field, select Case context.

5.  In the **Generator type** field, select Decision table.

6.  In the **Generator** field, select the Assignment group for a router issue decision table.

7.  Save the record to display the generator inputs.

8.  On the Generator input form, fill in the fields.

    1.  Select the pill picker next to the field.

    2.  In the **Product** field, select **Context: Case** &gt; **Product** &gt; **Display name**.

    3.  In the **Problem** field, select **Context: Case** &gt; **Short description**.

9.  Select **Update**.


## Result

![Resource generator configuration for Assignment group for router issue RG, using a decision table with inputs for Problem (case short description) and Product (case product display name).](../image/ex-config-rg-assg-grp.png)

## What to do next

[Create a field recommendation](ex-create-field-recommendation-assg-grp.md) that you can use while creating recommended action for recommending assignment group field value.

