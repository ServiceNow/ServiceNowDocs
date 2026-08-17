---
title: Improve the accuracy of AI reporting assistant results
description: Improve the accuracy of AI reporting assistant results when querying ServiceNow instance data by configuring knowledge graph tags. Knowledge graph tags provide table-level and column-level instructions that the AI reporting assistant uses internally when querying ServiceNow instance data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/configure-knowledge-graph-tags-for-ai-reporting-assistant.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [AI reporting assistant, Microsoft Word based audit report templates using Document designer, Common GRC features, Governance, Risk, and Compliance]
---

# Improve the accuracy of AI reporting assistant results

Improve the accuracy of AI reporting assistant results when querying ServiceNow instance data by configuring knowledge graph tags. Knowledge graph tags provide table-level and column-level instructions that the AI reporting assistant uses internally when querying ServiceNow instance data.

## Before you begin

A business domain and at least one knowledge graph tag must be available.

-   To create a business domain, see [Create a business domain](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/create-a-business-domain.md).
-   To create a knowledge graph tag, see [Create Knowledge Graph tag](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-knowledge-graph-tags.md).

Role required: sn\_grc\_doc\_design.admin

## Procedure

1.  In the filter navigator, enter `sn_doc_design_ai_reporting_config.LIST`.

2.  In the AI reporting configuration page, select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Business domain|Business domain associated with the knowledge graph tags.|
    |Knowledge graph tags|Knowledge graph tags associated with the business domain to improve AI reporting assistant query accuracy.|
    |Active|Option to activate the configuration.|

4.  Select **Submit**.


## What to do next

[Generate reports through the AI reporting assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/use-the-ai-reporting-assistant.md).

**Parent Topic:**[AI reporting assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/ai-reporting-assistant.md)

