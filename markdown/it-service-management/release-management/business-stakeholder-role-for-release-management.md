---
title: Business stakeholder role for Release Management
description: Use the business stakeholder role to read and retrieve data from any table of the Release Management application to generate reports.
locale: en-US
release: australia
product: Release Management
classification: release-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Release Management, IT Service Management]
---

# Business stakeholder role for Release Management

Use the business stakeholder role to read and retrieve data from any table of the Release Management application to generate reports.

When you activate the Business Stakeholder plugin \(com.snc.business\_stakeholder\) in your ServiceNow instance, the Read only roles for Release Management plugin \(com.snc.release\_management\_read\_roles\) is also activated. This plugin provides a business stakeholder role \(sn\_release\_read\) with which you can access all the tables of the Release Management application. You can assign this role to any user in your organization who is a business stakeholder.

## Plugin availability

If you are a new customer, the Read only roles for Release Management plugin \(com.snc.release\_management\_read\_roles\) is activated on zBoot. However, the business stakeholder role \(sn\_release\_read\) is available only when you activate the Release Management plugin \(com.snc.release\_management\_read\_roles\).

If you are an upgrade customer, you must manually activate the read-only roles for Release Management plugin and the Release Management plugin \(com.snc.release\_management\_v2\).

## Release Management tables accessible by users with the business stakeholder role

When the Read only roles for Release Management plugin \(com.snc.release\_management\_v2\) is active in your ServiceNow instance, the user with the business stakeholder role \(sn\_release\_read\) has read access to the following tables.

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product \[rm\_product\]

</td><td>

Represent whole products whose releases are being managed.It is optional to use the Product construct. A generic release can also be defined without any specific product.

</td></tr><tr><td>

Release \[rm\_release\]

</td><td>

Represent individual releases of the product.

</td></tr><tr><td>

Release Phase \[rm\_release\_phase\]

</td><td>

Represent the different stages of work required to complete a release.

</td></tr><tr><td>

Release Tasks \[rm\_task\]

</td><td>

Represent tasks under a phase for phase activities.

</td></tr><tr><td>

Release Items \[rm\_m2m\_release\_task\]

</td><td>

Represents work items and change records associated to the release.

</td></tr></tbody>
</table>**Parent Topic:**[Release Management](../concept/c_ITILReleaseManagement.md)

