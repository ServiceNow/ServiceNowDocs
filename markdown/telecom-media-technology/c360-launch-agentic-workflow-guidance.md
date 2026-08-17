---
title: Launch agentic workflow guidance
description: Launch agentic workflow guidance is a configuration record that determines which agentic workflow runs when a user selects it from the Recommended Actions panel. It also defines what context data is passed to the workflow during execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/c360-launch-agentic-workflow-guidance.html
release: australia
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 1
breadcrumb: [Recommendations panel, Use, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Launch agentic workflow guidance

Launch agentic workflow guidance is a configuration record that determines which agentic workflow runs when a user selects it from the Recommended Actions panel. It also defines what context data is passed to the workflow during execution.

The Launch Agentic Workflow guidance is available if Generative AI Controller is installed. It supports three inputs:

-   Use Case: The specific agentic workflow to run.
-   Context Data: An optional JSON string that is passed into the workflow as context memory when the workflow runs. Context data is background data and does not appear in the Recommended Actions panel or affect how recommendations are displayed.
-   Objective: The objective or the request provided to the workflow.

## Mapping guidance inputs

You can map guidance input in two ways, depending on how the workflow is triggered in the Recommended Actions panel:

-   Recommendation rule: Open the context record under Recommended Actions, open or create a rule, and add a recommendation with the **Guidance** action type and **Launch Agentic Workflow** as the action. After saving, the guidance inputs appear. Populate each input field as needed. You can use data pills to dynamically populate the value from the current record.
-   Search result mapping: Open the search result mapping record for the workflow and populate the guidance inputs.

For more information about mapping guidance inputs, see [Map AI search results with guidance inputs in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-create-search-result-mapping-for-ai-search.md).

**Parent Topic:**[Recommendations panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-recommendations.md)

**Related topics**  


[Recommendations panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-recommendations.md)

