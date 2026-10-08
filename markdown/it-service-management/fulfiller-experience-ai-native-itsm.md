---
title: Fulfiller experience in Simplified IT Service Management
description: The Simplified IT Service Management fulfiller experience consists of simplified incident and request management with AI recommendations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/fulfiller-experience-ai-native-itsm.html
release: brazil
topic_type: concept
last_updated: "2026-09-22"
reading_time_minutes: 4
breadcrumb: [Simplified IT Service Management, IT Service Management]
---

# Fulfiller experience in Simplified IT Service Management

The Simplified IT Service Management fulfiller experience consists of simplified incident and request management with AI recommendations.

## Fulfiller experience key features

These are the fulfiller experience key features with Simplified IT Service Management.

-   Automatically create an incident or request from a chat.
-   Provide incident and chat summaries and suggest next steps.
-   Generate recommendations, resolution notes, summaries, and email responses.
-   Attach knowledge articles, link similar incidents, and order catalog items.
-   Automatically capture conversation summary when a live chat is handed off to a fulfiller.
-   Provide a Service Desk Manager dashboard.

## Simplified IT Service Management home page

You can access the Simplified IT Service Management home page from Service Operations Workspace.

**Note:** For users that have the Service Desk Agent \[sn\_service\_desk\_agent\] role, the Simplified IT Service Management view is shown \(even with Advanced and Prime product tiers\).

To access advanced flow features, such as with Major Incident Management or the full Service Operations view for each workflow, ensure that the user does not have the sn\_service\_desk\_agent role with itil/admin roles.

The Simplified ITSM landing page contains these main metrics:

-   Assigned to you: Incidents, requests, and catalog tasks that are assigned to you.
-   Overdue: Incidents, requests, and catalog tasks that are breaching or about to breach.
-   Unassigned: Incidents, requests, and catalog tasks that are waiting to be assigned.

Also included are the Incidents, Requests, and Catalog Tasks lists.

\[Omitted image "home-ai-native-itsm.png"\] Alt text: AI native home landing page.

## Triage and Categorize agentic workflow

The Triage and Categorize agentic workflow automatically evaluates incoming incidents to determine the appropriate category, subcategory, service, offering, and configuration item. This workflow executes based on trigger conditions you define and reduces manual categorization effort and improves routing accuracy. To use this workflow, you must have the Service Desk Agent \[sn\_service\_desk\_agent\] role.

The workflow evaluates incident details such as description, symptoms, and affected services to automatically assign the most appropriate category. This routes incidents to the right team and reduces time to resolution.

The workflow also links the incident to a matching Major Incident or Problem when one exists. If no confident match is found, the workflow checks for a surge of 10 or more similar incidents within 30 minutes. When it detects a surge, it proposes a new Major Incident instead of linking the current incident.

**Note:** AI-generated categorization and routing suggestions may not always be accurate. Review all automated assignments before taking action.

Fulfillers can invoke the workflow by using keywords such as, "triage and categorize" followed by the incident number.

For more information, see [IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-catincidents-usecase.md).

## Investigate and Resolve agentic workflow

The Investigate and Resolve agentic workflow enables fulfillers to resolve incidents more efficiently by automatically suggesting resolution steps, related knowledge articles, and similar past incidents. This workflow executes based on trigger conditions you define. To use this workflow, you must have the Service Desk Agent \[sn\_service\_desk\_agent\] role.

The workflow analyzes the incident details and context to provide targeted recommendations for investigation and resolution. This enables fulfillers to focus on complex issues while the AI agent handles routine troubleshooting and information gathering.

**Note:** AI-generated recommendations may not always be accurate. Review all suggestions before applying them to an incident.

Fulfillers can invoke the workflow by using keywords such as, "investigate" or "tell me about" followed by the incident number.

For more information, see [IT Service Management AI agent collection Investigate and resolve ITSM incidents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-incident-resolver-workflow.md).

## Wrap-up and Resolve agentic workflow

The Wrap-up and Resolve agentic workflow enables fulfillers to close out an incident more efficiently. The workflow wraps up the incident and sets the incident state to Resolved. To use this workflow, you must have the Service Desk Agent \[sn\_service\_desk\_agent\] role.

After the incident is resolved, the workflow can optionally suggest knowledge articles or known error articles to attach to the incident. This helps document how the incident was resolved and makes the information available for future incidents.

**Note:** AI-generated recommendations may not always be accurate. Review all suggestions before applying them to an incident.

Fulfillers can invoke the workflow by using phrases such as, "Wrap-up incident", or "Wrap-up", followed by the incident number.

For more information, see [ITSM Wrap-up and resolve incident agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-wrap-up-resolve-incident-aw.md).

-   **[Left navigation bar in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/fulfiller-left-navigation.md)**  
The left navigation bar provides quick access to Simplified IT Service Management core functions and workspace navigation without navigating away from your current work.
-   **[Accept a live chat from a requester](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/accept-chat-ai-native-itsm.md)**  
Automatically create an incident by accepting a live chat or phone call from a requester.
-   **[Generating AI summary and next steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/generating-ai-native-itsm.md)**  
You can generate AI summary, key actions taken, proposed next steps, and related search results directly on the incident form to help resolve the incident, and also summarize the incident to gain an overall understanding of the incident details.
-   **[Using the Service Desk Team Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/using-now-assist-ai-native-itsm.md)**  
Service desk managers can use the Service Desk Team Dashboard to view key performance metrics, including incident and requested item backlog, and team MTTR.

**Parent Topic:**[Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/ai-native-it-service-desk-landing-page.md)

