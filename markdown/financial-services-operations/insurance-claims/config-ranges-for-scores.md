---
title: Configure the fraud score ranges with UI Builder
description: Configure the fraud score ranges by using the UI Builder. You can configure certain fields, such as the Ranges field, in the fraud information page of the CSM Configurable Workspace, so that you can set the score range.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generate and view a claim's fraud score, Use, Commercial Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Configure the fraud score ranges with UI Builder

Configure the fraud score ranges by using the UI Builder. You can configure certain fields, such as the **Ranges** field, in the fraud information page of the CSM Configurable Workspace, so that you can set the score range.

## Before you begin

Role required: admin

## About this task

**Note:** Any configuration changes made here appears at the Financial Services Operations Core level and will apply to all FSO Core applications.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder** &gt; **Page collections**.

2.  **CSM default record post-Details** &gt; **Fraud score** &gt; **Default**

3.  If a `Different application scope` message appears, select **Edit in original scope**.

4.  Set the minimum and maximum value on the configuration panel's **Config** tab by selecting **Ranges**.

5.  Set the value, color, and label by selecting **Configure Ranges**.

6.  Select **Apply**.

    By configuring the gauge, you can display the position of a particular value within a given range of minimum and maximum values. You can also see the progress by setting the color-coded data ranges. For more details on the gauge configuration, see the [ServiceNow® Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/utah/now-components/now-vis-gauge-wrapper/uib-setup).


**Related topics**  


[bundle-csm.csm-config-workspace-record-pages]

