---
title: Fetch UCM content updates manually
description: Manually fetch the latest Unified Content Management \(UCM\) content from the Continuance Delivery System \(CDS\) to bring new content and updates to your content library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/grc-common-functions/fetch-ucm-update-manual.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [UCM, content sync, Content Delivery Service, CDS]
breadcrumb: [Unified Content Management \(UCM\), Common GRC features, Governance, Risk, and Compliance]
---

# Fetch UCM content updates manually

Manually fetch the latest Unified Content Management \(UCM\) content from the Continuance Delivery System \(CDS\) to bring new content and updates to your content library.

## Before you begin

Unified Content Management \(sn\_esg\_content\) must be installed. For information on the respective plugins for your application, see [Unified Content Management \(UCM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/grc-common-functions/ucm-shared-architecture.md).

Role required: system administrator

## About this task

CDS delivers regulatory content and assessment templates to your instance separately from application releases. Scheduled jobs add this content to the content library once a month. Run the jobs yourself for your respective products when you need updated content before the next scheduled sync.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  To find the UCM jobs, filter by Application for Unified Content Management.

    You can choose from the following scheduled jobs depending on your application:

    |Application|Scheduled Job|
    |-----------|-------------|
    |**Policy and Compliance Management**|**Load Compliance UCM data**|
    |**Operational Sustainability Management**|**Load OSM UCM data**|
    |**Privacy Management Content**|**Load Privacy UCM data**|
    |**AI Risk and Compliance Content**|**Load AI risk and compliance UCM data**|
    |**Third-party Risk Management**|**Load TPRM UCM data**|

3.  To pull the latest content from CDS, open the load job for your application and select **Execute Now**.

4.  To add the content to the content library, open the **Sync data from ucm cds client pre-staging to staging table** job and select **Execute Now**.

    **Note:** Run Step 4 after the load jobs in the previous step finish. The load jobs retrieve the content, and this job makes it available in the content library.


## Result

New content and versions appear in the UCM home page of your application's workspace, where you can activate or update them.

**Parent Topic:**[Unified Content Management \(UCM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/grc-common-functions/ucm-shared-architecture.md)

