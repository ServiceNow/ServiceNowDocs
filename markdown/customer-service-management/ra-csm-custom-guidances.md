---
title: Guidances in Recommended Actions for Customer Service
description: A guidance is an action that an agent can take or information that an agent can share as they work to resolve tasks, such as customer service cases. Guidances appear as cards in the contextual side panel in a workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Recommended Actions for Service, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Guidances in Recommended Actions for Customer Service

A guidance is an action that an agent can take or information that an agent can share as they work to resolve tasks, such as customer service cases. Guidances appear as cards in the contextual side panel in a workspace.

The Recommended Actions for Customer Service application includes custom guidances for the following tables:

-   Knowledge
-   Case
-   Incident
-   Problem
-   Change Request

These guidances enable search results from the corresponding search source tables for the Case Context record. Customer service agents can see these results in the Recommended Actions tab in the contextual side panel.

## Knowledge guidance

The Case Context record includes a search result mapping record for the Knowledge table that maps search results to the [Attach and share article](ra-csm-guidances-attach-share-article.md) guidance. When an agent is viewing a case record, preview cards for Knowledge search results in the Recommended Actions tab include the **Attach and share article** action.

## Case guidance

The Case Context record includes a search result mapping record for the Case table. This record maps search results from the Case table to the **Case resolution guidance**.

The Case resolution guidance is configured with dynamic actions that are determined by the state of the case returned by the search. These actions include:

-   **Link as parent case**: This action links the recommended case as a parent to the current case. \(The current case is a non-major case and the recommended case is major/non-major\).
-   **Link as child case**: This action links the recommended case as a child to the current case. \(The current case is a major case and the recommended case is a non-major case.\)
-   **Copy resolution**: This action copies the resolution code and resolution notes from the recommended case to the current case. This action is available when the recommended case is in the Closed or Resolved state.

**Note:** If the current case and the recommended case are both major cases, no action is included on the preview card.

The preview card for the case resolution guidance includes the case title and number, the current state and priority, the case description, and the dynamic action.

## Interaction guidance

The Case Context record includes a search result mapping record for the Incident table. This record maps search results from the Incident table to the **Link incident to current case** guidance.

Agents can link the recommended incident by selecting the **Link incident** action on the preview card in the Recommended Actions tab. This action does the following:

-   Updates the **Incident** field on the case record with the incident number.
-   Adds an entry to the work notes.
-   Displays a message when the incident is successfully linked. A message is also displayed if the linking fails.

The preview card for the **Link incident to current case** guidance includes the incident title and number, the current state and priority, and a brief description of the incident.

## Problem guidance

The Case Context record includes a search result mapping record for the Problem table. This record maps search results from the Problem table to the **Link problem to current case** guidance.

Agents can link the recommended problem by selecting the **Link problem** action on the preview card in the Recommended Actions tab. This action does the following:

-   Updates the **Problem** field on the case record with the problem number.
-   Adds an entry to the work notes.
-   Displays a message when the problem is successfully linked. A message is also displayed if the linking fails.

The preview card for the **Link problem to current case** guidance includes the problem title and number, the current state, the number of related incidents, and a brief description of the problem.

## Change request guidance

The Case Context record includes a search result mapping record for the Change Request table. This record maps search results from the Change Request table to the **Link change request to current case** action.

Agents can link the recommended change request by selecting the **Link change request** action on the preview card in the Recommended Actions tab. This action does the following:

-   Updates the **Change Request** field on the case record with the change request number.
-   Adds an entry to the work notes.
-   Displays a message when the change request is successfully linked. A message is also displayed if the linking fails.

The preview card for the **Link change request to current case** guidance includes the change request title and number, the current state, the risk level and type of change, and a brief description of the change request.

