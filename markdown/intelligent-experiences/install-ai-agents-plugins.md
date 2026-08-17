---
title: Install ServiceNow Otto AI Agents
description: Install ServiceNow Otto AI Agents on your ServiceNow instance to enable the agentic AI experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/install-ai-agents-plugins.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, AI Agent Studio, Enable AI experiences]
---

# Install ServiceNow Otto AI Agents

Install ServiceNow Otto AI Agents on your ServiceNow instance to enable the agentic AI experience.

## Before you begin

To get started with AI agents, you must have:

-   **License requirements**: A ServiceNow Otto Pro Plus or Enterprise Plus license.

    **Note:** A ServiceNow Otto License is required. ServiceNow Otto AI Agents is available to all instances that have who have ServiceNow Otto.

-   **Instance requirements**: An instance on Australia Patch 1 or later.
-   **Application requirements**: The following store applications and all the dependency applications must be installed and updated:
    -   ServiceNow Otto for IT or HRSD \(or other workflows\).

        **Note:** ServiceNow Otto AI Agents aren’t standalone applications that you can install directly. To enable AI agents on your instance, you must install and activate other ServiceNow Otto applications that include AI agents, such as ServiceNow Otto for IT Service Management \(ITSM\) or ServiceNow Otto for Customer Service Management \(CSM\).

    -   ServiceNow Otto AI Agents store application
-   AI Search enabled on your instance.
-   The ServiceNow Otto panel must be turned on.

    **Note:** You can access AI agents in the ServiceNow Otto panel. To enable the ServiceNow Otto panel, see [Turn on the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).


Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for and select a ServiceNow Otto application, such as ServiceNow Otto for IT Service Management \(ITSM\) or Now Assist for Platform.

3.  Select **Install**.


## Result

AI agents associated with the ServiceNow Otto application are installed on your instance.

## What to do next

-   **Assign the admin role**

    Add the role `sn_aia.admin` to the user who will administer the AI Agent Studio, and then navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

-   **Access the AI Agent Studio**

    Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview** in the AI Agent Studio application navigator where you can create and manage AI agents and agentic workflows.


