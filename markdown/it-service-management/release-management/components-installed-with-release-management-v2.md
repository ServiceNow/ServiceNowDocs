---
title: Components installed with Release Management
description: Several types of components are installed with activation of the Release Management v2 plugin, including tables and user roles.
locale: en-US
release: yokohama
product: Release Management
classification: release-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Release Management, IT Service Management]
---

# Components installed with Release Management

Several types of components are installed with activation of the Release Management v2 plugin, including tables and user roles.

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Release admin

 \[release\_v2\_admin\]

</td><td>

Can access the entire application

</td><td>

release\_v2\_user

</td></tr><tr><td>

Release user

 \[release\_v2\_user\]

</td><td>

Can access the all the various feature and task-related modules but cannot update any content.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

The Release Management v2 application contains with a flexible product, release, phase, release work items, and task hierarchical table layout to allow for releases of varying complexity.

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
</table>**Parent Topic:**[Release Management v2 reference](../concept/reference-release-management.md)

