---
title: Activate AI agents for IT Operations Management \(ITOM\)
description: Activate AI agents associated with the Triage and analyze alerts agentic workflow, to enable the agentic AI experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/install-now-assist-ai-agents-itom.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [AI Agents, agentic AI]
breadcrumb: [Configure, ServiceNow Otto for ITOM, IT Operations Management]
---

# Activate AI agents for IT Operations Management \(ITOM\)

Activate AI agents associated with the Triage and analyze alerts agentic workflow, to enable the agentic AI experience.

## Before you begin

Before activating the AI agents, you must install the ServiceNow Otto for IT Operations Management \(ITOM\) plugin. For more information, see [Install the ServiceNow Otto for IT Operations Management \(ITOM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/install-now-assist-itom.md).

To get started with AI agents, you must have:

-   An instance on Yokohama patch 3 and above.
-   A ServiceNow Pro Plus or Enterprise Plus license.
-   AI Search enabled on your instance.

Role required: admin

## Procedure

1.  Activate the Triage and analyze alert agentic workflow in AI Agent Studio.

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    2.  In the table, select **Triage and analyze alerts**.

    The Triage and analyze alerts page in AI Agent Studio lets you manage the agentic workflow, including options for Describe and connect, Define trigger, and Select display.

2.  Make the Triage and analyze alerts agentic workflow visible in the ServiceNow Otto panel.

    1.  Navigate to **Select display**.

    2.  Next to **ServiceNow Otto panel** select the **Display** toggle to turn on the display.

    3.  Select **Save and test**.

    4.  Navigate to **All** &gt; **Virtual Agent** &gt; **Designer**.

    5.  From the **Select assistant** drop-down list, select **ServiceNow Otto Panel - Platform\(default\).**

    6.  Search for **Triage and analyze alerts**.

    7.  Select the row Actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text: Actions icon.\), and select **Promoted**.


## What to do next

To access AI agents in the ServiceNow Otto panel, you must enable the panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).

**Parent Topic:**[Configure ServiceNow Otto for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-configure.md)

