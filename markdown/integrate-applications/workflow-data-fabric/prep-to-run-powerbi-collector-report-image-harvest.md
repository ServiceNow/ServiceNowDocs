---
title: Configure Power BI report image harvesting
description: Enable report image harvesting to collect preview images from Power BI reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-report-image-harvest.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Prepare to run the PowerBI collector, PowerBI metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Configure Power BI report image harvesting

Enable report image harvesting to collect preview images from Power BI reports.

## Before you begin

Role required: admin

**Note:** Report image harvesting isn’t supported for Power BI Apps.

## About this task

Enable report image harvesting to collect preview images from Power BI reports for display in the Data Catalog.

## Procedure

1.  Enable the export setting in the Power BI Admin Portal.

    1.  Sign in to Power BI using a Power BI Admin account.

    2.  Navigate to **Settings** &gt; **Admin Portal**.

    3.  Locate and enable the **Export reports as image files** setting from the [Admin settings](https://learn.microsoft.com/en-us/power-bi/developer/embedded/export-to#using-the-api).

2.  Verify workspace capacity.

    Confirm that the reports to be exported are located in a workspace with Premium, Embedded, or Fabric capacity. For details, see the [Power BI documentation](https://learn.microsoft.com/en-us/power-bi/enterprise/service-premium-what-is).


**Parent Topic:**[Prepare to run the PowerBI collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector.md)

