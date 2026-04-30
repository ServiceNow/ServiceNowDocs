---
title: Add a custom column \(field\) to an HR table
description: You can add custom columns \(fields\) to an HR table.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure an HR service, HR service configuration, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Add a custom column \(field\) to an HR table

You can add custom columns \(fields\) to an HR table.

## Before you begin

Role required: sn\_hr\_core.admin

**Note:** When adding custom columns to an HR COE table, you must create a UI policy to hide it from other HR services that use that HR COE table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the table you want to add a custom column to.

3.  Under the **Columns** tab, select **New**.

4.  Fill in the fields for the **Dictionary Entry**.

    **Note:** For more information on columns and fields, see [Field administration](https://www.servicenow.com/docs/access?context=c_IntroductionToFields&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

5.  Select **Save** or **Submit**.

    **Note:** If you added a custom column to an HR COE table, you must create a UI policy action \(**Visible** field is set to **False**\) to hide it from other HR services that use that HR COE table. For example, if you add a custom column to the HR Payroll Case \[sn\_hr\_core\_case\_payroll\] table, it appears in all HR services related to this table. The custom column appears even after you add it for a specific HR service. For more information, see [UI policies](https://www.servicenow.com/docs/access?context=t_CreateAUIPolicy&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


**Parent Topic:**[Configure an HR service](configure-hr-service.md)

