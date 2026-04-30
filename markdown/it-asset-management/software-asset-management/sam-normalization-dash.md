---
title: Normalization and Content Service dashboard
description: View normalization trend charts on the Normalization and Content Service dashboard integrated with Performance Analytics.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Platform Analytics Solution for Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Normalization and Content Service dashboard

View normalization trend charts on the Normalization and Content Service dashboard integrated with Performance Analytics.

**Note:** The Normalization and Content Service dashboard is no longer available for new Zurich users who have activated the Software Asset Management Professional \(com.snc.samp\) plugin or upgraded to Zurich without activating the Software Asset Management Professional \(com.snc.samp\) plugin prior to Zurich.

-   If you activated the Software Asset Management Professional \(com.snc.samp\) plugin prior to Zurich but didn't activate the Workspace plugin \(com.sn\_sam\_workspace\), you have access to this dashboard.
-   If you activated the Software Asset Workspace \(sn\_sam\_workspace\) store application after upgrading to Zurich, you won’t be able to access this dashboard from the **Software Asset** navigation menu in your instance. You can however access this dashboard from the **Dashboards** navigation menu.

The Normalization and Content Service dashboard tab is accessed by navigating to **Software Asset** &gt; **Overview** and selecting **Normalization and Content Service** from the dashboard list. You can also access it from the dashboard list of another Software Asset Management dashboard. Select an element within a report to see more information, or add and move widgets as needed.

Normalization chart results are updated daily when the **SAM — Discovery Model Normalization** job is run. You can save charts in PNG or JPG formats.

![SAMNormalizationDashboard](../image/sam-normalization-dash.png "Normalization and Content Service dashboard")

|Report|Source list|Description|
|------|-----------|-----------|
|Overall Normalization Rates for Licensable Software|Software Installs Normalization Rates|Overall normalization status count for all licensable products.|
|Normalization Rate Breakdown for Top Publishers|Software Install Normalization Rates for Top Publishers|Licensable normalization status count per top publisher for Microsoft, Oracle, IBM, VMware, Citrix, SAP, and Adobe.|

## Central Data Service Download Status related list

The Central Data Service Download Status related list is updated daily when the **SAM — Central Data Service Download Status** job is run.

![SAMNormDashStatus](../image/sam-norm-dash-cds.png "Central Data Service Download Status related list")

|Field|Description|
|-----|-----------|
|Name|Table name from which content is pulled.|
|Current count|Number of records in the table.|
|Expected count|Expected number of records in the table.|
|Last updated on|Last date and time the data was pulled.|
|Next action|Next scheduled date and time to pull data.|

**Parent Topic:**[Platform Analytics Solution for Software Asset Management classic](../../../use/dashboards/application-content-packs/software-asset-mgmt-content-pack.md)

