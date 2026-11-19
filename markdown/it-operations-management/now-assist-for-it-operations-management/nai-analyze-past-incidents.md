---
title: Generate a ServiceNow Otto summary of past related incidents
description: View an AI generated summary of past incidents related to the current alert, including strategies used to resolve them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/nai-analyze-past-incidents.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Accelerate alert resolution with past incident analysis, Use generative AI, ServiceNow Otto for ITOM, IT Operations Management]
---

# Generate a ServiceNow Otto summary of past related incidents

View an AI generated summary of past incidents related to the current alert, including strategies used to resolve them.

## Before you begin

-   Install ServiceNow Otto for ITOM. For more information, see [Install the ServiceNow Otto for IT Operations Management \(ITOM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/install-now-assist-itom.md).
-   Ensure that the Alert investigation skill is active. For more information, see [Install the ServiceNow Otto for IT Operations Management \(ITOM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/install-now-assist-itom.md).
-   View important information about the ServiceNow® ServiceNow Otto for IT Operations Management \(ITOM\) application in [ServiceNow Otto for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md).

For comprehensive information about the ServiceNow Otto panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the List icon \(\[Omitted image "icon-lists.png"\] Alt text: List icon.\) in the navigation bar.

3.  Select **Lists** &gt; **Alerts** &gt; **All Alerts**.

4.  Open an alert.

5.  Select the ServiceNow Otto panel icon.

    The panel displays.

6.  Request a ServiceNow Otto past incidents investigation by selecting **Analyze related incidents**.

    An additional Large Language Model \(LLM\) validation layer is added to the AI search capability to improve the accuracy of results returned by AI skills.

    A summary of the most relevant related incidents displays in the panel.

7.  Inspect the details of a related incident by selecting the relevant link under Related Incidents.

    The incident page opens, showing the Overview tab.


**Parent Topic:**[Speed up alert resolution with a ServiceNow Otto analysis of past related incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/nai-past-incidents.md)

