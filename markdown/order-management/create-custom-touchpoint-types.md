---
title: Create custom touchpoint types
description: Create touchpoint types in Activity Management tailored to your sales organization's workflow to capture activities beyond the standard Discovery, Demo, and CBR types.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activity Management, Lead and opportunity management apps, Configure, Sales Customer Relationship Management]
---

# Create custom touchpoint types

Create touchpoint types in Activity Management tailored to your sales organization's workflow to capture activities beyond the standard Discovery, Demo, and CBR types.

## Before you begin

Role required: sn\_crm\_touchpoint.admin

## About this task

Several touchpoint types are available by default. To view the available options, see [Create new CRM touchpoint form](../reference/create-crm-touchpoint-form.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  In the **Label** search field, enter `CRM Touchpoint` and select the **CRM Touchpoint** \[sn\_crm\_touchpoint\_touchpoint\] table.

3.  In the **Column label** search field, enter `Subcategory` and select the record.

4.  If a message appears about the application scope, select **here** to be able to edit the record.

5.  Navigate to the **Choices** tab under Related Links.

6.  Select **New**.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|User‑visible name for the type shown in the Type drop-down menu on the CRM Touchpoints form. For example, Business Value Assessment \(BVA\).|
    |Value|Internal value stored in the database when a choice is selected.|

8.  Select **Submit**.


