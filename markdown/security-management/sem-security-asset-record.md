---
title: Security asset
description: A security asset record specifies the details, labels, and source data of an asset with the findings, remediation tasks, fixes, and vulnerabilities related to its configuration item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/sem-security-asset-record.html
release: australia
topic_type: concept
last_updated: "2026-10-16"
reading_time_minutes: 2
keywords: [Security asset, Asset record, Findings, Labels]
breadcrumb: [Security Assets view, Security Exposure Management Workspace, Explore, Unified Security Exposure Management, Security Operations]
---

# Security asset

A security asset record specifies the details, labels, and source data of an asset with the findings, remediation tasks, fixes, and vulnerabilities related to its configuration item.

The Findings, Remediation Tasks, Fixes, and Vulnerabilities tabs show only the records related to the configuration item \(CI\) that the asset is matched to.

## Record tabs

<table id="table-asset-record-tabs"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

Summary of an asset. Displays counts of its open findings by severity \(critical, high, medium, and low\), associated configuration item, and labels.

**Note:**

-   Before labels are updated for the asset, they're normalized and deduplicated, so a tag that several scanners report in different spellings or letter cases appears as one label. If a later scan no longer reports a label, the label stays on the asset.
-   For a code asset, the associated configuration item section is named **Associated product model** when the `sn_vul.use_product_model` system property is enabled.

</td></tr><tr><td>

Details

</td><td>

All fields recorded for the asset. A specific set of fields are recorded for each asset type. For information about these fields, see [Security asset fields for asset types in unified exposure pipeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/uep-asset-types-labels.md).

</td></tr><tr><td>

Findings

</td><td>

The findings for the asset, grouped into application findings, container findings, infrastructure findings, and misconfigurations. Only the groups that have findings for the asset appear.

 From this tab, you can bulk edit, create remediation task, and re-evaluate on the findings in each group.

</td></tr><tr><td>

Remediation Tasks

</td><td>

Remediation tasks for the configuration item of the asset, grouped by finding type. If the asset isn't matched to a configuration item, the list is empty.

</td></tr><tr><td>

Fixes

</td><td>

Fixes that address the findings for the asset, across all finding types. Fixes are deduplicated across scanners and imported after findings, so a fix can appear on this tab some time after its findings.

</td></tr><tr><td>

Vulnerabilities

</td><td>

Vulnerabilities, such as CVEs, behind the host, application, and container findings for the asset.

</td></tr></tbody>
</table>**Note:** From the contextual side panel, selecting the **Source information** tab shows the asset data that each integration reported for the asset. If no integration has reported source information for the asset, the tab shows an empty state.

## Risk scores and ratings

Each security asset shows a rolled-up risk score, a risk rating, and counts of its findings by severity. These values are calculated from the active findings that are matched to the asset's configuration item \(CI\).

The risk score is calculated using the Security Assets dashboard rollup calculator for an asset based on the following factors:

-   Highest risk score amongst the asset's active findings
-   Average risk score of those findings
-   Number of active findings

    **Note:** An asset with more active findings gets a higher risk score.


The risk rating is set from the risk score. The critical, high, medium, and low counts show the number of the asset's active findings at each severity.

**Important:** For an asset, these risk values are frequently recalculated, but updated only when a value has changed.

