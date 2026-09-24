---
title: Configure a Primary change model
description: Configure a Primary change model so that a change using this model generates one Child change for each affected configuration item \(CI\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/create-a-primary-change-model.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Primary change model, Scaled change model, scaled change]
breadcrumb: [Scaled change, Configure, Change Management, IT Service Management]
---

# Configure a Primary change model

Configure a Primary change model so that a change using this model generates one Child change for each affected configuration item \(CI\).

## Before you begin

-   Activate the Major Change \(**com.sn\_major\_change**\) plugin. For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateAPlugin.md).
-   Create a base change model to configure as the Primary change model. For more information, see [Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-change-model.md).

Role required:`sn_change_write or itil`

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Models** and open the change model to configure as the Primary change model.

2.  Open the state record on which you want Child changes to be created, for example open the **Assess** state.

    On the **Attributes** tab, add the **Allow Child Change Creation** attribute with **Active** selected. Without this attribute, Child changes are not created when the Primary change enters that state.

3.  Select **Submit**.


## Result

The Primary change model is available for selection on new change requests. When a change using this model enters the configured state, the flow you configure in [Create a scaled change flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-scaled-change-flow.md) generates one Child change for each CI in the **Affected CIs** related list.

## What to do next

Create a Child change model for the Child changes that this Primary change model generates. Fore more information, see [Configure a Child change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-child-change-model.md).

**Parent Topic:**[Scaled change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/scaled-change-overview.md)

