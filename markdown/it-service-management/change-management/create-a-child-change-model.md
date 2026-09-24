---
title: Configure a Child change model
description: Configure a Child change model to define the states required by the Child change requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/create-a-child-change-model.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Child change model, Minor model, scaled change]
breadcrumb: [Scaled change, Configure, Change Management, IT Service Management]
---

# Configure a Child change model

Configure a Child change model to define the states required by the Child change requests.

## Before you begin

Role required: `sn_change_write or itil`.

-   Activate the Major Change \(**com.sn\_major\_change**\) plugin. For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateAPlugin.md).
-   Create a base change model to use as the Child change model. See [Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-change-model.md).

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Models** and open the change model to configure as the Child change model.

2.  Select **Submit**.


## Result

The Child change model is available for use by a Primary change model's flow.

## What to do next

Create a flow on the Primary change model, and add the `Child change requests creation` action, and set its change model input to your Child change model. For more information, see [Create a scaled change flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-scaled-change-flow.md).

**Parent Topic:**[Scaled change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/scaled-change-overview.md)

