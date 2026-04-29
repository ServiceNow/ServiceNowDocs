---
title: Industrial Workspace homepage destination rules
description: Depending on your assigned roles, you're redirected to different pages in the Industrial Workspace with homepage destination rules. This helps you access the data that you need more quickly and efficiently.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Industrial Workspace, Operational Technology]
---

# Industrial Workspace homepage destination rules

Depending on your assigned roles, you're redirected to different pages in the Industrial Workspace with homepage destination rules. This helps you access the data that you need more quickly and efficiently.

## Homepage destination rules overview

Each destination rule redirects different OT users to different pages on the Industrial Workspace based on their assigned role or roles. Some roles may not have access to the data on one page, so redirecting users to a page where data is available to view helps them better navigate the Industrial Workspace. For example, users with only the Operational Technology Editor \[cmdb\_ot\_editor\] role can't view data on the OT Action-Oriented Landing Page, so they only see the an empty landing page. Instead, they're redirected to the Industrial Workspace Lists, where they can view the applicable OT device data.

## Industrial Workspace homepage destination rule descriptions

The following table describes the Industrial Workspace homepage destination rules and their destinations.

<table id="table_s4z_ljk_mbc"><thead><tr><th>

Rule

</th><th>

Destination

</th><th>

Roles redirected

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT Progress Scorecard Page

</td><td>

now/mfg/ot-progress-scorecard/ \(OT Progress Scorecard\)

</td><td>

ot\_progress\_scorecard\_viewer

</td><td>

The OT Progress Scorecard rule takes users with the roles described in the rule directly to the OT Progress Scorecard when they log in.

</td></tr><tr><td>

Industrial Workspace Home Page

</td><td>

now/mfg/home \(OT Action-Oriented Landing Page\)

</td><td>

-   sn\_ot\_incident\_read
-   sn\_ot\_change\_read
-   sn\_otvr.remediation\_owner

</td><td>

The Industrial Workspace Home Page rule takes users with the roles described in the rule directly to the OT Action-Oriented Landing Page when they log in.

</td></tr><tr><td>

OT Dashboard Library Page

</td><td>

now/mfg/dashboard-library \(OT Dashboard Library\)

</td><td>

cmdb\_ot\_viewer + cmdb\_ot\_isa\_viewer

</td><td>

The OT Dashboard Library Page rule takes users with the roles described in the rule directly to the OT Visibility dashboard when they log in.**Note:** The OT Dashboard Library Page rule only displays if Operational Technology Manager is installed.

</td></tr><tr><td>

ISA Equipment Model Page

</td><td>

now/mfg/isa-equipment-model \(Equipment Model Manager\)

</td><td>

cmdb\_ot\_isa\_viewer

</td><td>

The ISA Equipment Model Page rule takes users with the roles described in the rule directly to the Equipment Model Manager when they log in.**Note:** The ISA Equipment Model Page rule only displays if Industrial Process Manager is installed.

</td></tr><tr><td>

Industrial Workspace List Page

</td><td>

now/mfg/list \(Industrial Workspace Lists\)

</td><td>

cmdb\_ot\_viewer

</td><td>

The Industrial Workspace List Page rule takes users with the roles described in the rule directly to the Industrial Workspace Lists when they log in.

</td></tr></tbody>
</table>**Parent Topic:**[Using the Industrial Workspace](using-industrial-workspace.md)

