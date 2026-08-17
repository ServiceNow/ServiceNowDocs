---
title: Get started with CMDB success advisor setup for SAM
description: Set up your Software Asset Management \(SAM\) specific advisor dashboard by selecting software products to define the SAM advisor scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/cmdb-sa-sam-get-started.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-07-22"
reading_time_minutes: 2
keywords: [SAM advisor dashboard setup, select software products, SAM advisor scope, Edit dashboard scope dialog box, software product selection]
breadcrumb: [Set up advisor, Use SAM advisor, Software Asset Management, IT Asset Management, Asset Management]
---

# Get started with CMDB success advisor setup for SAM

Set up your Software Asset Management \(SAM\) specific advisor dashboard by selecting software products to define the SAM advisor scope.

## Before you begin

Role required: sam\_admin or sn\_cmdb\_admin

## About this task

Selecting software products defines which software the CMDB success advisor monitors for SAM data quality. Only licensable software products that are flagged for reporting are available for selection. The selected products determine the scope of the SAM advisor dashboard, including the KPIs that are tracked.

## Procedure

1.  On the CMDB success advisor landing page, select **Select software products** within the SAM card.

    See [Viewing the CMDB success advisor landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-sa-landing-page.md).

2.  In the Edit dashboard scope dialog box, use the **Search** field to find a software publisher or product.

    You can also select **Expand** next to a publisher to view its available software products.

3.  Select software products to add to your SAM advisor scope.

    |Action|Result|
    |------|------|
    |Select **Select all** for an expanded publisher.|Adds every available software product for that publisher to your selection.|
    |Select the check box next to an individual software product.|Adds that software product to your selection.|
    |Select **Remove** next to a product in the selected products list.|Removes that software product from your selection.|

    **Note:** Only software products with a licensable product type that are flagged for reporting are available for selection. Publishers with no qualifying software products aren't shown. You can select up to 200 software products by default.

4.  Select **Save** to build the CMDB success advisor for SAM dashboard.

    **Note:** **Save** is disabled if you deselect all software products.


## Result

The SAM data collection begins immediately via the **CMDB Advisor - SAM Daily Data Collection** scheduled job. Your first set of dashboard metrics doesn't wait for a scheduled cycle. The SAM advisor dashboard is populated after this initial data collection completes. The scheduled job then continues running on a daily basis. Until this initial data collection completes, dashboard cards indicate that no data is available and let you refresh to check again.

Once initial data collection completes, you receive a notification indicating that insights for the software products in your SAM advisor scope are ready for review.

To update the scope after initial setup, select **Edit dashboard scope** on the SAM advisor dashboard. See [Manage SAM advisor scope in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/cmdb-sa-sam-optimize-dashboard.md).

