---
title: Create a Copilot Studio Dataverse custom role
description: Create a Copilot Studio Dataverse custom role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-a-copilot-studio-dataverse-custom-role.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-07-03"
reading_time_minutes: 1
breadcrumb: [Microsoft, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create a Copilot Studio Dataverse custom role

Create a Copilot Studio Dataverse custom role.

## Before you begin

Role required: User Security role

## Procedure

1.  Navigate to **Power Platform Admin Center** &gt; **Environments** &gt; **Pick the environment** &gt; **Settings** &gt; **Users + Permissions** &gt; **Security roles**

2.  Select **New role** and give it a name like SGC-Copilot Discovery \(Read only\).

    **Note:** Start empty rather than copying, so you don't inherit stray privileges.

3.  In the role editor, find each of the three tables and set only the Read privilege.

    Three tables:

    -   Bot— The agents/copilots themselves.
    -   Botcomponent— Topics, entities, and other authored components.
    -   Conversationtranscript— The transcript records; the transcript body lives in the Content column, which comes back with the row's Read privilege \(no separate file/attachment privilege needed for this table\).
4.  Set the Read access level to the scope your discovery needs.

    For tenant/environment‑wide cataloging via a service principal, set Read to **Organization** \(the filled full circle\) on all three tables. Anything lower \(User/BU\) will silently hide records the app user doesn't "own".

5.  Select **Save**.


