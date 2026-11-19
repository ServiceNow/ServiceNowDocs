---
title: Agent assist
description: Learn about how the CSM Agent Workspace Agent assist functions with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-agent-assist.html
release: australia
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Agent assist

Learn about how the CSM Agent Workspace Agent assist functions with CSM Configurable Workspace.

Agent assist provides agents with automatic search results that show possible solutions for records they open. Configure Agent assist in CSM Configurable Workspace by configuring a record page with a Glide form data source and a Contextual Sidebar. For more information, see [Agent assist Overview](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/sn-agent-assist-uib/overview) on the ServiceNow Developer Site.

**Note:** You may need to log in to the Developer Site to see the content.

For more information about using contextual search for Agent Assist, see [Contextual search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ContextualSearch.md).

If Agent assist isn't configured correctly in CSM Configurable Workspace, agents lose the suggested-solution panel and must search manually. Unlike most CSM Agent Workspace configurations, Agent assist settings carry over without a migration step. However, CSM Configurable Workspace requires you to configure Agent assist through the record page setup instead of a standalone configuration.

## Before you verify Agent assist

-   Confirm that Agent assist was configured and active in your CSM Agent Workspace deployment.
-   Open a case record in CSM Configurable Workspace and check whether the Recommended Actions panel appears in the contextual sidebar. Agent assist results surface through the Contextual Sidebar component.

## Verify Agent assist after migration

Role required: admin

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**. On the **Experiences** tab, select **CSM/FSM Configurable Workspace**.
2.  Open the CSM default record page and confirm that it has a Glide form data source configured.
3.  Confirm that the page includes a Contextual Sidebar component.
4.  Open a case record as an agent and verify that search results appear in the Recommended Actions panel.

