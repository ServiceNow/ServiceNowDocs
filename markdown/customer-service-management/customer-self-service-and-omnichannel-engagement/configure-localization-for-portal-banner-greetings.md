---
title: Configure localization for Portal Banner heading
description: Configure the portal banner heading instance option to support localization and personalize the portal experience for different users.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Portal Banner widget, Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Configure localization for Portal Banner heading

Configure the portal banner heading instance option to support localization and personalize the portal experience for different users.

## Before you begin

Role required: sp\_admin

## About this task

The portal banner widget enables you to customize the heading text displayed to users on the business portal. You can modify the heading text from the instance options and then create a translation record in the sys\_ui\_message table. This setup lets you personalize user experience across different regions and languages.

## Procedure

1.  Configure the instance option.

    1.  Navigate to the page/portal where the widget is configured.

    2.  Press Control+right-click on the Portal Banner widget and select **Instance Options**.

    3.  In **Heading**, enter the desired text.

        For details on filling the Heading field, see [Portal Banner widget instance options form](../reference/banner-widget-inst-options.md).

2.  Create a translation record \(for localization\).

    1.  Navigate to **All** &gt; **System Localization** &gt; **Messages**.

    2.  Select **New**.

    3.  On the Message New Record form, fill in the fields.

<table id="table_zdg_5z5_chc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key

</td><td>

Exact text as configured in the instance option.

 Pass the parameters, if you have used variables in the heading field:

-   &lt;user&gt;: \{firstName\} \{lastName\}
-   &lt;title&gt;: \{title\}


</td></tr><tr><td>

Language

</td><td>

Target language

</td></tr><tr><td>

Code

</td><td>

sn\_ciwf\_ui\_cmpnt

</td></tr><tr><td>

Message

</td><td>

Translation of text entered in the Key field.

</td></tr></tbody>
</table>    4.  Select **Submit**.


## Result

A new translation record is created which supports localization.

