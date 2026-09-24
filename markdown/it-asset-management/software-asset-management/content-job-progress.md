---
title: Monitoring content job progress
description: Track the first-time run of the content jobs that load the Software Asset Management Content Service data into your instance. View job status and completion details to confirm that the initial download completed and that delta runs are current.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/content-job-progress.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure SAM using Configuration Console, Configuration Console for Software Asset Management, Software Asset Management installation methods, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Monitoring content job progress

Track the first-time run of the content jobs that load the Software Asset Management Content Service data into your instance. View job status and completion details to confirm that the initial download completed and that delta runs are current.

**Note:** Access to the Content job progress module requires the cds\_client\_admin role.

## About content jobs

Content jobs download software content from the ServiceNow® Content Service into your instance. This content includes publishers, products, versions, discovery models, normalization rules, product lifecycles, subscription product definitions, and related reference data. Software Asset Management uses this content to normalize discovered software, identify products, and support licensing and reconciliation.

When you configure the Software Asset Management application for the first time in the Configuration Console, the system schedules Software Asset Management specific content jobs. These jobs run a full pull of the Software Asset Management Content Service to populate your instance. After the first run completes, these jobs run twice a week to pull delta updates. Delta runs make new and updated content available in your instance.

Content job records are stored in the Data Services Schedule \[cds\_client\_schedule\] table.

## What the page shows

The Content job progress page has two areas:

-   **List view**

    Displays each content job with its target table, order, last updated timestamp, and run frequency. The list view reflects the status of both the first-time run and subsequent delta runs.

-   **Job status panel**

    Displays the progress of the first-time run only, grouped under **Completed** and **Scheduled** tabs. As each job finishes the first-time run, it moves from **Scheduled** to **Completed**. The panel does not refresh for delta runs. To review delta run status, use the list view.


## When to use this page

-   Confirm that the initial content download completed after setting up the Software Asset Management application.
-   Review the last updated timestamp for a specific content job to verify that delta runs are current.
-   Identify a content job that has not run as expected before contacting support.

**Parent Topic:**[Configure Software Asset Management using the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-sam-from-config-console.md)

**Related topics**  


[Content updates for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sam-content-updates.md)

