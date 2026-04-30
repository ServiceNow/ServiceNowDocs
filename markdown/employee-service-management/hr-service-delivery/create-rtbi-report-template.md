---
title: Create RTBI report template
description: Create a custom RTBI report template to use for the RTBI report displayed to the employee or alumni. The base system report generation uses the default template HR PII Template.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Personal Data Rights in HR Service Delivery, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create RTBI report template

Create a custom RTBI report template to use for the RTBI report displayed to the employee or alumni. The base system report generation uses the default template HR PII Template.

## Before you begin

Role required: admin

To use this template, you can create a new HR service, and record producer, then add the template in the Template field. For more information on configuring an HR service, see [Configure an HR service](configure-hr-service.md).

Verify that the following HR services are active:

-   Erasure of Personal Data
-   Request Personal Information Report

Verify the following In Record produces are active:

-   Erasure of Personal Data Request
    -   Available For - Users with 'snc\_internal' role, HRSM Alumni
    -   Not Available For - SNC External \(remove this role\).
-   Personal Information Report
    -   Available For - Users with 'snc\_internal' role, HRSM Alumni.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Data Classification** &gt; **RTBI Report Template**.

2.  Select **New**.

3.  Enter the Name and Description for the template.

4.  In the Body field, create the structure of the template.

    By default, you’ll see $\{reported\_date\} $\{target\_user\} $\{template\_script\}, where the reported date, target user, and the template script values are dynamically filled-in.

5.  In the Script field, edit the template HTML code if needed.

6.  Select **Submit**.

7.  Open the newly created template.

8.  In the RTBI Configurations related links, select the **Edit** button to add an existing RTBI configuration, or the **New** button to create a new configuration and add it.

9.  Select **Preview** to see how the report is displayed for a selected user.

10. Select **Publish** to publish the new report template.


