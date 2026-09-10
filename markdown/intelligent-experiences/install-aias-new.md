---
title: Install AI Agent Studio
description: Install Now Assist AI agents on your ServiceNow instance to enable the agentic AI experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/install-aias-new.html
release: australia
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 2
keywords: [Install AI Agents]
breadcrumb: [Configure AI Agent Studio, AI Agent Studio, Enable AI experiences]
---

# Install AI Agent Studio

Install Now Assist AI agents on your ServiceNow instance to enable the agentic AI experience.

## Before you begin

To get started with AI agents, you must have:

-   **License requirements**: A ServiceNow Pro Plus or Enterprise Plus license.

    **Note:** A Now Assist License is required. Now Assist AI Agents is available to all users who have Now Assist.

-   **Instance requirements**: An instance on Australia Patch 1 or later.
-   **Application requirements**: The following store applications and all the dependency applications must be installed and updated:
    -   Now Assist for IT or HRSD \(or other workflows\).

        **Note:** AI agents aren’t standalone applications that you can install directly. To enable AI agents on your instance, you must install and activate other Now Assist applications that include AI agents, such as ServiceNow Otto for IT Service Management \(ITSM\) or ServiceNow Otto for Customer Service Management \(CSM\).

    -   Now Assist AI Agents store application
-   AI Search enabled on your instance.
-   The Now Assist panel must be turned on.

    **Note:** You can access AI agents in the Now Assist panel. To enable the Now Assist panel, see [Turn on the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).


Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for and select a Now Assist application, such as ServiceNow Otto for IT Service Management \(ITSM\) or Now Assist for Platform.

3.  Select **Install**.


## Result

AI agents associated with the Now Assist application are installed on your instance.

## What to do next

-   **Assign the admin role**

    Add the role `sn_aia.admin` to the user who will administer the AI Agent Studio, and then navigate to **All &gt; AI Agent Studio &gt; Overview**.

-   **Access the AI Agent Studio**

    Navigate to **All &gt; AI Agent Studio &gt; Overview** in the AI Agent Studio application navigator where you can create and manage AI agents and agentic workflows.


Group Action Framework \(GAF\) is an optional way for AI agents to identify and access records using AI-generated indexes and clusters. GAF can be faster and more reliable than AI Search, the default, in some cases. If you want to set up GAF, which can be used instead of AI Search results for gathering related records, see [Set up Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-gaf.md).

