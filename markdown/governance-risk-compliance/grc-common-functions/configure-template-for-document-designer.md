---
title: Configure templates for Document Designer
description: Configure the template to specify the fields from which data must be obtained and displayed on the audit report.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure document templates using Document Designer, Microsoft Word based audit report templates using Document designer, Common GRC features, Governance, Risk, and Compliance]
---

# Configure templates for Document Designer

Configure the template to specify the fields from which data must be obtained and displayed on the audit report.

## Before you begin

Role required: sn\_grc\_doc\_design.admin and sn\_audit.admin

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Report** &gt; **Template Configurations**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the template configuration. For example, you can specify `Engagement template configuration`.|
    |Business domain|Domain from which the template is being configured. In this example, it is set to **Audit**.|
    |Table|Table on which the report is generated.|
    |Fields|Fields from which data must be displayed on the report. Move the required fields from the **Available** list to the **Selected** list.|

4.  Select **Submit**.


## What to do next

Create a data relationship path from the template configuration to go to any table that you require. For more information, see [Create data relationships](create-data-relationships.md).

