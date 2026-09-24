---
title: Cluster analysis configurations for SPM work items
description: The Process Mining application provides solution definitions for demands, that you can use to configure cluster analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/cluster-analysis-configurations-for-spm-work-items.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [SPM, Automatic content pack delivery, Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Cluster analysis configurations for SPM work items

The Process Mining application provides solution definitions for demands, that you can use to configure cluster analysis.

**Important:** This feature is included with the Process Mining SPM content pack, which is delivered automatically when SPM is installed on your instance. For more information, see [Automatic delivery of content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/process-mining-content-pack-delivery.md).

## Clustering solution definition configurations

A Process Mining administrator \(sn\_process\_mining\_admin\) can access the SPM work item solution definition configurations by navigating to **All** &gt; **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

**Note:** By default, these solution definitions are configured as follows:

-   The **Fields** field is configured to description.
-   The **Minimum number of records per cluster** field is set to a value of 150.
-   The **Word Corpus** field is configured to the corresponding word corpus record, for example, the demand clustering definition is configured to the demand word corpus record. Each of the word corpus record gathers all description and short description data for the last 12 months.

The clustering solution definitions also contain the purity fields for demands, which are department, business\_unit, and priority.

**Parent Topic:**[Content pack for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/integration-with-spm.md)

