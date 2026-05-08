---
title: Installed with Badge Reader Integration
description: Several types of components are installed with activation of the Badge Reader Integration plugin, including tables and user roles.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate Badge Reader Integration, Badge Reader Integration for Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Installed with Badge Reader Integration

Several types of components are installed with activation of the Badge Reader Integration plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

Demo data is available for this feature.

<table id="table_ms2_yqb_yjb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Badge admin\[sn\_badge.badge\_admin\]

</td><td>

Used to administer badge reader integrations.

</td><td>

None

</td></tr></tbody>
</table><table id="table_vvc_brb_yjb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Badge\[sn\_badge\_user\_badge\]

</td><td>

Record used to configure a user badge, associating a user to a badge number and facility code.

</td></tr><tr><td>

Badge Event Handler\[sn\_badge\_event\_handler\]

</td><td>

Record used to configure actions associated with a badge scan event. Stores an event handler script that can be mapped to a badge reader.

 Extends the Application File table.

</td></tr><tr><td>

Badge Scan Log\[sn\_badge\_scan\_log\]

</td><td>

Record used to log all badge reader error events.

</td></tr><tr><td>

Badge Reader\[sn\_badge\_badge\_reader\]

</td><td>

Record used to configure badge reader devices.

 Extends the Task table.

</td></tr></tbody>
</table>**Parent Topic:**[Activate Badge Reader Integration](../task/activate-badge-reader-integration.md)

