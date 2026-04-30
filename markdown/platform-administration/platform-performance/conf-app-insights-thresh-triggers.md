---
title: Configure Application Insights threshold triggers
description: Detect that a threshold has been exceeded and create a trigger to perform a sequence of actions.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Configure Application Insights threshold triggers

Detect that a threshold has been exceeded and create a trigger to perform a sequence of actions.

## Before you begin

Role required: sn\_app\_insights.admin or admin

## About this task

Application Insights uses the ServiceNow® Workflow Studio to create the trigger and action. You can configure one flow per threshold. You can use any of the actions available in the Workflow Studio and the spokes from Integration Hub. This example configures a trigger to send an email.

## Procedure

1.  Navigate to **All** &gt; **Application Insights** &gt; **Application Insights**.

2.  Select **Thresholds**.

3.  Select an existing threshold from the Thresholds list.

4.  From the ellipses, select **Create flow**.

    The Workflow Studio opens. The system automatically populates a base template with a trigger and three actions.

    Modify the base template to fit your needs.

    For more information about using the Workflow Studio, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

5.  Select **Send Email**.

6.  In the To, CC, and BCC lines, enter the email addresses that you want to send the notification to.

7.  In the **Subject** and **Body** fields, enter the text that you want.

8.  Select **Done**.

9.  Select **Save**.

10. To activate the trigger, select **Activate**.

11. To edit an existing trigger:

    1.  Select **Thresholds**.

    2.  From the Thresholds list, select an existing threshold.

    3.  From the ellipses, select **Edit flow**.

    4.  Change the settings.

    5.  Select **Save**.


**Parent Topic:**[Application Insights](../concept/application-insights.md)

