---
title: Run a job to sync TRM product names in EA Workspace
description: Run a scheduled job to sync the names of Technology Reference Model \(TRM\) products with the names of their linked Software Asset Management \(SAM\) software products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-schedule-job-sync-trm-product-names.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Working with Technology Reference Model \(TRM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Run a job to sync TRM product names in EA Workspace

Run a scheduled job to sync the names of Technology Reference Model \(TRM\) products with the names of their linked Software Asset Management \(SAM\) software products.

## Before you begin

Role required: admin

## About this task

When you create a TRM product by associating it with a SAM software product, the TRM product inherits the SAM software product name at creation time. If the SAM software product name is later updated — for example, when a vendor renames a product or when the content library is updated with a corrected name — the linked TRM product name is not automatically updated. You can run this scheduled job on an ad hoc basis whenever you need to sync TRM product names with the latest SAM software product.

**Note:** SAM software products are managed in the Software Product \(samp\_sw\_product\) table, which is outside the EA Workspace. Name changes must be synced manually using this job.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the scheduled job **Sync TRM Product Names with Software Products**.

    **Note:** The scheduled job is set to run on demand and is inactive by default. If a banner appears indicating that the record is in the EA Workspace application but your current application is Global, you don't need to change the application scope. The **Execute Now** button is still available.

3.  Select **Execute Now**.


## Result

The names of TRM products of type **Software** that are linked to a SAM software product are updated to match the latest SAM software product names in the TRM Products \(sn\_apm\_trm\_standards\_product\) table. Only TRM products whose names differ from their linked SAM software product are updated; the rest are skipped.

To verify the job outcome, navigate to **All** &gt; **System Logs** &gt; **Application Logs** and search for **SyncTRMProductNames**. The log entry shows:

-   Update count: Number of TRM product names that were updated
-   Skip count: Number of TRM products skipped because their names already matched, or because the software product reference was invalid
-   Error count: Number of records that could not be updated

**Parent Topic:**[Working with Technology Reference Model \(TRM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-trm.md)

**Related topics**  


[Request a TRM product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-request-a-trm-products.md)

[Add a TRM product in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-trm-prod-lifecycle.md)

[View all TRM products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-all-trm-products.md)

[View all TRM products grouped by product category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-all-trm-products-grouped-by-product-category.md)

