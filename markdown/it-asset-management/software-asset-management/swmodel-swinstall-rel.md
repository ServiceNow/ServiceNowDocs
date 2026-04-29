---
title: Software model relationship to software installation
description: Associating each software installation with a software model lets you perform audit reporting of licensable and non-licensable software.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software model relationship to software installation

Associating each software installation with a software model lets you perform audit reporting of licensable and non-licensable software.

## Overview

Software models are automatically created for licensable and non-licensable products if the following system properties are enabled:

-   **com.snc.samp.automaticsmrcreation**: for licensable products
-   **com.snc.samp.automaticsmcreation**: for non-licensable products

If the system properties are enabled and a discovery model match exists, even if the match is generic, a software model will not be created. If the system properties are not enabled, the software model is just matched to a discovery model; no software models are created.

A match is made to the most specific software model. If no specific software model exists for the discovery model, then the match is made to the most generic software model.

During the matching process, if a matching software model is found, but it has an install condition on it then it's not considered to be a match. In such a scenario, a software model is automatically created without an install condition.

For each normalized publisher and normalized product pair in the Software Discovery Model \(cmdb\_sam\_sw\_discovery\_model\) table, the scheduled job, **SAM – Discovery Model to Software Model matching**, gets all software models with matching publisher and product. If the software model has no install condition, subscription condition, or DB option, the system gets matching discovery models with normalized publisher, normalized product, normalized edition, and normalized version values. Once a match is found, the software model reference is put on the software model column in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table.

## Manually set software model

If you choose to match on a more generic software model than what the scheduled job **SAM – Discovery Model to Software Model matching** sets, you can manually set the desired software model in the form view on the Software Discovery Model \(cmdb\_sam\_sw\_discovery\_model\) table. The Automatically matched column becomes unchecked.

If a software model is set and the Automatically matched column's value is false, the scheduled job will not override the software model value on subsequent executions.

## Sample matches

The following are some sample scenarios of software model and discovery model matches.

<table id="table_akz_pyf_ltb"><thead><tr><th>

Discovery model

</th><th>

Software models

</th><th>

Matches with

</th></tr></thead><tbody><tr><td>

SQL Server 2019 Enterprise

</td><td>

-   SQL Server 2019 Enterprise
-   SQL Server 2019

</td><td>

SQL Server 2019 Enterprise software model

</td></tr><tr><td>

SQL Server 2019 Enterprise

</td><td>

-   SQL Server 2019 Enterprise with install conditions
-   SQL Server 2019 \(Edition is anything\)

</td><td>

SQL Server 2019 software model​​

</td></tr><tr><td>

SQL Server 2019

</td><td>

SQL Server 2019 with install conditions \(Edition is anything\)​

</td><td>

No match found.

 If the system property is enabled, a new software model will be created: SQL Server Enterprise \(Version is anything\)​.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

