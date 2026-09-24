---
title: Create a custom deduplication rule
description: Create a custom deduplication rule to define how duplicate software installations are identified and matched within your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/configure-custom-deduplication-rule.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [deduplication rule]
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management, Asset Management]
---

# Create a custom deduplication rule

Create a custom deduplication rule to define how duplicate software installations are identified and matched within your organization.

## Before you begin

Role required: sam\_admin

## About this task

Deduplication rules compare version numbers across installation records on the same device and determine which installation record is retained as primary. Create a custom deduplication rule to identify duplicate installation records on a device when the default **Major** version comparison doesn't match your organization's duplicate detection requirements. The Software Asset Management application uses this custom rule to match installations of the specified product according to your selected version comparison level. Duplicate installations matching this rule are grouped together, and the Software Asset Management application selects a primary installation based on discovery source reliability and data completeness.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **Administration** &gt; **Deduplication rules**.

2.  Select **New**.

3.  On the Create New Custom Deduplication form, fill in the fields.

<table id="table_rz1_r35_zjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product

</td><td>

The product name to which this rule applies. The rule only matches installations of the selected product.

</td></tr><tr><td>

Active

</td><td>

The option that indicates whether the deduplication rule is active.

</td></tr><tr><td>

Version Level

</td><td>

The version-matching levels that control how strictly the system compares version numbers when identifying duplicates: -   **Major version**: Installs with matching major versions are considered duplicates regardless of minor version differences. For example, versions 19.1 and 19.2 of the same product on the same device are treated as duplicates. Installs with unparseable version strings are skipped and not deduplicated at this level.
-   **Exact version**: Installs are considered duplicates only if their normalized version and normalized edition match exactly. This is the most conservative level. Use for products where minor version differences represent distinct deployments that must be tracked separately for compliance.
-   **Any**: Only one install per product and edition combination is kept per device, regardless of version. This is the most aggressive level. Use for products where any version on a device counts as a single installation for compliance purposes.


</td></tr><tr><td>

Stale Record Threshold \(Days\)

</td><td>

Number of days after which an unrefreshed record is considered stale.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

-   The deduplication rule record starts showing in the Deduplication rules list.
-   The deduplication rule record is stored in the Custom Deduplication Rules \[sam\_sw\_dedup\_rule\] table.

**Parent Topic:**[Using Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/using-sam-workspace.md)

**Related topics**  


[Software install deduplication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/deduplication-rule.md)

