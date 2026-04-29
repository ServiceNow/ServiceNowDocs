---
title: Default security filters
description: Generally data filters are applied after absolute ACLs \(also sometimes called table-level ACLs\), and after row-level ACLs. They are applied by default, and can be impactful to system behavior if not used carefully.
locale: en-US
release: australia
product: Data Filtration
classification: data-filtration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security data filters, Access Management]
---

# Default security filters

Generally data filters are applied after absolute ACLs \(also sometimes called table-level ACLs\), and after row-level ACLs. They are applied by default, and can be impactful to system behavior if not used carefully.

## Default applied security data filters

Security data filters are applied by default to the following places:

<table id="table_wgc_wk1_b2c"><thead><tr><th>

Category

</th><th>

Application

</th></tr></thead><tbody><tr><td>

List and Forms

</td><td>

-   UI16
-   Workspaces
-   Service Catalog
-   Service Portal
-   Mobile

</td></tr><tr><td>

Reports and Dashboards

</td><td>

-   Reports
-   Data visualizations
-   Core UI Dashboards
-   Platform Analytics experience dashboards

</td></tr><tr><td>

Data Export

</td><td>

-   Export XML
-   CSV
-   Excel
-   JSON
-   PDF

</td></tr><tr><td>

Flow Engine

</td><td>

Record Lookup steps

</td></tr><tr><td>

Search

</td><td>

-   AI Search
-   Text Search

</td></tr><tr><td>

GlideRecord

</td><td>

-   GlideRecordSecure
-   GlideRecordSandbox
-   GlideAggregateSandbox

</td></tr><tr><td>

REST and GraphQL APIs

</td><td>

-   REST table API
-   REST stats API
-   GraphQL table and stats API equivalent

</td></tr></tbody>
</table>