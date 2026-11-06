---
title: Security Assets view
description: You can review the assets that your security integrations report, with the risk rating, open findings, labels, and sources of each asset.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/sem-security-assets-page.html
release: australia
topic_type: concept
last_updated: "2026-10-16"
reading_time_minutes: 2
keywords: [Security assets, Asset inventory, Risk rating, Labels]
breadcrumb: [Security Exposure Management Workspace, Explore, Unified Security Exposure Management, Security Operations]
---

# Security Assets view

You can review the assets that your security integrations report, with the risk rating, open findings, labels, and sources of each asset.

Each asset is matched to a configuration item \(CI\) in the CMDB. The findings, remediation tasks, fixes, and vulnerabilities that you see for an asset are the ones related to that CI. An asset could be a host, a cloud resource, a container image, a virtual machine image, a domain name, or a code repository. Asset data is reported by scanners and normalized, so an asset that several scanners report appears only once.

**Note:** The Security Assets view is available only when scanner integrations are configured using the unified exposure pipeline. For information about the unified exposure pipeline, see [Unified Security Exposure Management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/integrating-usem.md).

## Opening the Security Assets page

Navigate to **Workspaces** &gt; **Security Exposure Management** and select **Security Assets**.

## Summary

You can select any of the following asset cards to display the associated list of assets:

-   All assets
-   Assets with a risk rating of Critical
-   Assets that have critical-severity findings that aren't assigned
-   Critical assets that are publicly exposed
-   Critical assets that are internet facing

## Asset list

The asset list displays the assets that match the selected card. You can sort, filter, and search through the list. For each asset, the following information is displayed:

-   Risk rating of the asset, shown in a color for each rating
-   Number of open findings for the asset, grouped by severity
-   Labels that scanners attach to the asset, such as environment or ownership tags. For more information, see [Security asset record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/sem-security-asset-record.md).
-   Integrations that report the asset

Selecting an asset in the list opens its record. For more information, see [Security asset record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/sem-security-asset-record.md).

