---
title: Map assessment template with segmentation rule
description: You can map assessment templates with segmentation rules in the Source-to-Pay workspace. A rule defines which suppliers receive assessments based on the configured criteria.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-02-22"
reading_time_minutes: 1
breadcrumb: [Configure smart assessments, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Map assessment template with segmentation rule

You can map assessment templates with segmentation rules in the Source-to-Pay workspace. A rule defines which suppliers receive assessments based on the configured criteria.

## Before you begin

Role required: sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Create a segmentation rule.

    For more information, see [Create segmentation rule](../task/create-segmentation-rule-slo.md).

3.  Select **Assessment templates** and **New** to map an assessment template with this segmentation rule.

    ![Creating assessment template from segmentation rule](../image/slo-seg-rule-assmnt-temp.png)

4.  Fill in the details in the new segmentation rule assessment template form.

    |Field|Description|
    |-----|-----------|
    |**Assessment template**|Assessment template used for mapping with the segmentation rule.|
    |**Audience type**|Type of recipients of the assessment.|
    |**Segmentation rule**|Segmentation rule for which assessment is getting created \(auto-filled\).|
    |**Due date**|Date of expiry of the assessment.|

5.  Select **Save**.


## What to do next

Trigger assessments from the segmentation rule assessment mapping templates.

**Parent Topic:**[Configure smart assessments](configure-smart-assessments.md)

