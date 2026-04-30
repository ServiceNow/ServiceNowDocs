---
title: Example agentic workflow
description: Use the example agentic workflow with clear name, description, and list of steps fields to use as a guide when creating your own agentic workflows.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-10-16"
reading_time_minutes: 2
breadcrumb: [Writing effectively for agentic AI, AI agents best practices, Explore, Now Assist AI agents, Enable AI experiences]
---

# Example agentic workflow

Use the example agentic workflow with clear name, description, and list of steps fields to use as a guide when creating your own agentic workflows.

-   **Name**

    Investigate incident

-   **Description**

    This workflow streamlines incident management by analyzing incidents, linking them to existing problems, and identifying relevant catalog items. It leverages three specialized AI agents: the ITSM Incident Resolution Investigation AI Agent retrieves incident details, identifies similar incidents, and fetches relevant knowledge articles; the Link Incident to Problem AI Agent searches for and links incidents to existing problems based on contextual similarity; and the Find Catalog Item AI Agent locates relevant catalog items and integrates their details into incident records or provides direct links. This structured orchestration ensures efficient incident resolution, reduces redundancy, and enhances decision-making by leveraging historical data, organizational knowledge, and catalog resources, ultimately improving enterprise incident management effectiveness.

-   **List of steps**

    Step 1: Incident Analysis:

    Analyze incident details and retrieve relevant historical data and knowledge articles.

    Step 1.1: Retrieve Incident Context:

    -   Use the ITSM Incident Resolution Investigation AI Agent to fetch incident details \(short description, description, caller, state\).
    -   If retrieval fails, inform the user: "Unable to retrieve incident details. Please verify the incident number." and terminate workflow.
    Step 1.2: Identify Similar Incidents and Knowledge Articles:

    -   Use the ITSM Incident Resolution Investigation AI Agent to find similar incidents and relevant knowledge articles.
    -   Confirm with the user before adding resolutions to incident comments.
    Step 1.3: Prepare Incident Documentation:

    Update incident additional comments with approved resolutions and knowledge article references, preparing clear documentation for next phase.

    Step 2: Problem Linking:

    Link the incident to an existing relevant problem, if applicable.

    Step 2.1: Receive Incident Documentation:

    Use Link Incident to Problem AI Agent to validate incident details and confirm no existing problem linkage.

    Step 2.2: Identify Relevant Problems:

    -   Execute search for relevant problems using incident short description.
    -   If no relevant problems found, inform the user: "No relevant problems found to link." and proceed to Catalog Item Identification.
    Step 2.3: Link Incident to Problem:

    -   Present most similar problem details to the user for approval.
    -   Upon user approval, link incident to problem using "Set problem to incident" tool; confirm successful linkage to the user.
    Step 3: Catalog Item Identification:

    Identify and integrate relevant catalog items into the incident record.

    Step 3.1: Receive Incident and Problem Context:

    Use Find Catalog Item AI Agent to validate incident context and prepare for catalog item search.

    Step 3.2: Execute Catalog Item Search:

    -   Perform targeted search for relevant catalog items based on incident description.
    -   If no catalog items found, inform the user: "No relevant catalog items identified." and proceed to final delivery.
    Step 3.3: Integrate Catalog Item Details:

    -   Present catalog item choices to the user; upon selection, either add catalog item details to incident additional comments or provide direct catalog item link.
    -   Confirm successful integration or delivery to the user and complete workflow.

