---
title: Roles and tables installed with AI Data Explorer
description: Reference information for roles and tables installed when you activate AI Data Explorer. Use this information to understand permissions and metadata storage for explorations.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [roles, tables, permissions, explorations, AI canvas, notebook, now assist explorer, semantic data layer, workspaces, metadata]
audience: administrator
breadcrumb: [Reference, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Roles and tables installed with AI Data Explorer

Reference information for roles and tables installed when you activate AI Data Explorer. Use this information to understand permissions and metadata storage for explorations.

## Roles installed

<table id="table_gd5_y3q_tfc"><thead><tr><th>

Role name

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

now\_assist\_explorer\_user

</td><td>

Enables users to see AI Data Explorer in unified navigation and the Explore button ![Explore with AI button](../image/analyze-ai-icon.png) on eligible lists and widgets on dashboards. Users can create explorations or browse and edit shared explorations.

**Note:** If you share an exploration with edit rights, but the user does not have this role, they can only view the exploration regardless.

</td><td>

sn\_query\_gen.user

</td></tr><tr><td>

now\_assist\_explorer\_admin

</td><td>

Can access and manage all explorations on the instance. Can control the visibility of AI Data Explorer in workspaces. Can view logs and manage tables in the semantic data layer \(inherited from sn\_query\_gen\_admin\). For more information, see [Query Generation logs](query-generation-logs.md) and [Add a table to the semantic data layer](../task/add-table-semantic-layer.md#).

</td><td>

now\_assist\_explorer\_user, sn\_query\_gen.admin, uxframework\_user

</td></tr></tbody>
</table>## Tables installed

The AI Data Explorer application is private. You cannot edit these tables directly. However, if you have the admin role, you can read them. Each table begins with the prefix "paai\_canvas."

PAAI Canvas, PAAI Canvas Component, and PAAI Canvas Conversation records follow this hierarchy: Canvas \(one record per exploration\) &gt; Conversation \(currently one per canvas\) &gt; Component \(one or more per conversation\).

<table id="table_kd5_y3q_tfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PAAI Canvas

 \[paai\_canvas\]

</td><td>

Contains name, goal, sys ID, domain, and other metadata that defines an exploration. Each record is a separate exploration.

</td></tr><tr><td>

PAAI Canvas Component

 \[paai\_canvas\_component\]

</td><td>

Contains the metadata for the UX macroponents, such as data visualizations, that get added to an exploration.

</td></tr><tr><td>

PAAI Canvas Conversation

 \[paai\_canvas\_conversation\]

</td><td>

Conversations include AI answers with text, links to data visualizations, and any user input. Currently there is one conversation per exploration.

</td></tr><tr><td>

PAAI Canvas Log

 \[paai\_canvas\_log\]

</td><td>

Stores relevant licensing information.

</td></tr><tr><td>

PAAI Canvas Permission

 \[paai\_canvas\_permission\]

</td><td>

Permissions governing who an exploration is shared with. Each collaborator has a permission record for their rights in that exploration. A user has one such record for each exploration they collaborate in.

</td></tr><tr><td>

PAAI Canvas Workspace Config\[paai\_canvas\_workspace\_config\]

</td><td>

Workspaces/experiences for which links from data visualizations to AI Data Explorer are turned off.

</td></tr></tbody>
</table>**Parent Topic:**[AI Data Explorer reference](../concept/now-assist-explorer-reference.md)

