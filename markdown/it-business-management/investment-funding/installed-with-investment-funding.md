---
title: Components installed with Investment Funding
description: Several types of components are installed with activation of the Investment Funding \(sn\_invst\_pln\) plugin, including tables and user roles.
locale: en-US
release: australia
product: Investment Funding
classification: investment-funding
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install Investment Funding, Investment Funding, Strategic Portfolio Management]
---

# Components installed with Investment Funding

Several types of components are installed with activation of the Investment Funding \(sn\_invst\_pln\) plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed with Investment Funding

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Investment admin\[sn\_invst\_pln\_v2.investment\_admin\]

</td><td>

Creates investment entities and sets up preferences and fiscal calendar.

</td><td>

fiscal\_calendar\_admin

</td></tr><tr><td>

Investment planner\[sn\_invst\_pln\_v2.investment\_planner\]

</td><td>

Manages top investment, investment entities, and records associated with investment entities.

</td><td>

investment\_user

</td></tr><tr><td>

Investment user\[sn\_invst\_pln\_v2.investment\_user\]

</td><td>

Manages investments and funds.**Note:** Users with this role can perform create, read, update, and delete operations on all cost and benefit plans.

</td><td>

fiscal\_calendar\_user

</td></tr></tbody>
</table>## Tables installed with Investment Funding

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business Case\[business\_case\]

</td><td>

Stores business cases for investments.

</td></tr><tr><td>

Fund Request\[sn\_invst\_pln\_invst\_funding\_base\_request\]

</td><td>

Stores fund request details.

</td></tr><tr><td>

Funding\[sn\_invst\_pln\_invst\_funding\_base\_fund\]

</td><td>

Stores fund details.

</td></tr><tr><td>

Funding Base\[sn\_invst\_pln\_invst\_funding\_base\]

</td><td>

Base table for funding and requests.

</td></tr><tr><td>

Funding Base Breakdown\[sn\_invst\_pln\_invst\_funding\_base\_breakdown\]

</td><td>

Stores the breakdown of funding base records.

</td></tr><tr><td>

Funding Configuration\[sn\_invst\_pln\_invst\_funding\_configuration\]

</td><td>

Stores funding configuration details.

</td></tr><tr><td>

Investment Entity\[sn\_invst\_pln\_invst\_funding\_entity\]

</td><td>

Stores investment entity types.

</td></tr><tr><td>

Funding State\[sn\_invst\_pln\_invst\_funding\_state\]

</td><td>

Stores different states of a funding.

</td></tr><tr><td>

Investment\[sn\_invst\_pln\_invst\_investment\]

</td><td>

Stores investment details.

</td></tr></tbody>
</table>**Parent Topic:**[Install Investment Funding](../task/activate-investment-funding.md)

