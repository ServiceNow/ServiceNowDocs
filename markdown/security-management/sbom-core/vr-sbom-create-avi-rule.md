---
title: Create an application vulnerable item rule in the Software Bill of Materials Workspace
description: Set up the conditions under which application vulnerable items \(AVITs\) are created automatically in the AVI Creation Rules module in the Software Bill of Materials \(SBOM\) Workspace.
locale: en-US
release: yokohama
product: SBOM Core
classification: sbom-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Create an application vulnerable item rule in the Software Bill of Materials Workspace

Set up the conditions under which application vulnerable items \(AVITs\) are created automatically in the AVI Creation Rules module in the Software Bill of Materials \(SBOM\) Workspace.

## Before you begin

The SBOM Response application is required if you want to create application vulnerable items. See [Exploring Software Bill of Materials](../concept/vr-sbom-exploring.md) for more information.

Role required: sn\_sbom\_resp.manage\_avi\_rule.

## Procedure

1.  Navigate to **SBOM Workspace** &gt; **AVI Creation Rules**.

2.  Select **New**.

3.  Fill out the fields.

<table id="table_kdg_gbq_xzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the rule.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the creation rule is activated.

</td></tr><tr><td>

Execution order

</td><td>

Order in which the rules are evaluated. The rule with the lowest numerical value runs first.

 For example, you might create higher priority rules for items that need special handling, or where risk is critical, so they are run first. Next, create general rules for items that require no special handling. Finally, create a default rule to catch any components that have vulnerabilities.

</td></tr><tr><td>

Description

</td><td>

Description of the rule to help you distinguish it from other rules.

</td></tr><tr><td>

Conditions

</td><td>

Create the conditions under which application vulnerable items \(AVIs\) are created.For example, you might select **\[Vulnerability &gt; Severity\]\[is\]\[1-Critical\]** to create AVITs for components that have vulnerabilities that are high-risk and might severely impact you.

Note that you can add more conditions.

</td></tr></tbody>
</table>4.  Select **Save**.

    Your creation rule runs automatically after the next upload and creates AVIs for components that match your conditions. You can also run the rule on-demand from the AVI Creation Rules module by selecting **Execute Now**.


## Result

After they are created, you can verify that an AVIT was created specifically for SBOM data by checking the values in the **Source** and **Scan type** fields on an AVI record.

|Field|Value|
|-----|-----|
|Source|SBOM|
|Scan type|SBOM-SCA|

