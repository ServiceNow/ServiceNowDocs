---
title: Automated Test Framework REST properties
description: These properties are installed with ATF REST.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administering REST test step configurations, Administer, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Automated Test Framework REST properties

These properties are installed with ATF REST.

**Note:** To open the System Property \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_wqq_xcy_1z"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

glide.atf.rest.log.header\_blacklist

</td><td>

A list of headers whose content is not to be added to the log, or shown on a form. The phrase 'Header redacted for security' is saved instead.-   **Type**: String
-   **Default value**: empty
-   **Other possible values**: A comma-separated list of header names.
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.atf.rest.request\_payload\_max\_size

</td><td>

The maximum size of the request payload.-   **Type**: String
-   **Default value**: 100 Kb
-   **Maximum value**: 1024 Kb
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.atf.rest.response\_payload\_max\_size

</td><td>

The maximum size of the response payload.-   **Type**: String
-   **Default value**: 100 Kb
-   **Maximum value**: 5120 Kb
-   **Maximum value**: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Administering REST test step configurations](../concept/atf-administer-rest.md)

