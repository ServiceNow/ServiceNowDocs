---
title: Components installed with Legal Stock Preclearance
description: Several types of components are installed with activation of the Legal Stock Preclearance application, including tables and user roles.
locale: en-US
release: australia
product: Legal Stock Preclearance
classification: legal-stock-preclearance
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Legal Stock Preclearance, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Legal Stock Preclearance

Several types of components are installed with activation of the Legal Stock Preclearance application, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Stock Preclearance Administrator\[sn\_lg\_stock\_cp. stock\_config\]

</td><td>

Provides access to set up stock preclearance data such as trading windows, holidays, and access persons.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr></tbody>
</table>## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Access Persons\[sn\_lg\_stock\_cp\_access\_person\]

</td><td>

Stores users designated as Access Persons to submit a stock preclearance request.

</td></tr><tr><td>

Calendar year\[sn\_lg\_stock\_cp\_trading\_year\]

</td><td>

Stores calendar years used for setting up trading holidays for your organization during which no trading in securities is permitted.

</td></tr><tr><td>

Holiday\[sn\_lg\_stock\_cp\_trading\_holiday\]

</td><td>

Stores the stock exchange trading holidays for your organization.

</td></tr><tr><td>

Trading Window\[sn\_lg\_stock\_cp\_trading\_window\]

</td><td>

Stores the trading window details for stock preclearance requests.

</td></tr><tr><td>

Trading Window Requests\[sn\_lg\_stock\_cp\_trading\_window\_request\]

</td><td>

Stores the trading window requests for stock preclearance requests.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Stock Preclearance reference](legal-stock-pre-reference.md)

