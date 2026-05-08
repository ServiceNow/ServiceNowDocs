---
title: Viewing cloud assets
description: This page displays the Cloud assets view. It lists all compute assets across connected cloud providers such as AWS, Azure, GCP, and OCI along with location, cloud account, installation status, owner, discovered dates, ownership attestation, and cost center.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Viewing Cloud Account Management dashboards, Using Cloud Account Management in Cloud Workspace, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Viewing cloud assets

This page displays the Cloud assets view. It lists all compute assets across connected cloud providers such as AWS, Azure, GCP, and OCI along with location, cloud account, installation status, owner, discovered dates, ownership attestation, and cost center.

As an admin, you can access the dashboard by navigating to **All** &gt; **Cloud Workspace** &gt; **Monitor and track**

![Cloud assets](../image/cloud-assets.png "Cloud assets")

Click the respective name to view the details.

![cloud asset details](../image/cloud-asset-details.png "View cloud asset details")

In Asset Explorer, retired configuration items \(CIs\) remain in the asset table as long as they exist in the CMDB, even after retirement. To manage this, users can configure a custom retention period \(in seconds\) that automatically removes retired CIs from the asset table after the defined duration. For example, setting the property to 86,400 seconds \(1 day\) ensures that a retired CI is removed from the asset table one day after retirement, even though it may continue to exist in the CMDB. This helps improve performance for high-volume environments by ensuring that only active CIs remain in the asset table.

For more information about the various sections, see [Managing the Cloud Account Management cloud asset details](manage-cam-ci-details.md).

