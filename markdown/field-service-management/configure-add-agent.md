---
title: Configure additional settings for dispatchers to temporarily add agents
description: There are additional settings you, the administrator, can configure for dispatchers to temporarily add agents. You can enable more fields for dispatchers to search on.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure additional settings for dispatchers to temporarily add agents

There are additional settings you, the administrator, can configure for dispatchers to temporarily add agents. You can enable more fields for dispatchers to search on.

By default dispatchers can add any agent to Dispatcher Workspace who is part of the assignment groups or territories they manage. You can enable dispatchers to add any agent to Dispatcher Workspace, even those outside of the assignment groups or territories the dispatcher manages. Note that dispatchers can only search for the agent; they cannot assign tasks to agents unless the dispatcher manages the assignment group or territory that the agent is part of.

Dispatchers can search for agents by their name, email address, or employee number. Administrators can allow dispatchers to search for any filed that is available on the system user table.

1.  Turn on the setting **Enable dispatcher to add agents outside of their assigned assignment groups / territories** on the Configure settings page to allow dispatchers to search for any agent. For more information see [Configure settings for Dispatcher Workspace](../task/configure-workspce-settings.md).
2.  Add additional fields dispatchers can search for agents by. You can add any field that is on the system user table. For more information look for the **Add agents by searchable fields** in [Configure settings for Dispatcher Workspace](../task/configure-workspce-settings.md).

