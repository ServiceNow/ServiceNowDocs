---
title: Roles required for using the release lifecycle documentation AI agent
description: Learn about which roles are required for using the release lifecycle documentation AI agent.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: reference
last_updated: "2026-04-01"
reading_time_minutes: 1
breadcrumb: [Configure, Release lifecycle documentation AI agent, Use agentic AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Roles required for using the release lifecycle documentation AI agent

Learn about which roles are required for using the release lifecycle documentation AI agent.

<table id="table_klx_5wh_53c"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

update\_set\_admin

</td><td>

Grants access to update set operations that the release lifecycle documentation AI agent uses.

</td></tr><tr><td>

sn\_aia.viewer

</td><td>

Grants access to view and interact with AI agent results.

</td></tr><tr><td>

sn\_releaseops.release\_notes\_user

</td><td>

Grants access to generate and view release notes within ReleaseOps.**Note:** The releaseops\_admin role also includes the release\_notes\_user role. Assigning the releaseops\_admin role is sufficient for using the release lifecycle documentation AI agent, if the user already needs full ReleaseOps admin access.

</td></tr></tbody>
</table>**Parent Topic:**[Configure release lifecycle documentation AI agent](../concept/configure-release-lifecycle-documentation-ai-agent.md)

