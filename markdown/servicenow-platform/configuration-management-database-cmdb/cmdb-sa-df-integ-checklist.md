---
title: Data integration checklist for Data Foundations in CMDB success advisor
description: Use the data integration checklist to verify that Discovery patterns and Service Graph Connectors are correctly configured and actively contributing to your Configuration Management Database \(CMDB\), promoting quality foundational data.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Analyze data integrations, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data integration checklist for Data Foundations in CMDB success advisor

Use the data integration checklist to verify that Discovery patterns and Service Graph Connectors are correctly configured and actively contributing to your Configuration Management Database \(CMDB\), promoting quality foundational data.

## Discovery patterns checklist

Confirm each Discovery pattern is enabled and effectively populating attributes for your principal classes.

<table id="table_zwd_2zm_k3c"><thead><tr><th>

Select

</th><th>

Check item \(field\)

</th><th>

Description

</th><th>

Action

</th></tr></thead><tbody><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Pattern name

</td><td>

Name of the discovery pattern contributing CI data for Data Foundations.

</td><td>

Confirm that the pattern is relevant for your principal classes.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Status

</td><td>

Current state of the pattern as active or inactive. Only active patterns contribute data.

</td><td>

Verify that the pattern is active with Status set to Active to confirm it’s contributing data.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Attribute coverage

</td><td>

Number of CI attributes populated by the pattern.

</td><td>

Check how many relevant CI attributes are populated for each principal class.**Note:** Low attribute coverage may suggest shallow discovery or misaligned pattern logic.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Suggested version

</td><td>

Latest suggested version for optimal attribute coverage.

</td><td>

Plan and perform an upgrade to the suggested version or higher to improve coverage.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Installed version

</td><td>

Version currently in use in your instance.

</td><td>

Compare with the suggested version and upgrade if necessary.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

View pattern

</td><td>

Link to inspect the pattern configuration.

</td><td>

Select the link to review or modify the pattern logic.

</td></tr></tbody>
</table>## Service Graph Connectors checklist

Confirm Service Graph Connectors are installed and actively contributing hardware data.

<table id="table_lbw_cj2_ggc"><thead><tr><th>

Select

</th><th>

Check item \(field\)

</th><th>

Description

</th><th>

Action

</th></tr></thead><tbody><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Connector name

</td><td>

Name of the Service Graph Connector providing CI data for Data Foundations.

</td><td>

Confirm that the Service Graph Connector is required for your principal classes.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Status

</td><td>

Current state of the Service Graph Connector as active or inactive.

</td><td>

Activate Service Graph Connectors that are needed for Data Foundations but currently inactive.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Attribute coverage

</td><td>

Number of hardware attributes populated by the Service Graph Connector.

</td><td>

Check how many relevant CI attributes are being populated for each principal class.**Note:** Low coverage may indicate incomplete mappings or missing source data.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Suggested version

</td><td>

Latest suggested version for optimal attribute coverage.

</td><td>

Plan and perform an upgrade to the suggested version or higher to improve coverage.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Installed version

</td><td>

Version currently in use in your instance.

</td><td>

Compare with the suggested version and upgrade if necessary.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Active connections

</td><td>

Number of active connections.

</td><td>

Confirm that at least one connection is actively importing data per principal class.

</td></tr><tr><td>

![](../../../reuse/icons/product-icons/square-outline-24.svg)

</td><td>

Inactive connections

</td><td>

Number of inactive connections.

</td><td>

Review and troubleshoot any configured connections that aren’t currently active.

</td></tr></tbody>
</table>## Optional checks for Discovery patterns and Service Graph Connectors

|Select|Check item|Description|Action|
|------|----------|-----------|------|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|No entitlements warning|Discovery patterns or Service Graph Connectors tile showing no entitlements, indicating missing access or licensing.|Verify licensing and entitlements with your administrator.|
|![](../../../reuse/icons/product-icons/square-outline-24.svg)|Suggested integrations reviewed|Some Discovery patterns are listed as suggestions because they aren’t installed or active, and some Discovery patterns are listed but are not actively used.|Evaluate business need and consider implementing high-value suggested integrations.|

## Final validation

Once all data integration checks are complete:

-   Discovery patterns relevant to your principal classes are active.
-   At least one Service Graph Connector is active for each principal CI class in your DF scope.
-   Attribute coverage across integrations supports your Data Foundations outcome.
-   Integrations are populating ownership, relationship, and key infrastructure attributes.
-   CMDB records for principal classes are accurate and complete.

