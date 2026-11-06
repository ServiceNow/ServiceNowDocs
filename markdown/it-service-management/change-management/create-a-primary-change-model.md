---
title: Configure a Primary change model
description: Configure a Primary change model so that a change using this model generates one Child change for each affected configuration item \(CI\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/create-a-primary-change-model.html
release: australia
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

-   The Major Change plugin \(com.sn\_major\_change\) must be active. For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).
-   A base change model to configure as the Primary change model must exist. For more information, see [Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-a-change-model.md).

Role required: sn\_change\_write or itil

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Models** and open the change model to configure as the Primary change model.

2.  Open the state record in which Child changes are created, for example, the **Assess** state.

    On the **Attributes** tab, add the **Allow Child Change Creation** attribute with **Active** selected. Without this attribute, Child changes are not created when the Primary change enters that state.

3.  Select **Submit**.


## Result

The Primary change model is available for selection on new change requests. When a change using this model enters the configured state, the flow you configure in [Create a scaled change flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-a-scaled-change-flow.md) generates one Child change for each CI in the **Affected CIs** related list.

## What to do next

Create a Child change model for the Child changes that this Primary change model generates. For more information, see [Configure a Child change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-a-child-change-model.md).

**Parent Topic:**[Scaled change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/scaled-change-overview.md)

