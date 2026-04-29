---
title: Components Installed with Quote Management
description: Several types of components are installed with activation of the Quote Management plugin, including user roles.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, price, quote, Reference, Sales and Order Management]
---

# Components Installed with Quote Management

Several types of components are installed with activation of the Quote Management plugin, including user roles.

## Roles installed

<table id="table_rt5_bzl_nhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Quote responsibility read granular \[sn\_quote\_mgmt\_core.quote\_responsibility\_read\_granular\]

</td><td>

Provides granular read access to quote and related entities through the responsibility framework.

</td><td>

None

</td></tr><tr><td>

Quote responsibility write granular \[sn\_quote\_mgmt\_core.quote\_responsibility\_write\_granular\]

</td><td>

Provides granular write access to quote and related entities through the responsibility framework.

</td><td>

sn\_quote\_mgmt\_core.quote\_responsibility\_read\_granular

</td></tr><tr><td>

Quote integrator \[sn\_quote\_mgmt\_core.quote\_integrator\]

</td><td>

Role required to access quote features when using the advanced configurator.

</td><td>

sn\_quote\_mgmt\_core.quote\_writer

</td></tr><tr><td>

Quote admin \[sn\_quote\_mgmt\_core.quote\_admin\]

</td><td>

A granular role created to give create, update, read, or delete access on quote tables.

</td><td>

sn\_quote\_mgmt\_core.quote\_writer

</td></tr><tr><td>

Quote writer \[sn\_quote\_mgmt\_core.quote\_writer\]

</td><td>

A granular role created to give write access to quote tables.

</td><td>

-   sn\_quote\_mgmt\_core.quote\_viewer
-   sn\_nb\_action.next\_best\_action\_user
-   sn\_doc.reader

</td></tr><tr><td>

Quote viewer \[sn\_quote\_mgmt\_core.quote\_viewer\]

</td><td>

A granular role created to give read access to quote tables.

</td><td>

-   sn\_bus\_loc.ibl\_viewer
-   sn\_service\_org.customer\_criteria\_read
-   sn\_bus\_loc.ebl\_viewer
-   sn\_csm\_pricing.pricelist\_viewer
-   sn\_tmt\_core.inbound\_queue\_read
-   sn\_prd\_invt.product\_inventory\_viewer
-   sn\_customerservice.customer\_data\_viewer

</td></tr></tbody>
</table>**Parent Topic:**[Configure, price, quote reference](../concept/reference-cpq.md)

