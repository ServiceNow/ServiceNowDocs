---
title: Bulk-enrich assets with ServiceNow Otto
description: Ask ServiceNow Otto to bulk-enrich a batch of Data Catalog assets from anywhere in Workflow Data Fabric.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/bulk-enrich-assets-otto-dc.html
release: australia
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 1
keywords: [bulk enrichment, Otto, Data Catalog, AI metadata]
breadcrumb: [Enriching data assets with AI, Metadata enrichment with ServiceNow Otto, Data Catalog, Workflow Data Fabric]
---

# Bulk-enrich assets with ServiceNow Otto

Ask ServiceNow Otto to bulk-enrich a batch of Data Catalog assets from anywhere in Workflow Data Fabric.

## Before you begin

Role required: df\_data\_steward, now\_assist\_panel\_user, and wdf\_operator

## Procedure

1.  In the Workflow Data Fabric header, select the ServiceNow Otto icon.

    You can access this from any Workflow Data Fabric page, including Data Catalog.

    If the ServiceNow Otto icon does not appear in the Workflow Data Fabric header, Otto for Workflow Data Fabric \(sn\_nowassist\_wdf\) may not be installed.

    If the icon is visible but nothing happens when you select it, verify that your account has the **now\_assist\_panel\_user** role. Contact your administrator to request access.

    For configuration details, see [Metadata enrichment prerequisites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/ai-enrichment-prerequisites-dc.md).

2.  In the panel that opens, select the bulk-enrich promoted topic, or type a request such as `bulk enrich assets`.

3.  Choose whether to review pending suggestions from a previously submitted request, or start a new request.\[Omitted image "dc-bulk-enrich-with-ai.png"\] Alt text: Enrich data assets with AI

4.  If starting a new request, select an asset type from the list to enrich.

    ServiceNow Otto suggests asset types based on the assets available in your catalog. Use the search field to find a specific asset type.

5.  If you want to select specific assets, select **I want to select my own assets instead**.

    The Select assets to enrich page opens. Use the search field and filters to find assets, then select the assets to add to the enrichment request.

    Select **Confirm selection** to return to the panel with your selected assets queued.

6.  Select **Confirm** to submit the request.


## Result

ServiceNow Otto creates the job and returns a job ID, plus links to monitor progress and open the review workspace. See [Monitor an enrichment job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/monitor-enrichment-job-dc.md).

\[Omitted image "dc-bulk-enrich-ai-submitted.png"\] Alt text: Enrichment job submitted confirmation screen showing job ID and links

**Parent Topic:**[Enriching data assets with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/enrich-data-assets-ai-dc.md)

