---
title: Enable Dynamic Translation for capabilities in Generative AI Controller
description: Use Dynamic Translation to add multiple language support for generative AI capabilities to support users who speak languages other than English.
locale: en-US
release: yokohama
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Enable Dynamic Translation for capabilities in Generative AI Controller

Use Dynamic Translation to add multiple language support for generative AI capabilities to support users who speak languages other than English.

## Before you begin

You must have the Dynamic Translation and Conversational Dynamic Translation plugins installed and enabled on your instance. For more information on setting up Dynamic Translation, see [configuring Dynamic Translation](https://www.servicenow.com/docs/access?context=configuring-dynamic-translation&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

You must have a default Translation Configuration set in the Translation Configuration table \(sn\_dt\_translator\_configuration\).

Role required: admin

## About this task

By default, Dynamic Translation is inactive for capabilities with Generative AI Controller.​

Dynamic Translation isn't available for capabilities in Virtual Agent or Now Assist panel.

## Procedure

1.  Navigate to the OneExtend Capability \(sys\_one\_extend\_capability\) table by entering `sys_one_extend_capability.list`in the navigator.

2.  Open the record for the capability that you want to enable Dynamic Translation for.

3.  In the OneExtend Capability Attributes related list, open the record for the attribute you would like to be translated, such as response.

4.  Select **Translate** to enable translation.

    If you don't see the field on the form, you must edit the form to display the **Translate**. One way of adding the field to the form is by selecting the menu icon by the table name of the form and choosing **Configure** &gt; **Form Layout**. Add the **Translate** field to the Selected list. Then, select **Save** to save the form. You're then redirected back to the record with the field available to select.

5.  Select **Submit** to save the record.


## Result

Dynamic Translation is installed for your generative AI capability on the attribute that you selected.

