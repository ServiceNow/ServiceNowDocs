---
title: Cluster analysis configurations for ITSM work items
description: The Process Mining application provides solution definitions for incidents, problems, change requests, and requested items. You can use these definitions to configure cluster analysis for those work items.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Content pack for ITSM, Activate Process Mining content packs, Activating Process Mining, Process Mining, Platform Analytics]
---

# Cluster analysis configurations for ITSM work items

The Process Mining application provides solution definitions for incidents, problems, change requests, and requested items. You can use these definitions to configure cluster analysis for those work items.

**Important:** This feature is available with the ServiceNow Store Process Mining ITSM content pack v1.2. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Clustering solution definition configurations

A Process Mining administrator \(sn\_process\_optimization\_admin\) can access the ITSM work item solution definition configurations by navigating to **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

**Note:** By default, these solution definitions are configured as follows:

-   The **Fields** field is configured to Short description.
-   The **Minimum number of records per cluster** field is set to a value of 150.
-   The **Word Corpus** field is configured to the corresponding word corpus record, For example, the Incident clustering definition is configured to the incident word corpus record. Each of the word corpus record gathers all description and short description data for the last 12 months.

The clustering solution definitions also contain the purity fields listed in the table below.

<table id="table_ax4_nzk_2qb"><thead><tr><th>

Clustering Solution Definition

</th><th>

Purity Fields

</th></tr></thead><tbody><tr><td>

Incident

</td><td>

-   Assignment Group
-   Category
-   Configuration item
-   Service

</td></tr><tr><td>

Problem

</td><td>

-   Assignment Group
-   Category
-   Configuration item
-   CMDB CI
-   Business service

</td></tr><tr><td>

Change request

</td><td>

-   Assignment Group
-   Category
-   Model
-   Risk
-   Type

</td></tr><tr><td>

Requested item

</td><td>

-   Assignment Group
-   Category item
-   Requested for
-   Assigned to

</td></tr></tbody>
</table>For information on how to perform a cluster analysis from the Process Mining application, see [Perform a cluster analysis](../concept/cluster-analysis.md).

**Parent Topic:**[Content pack for ITSM](../concept/itsm-proc-opti-content-pack.md)

