---
title: Cluster analysis configurations for SPM work items
description: The Process Mining application provides solution definitions for demands, that you can use to configure cluster analysis.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Content pack for SPM, Activate Process Mining content packs, Activating Process Mining, Process Mining, Platform Analytics]
---

# Cluster analysis configurations for SPM work items

The Process Mining application provides solution definitions for demands, that you can use to configure cluster analysis.

**Important:** This feature is available with the ServiceNow Store Process Mining SPM content pack v1.0. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Clustering solution definition configurations

A Process Mining administrator \(sn\_process\_optimization\_admin\) can access the SPM work item solution definition configurations by navigating to **All** &gt; **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

**Note:** By default, these solution definitions are configured as follows:

-   The **Fields** field is configured to description.
-   The **Minimum number of records per cluster** field is set to a value of 150.
-   The **Word Corpus** field is configured to the corresponding word corpus record, For example, the demand clustering definition is configured to the demand word corpus record. Each of the word corpus record gathers all description and short description data for the last 12 months.

The clustering solution definitions also contain the purity fields for demands, which are department, business\_unit, and priority.

**Parent Topic:**[Content pack for SPM](integration-with-spm.md)

