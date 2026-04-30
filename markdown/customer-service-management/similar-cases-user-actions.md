---
title: Similar case user actions
description: Customer service agents and major issue managers can use the similar case recommendation feature to link cases, copy resolution information, propose major case candidates, and add cases to existing major cases.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Similar case recommendations, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Similar case user actions

Customer service agents and major issue managers can use the similar case recommendation feature to link cases, copy resolution information, propose major case candidates, and add cases to existing major cases.

<table id="table_dgq_zmq_cgb"><thead><tr><th>

User Action

</th><th>

Description

</th><th>

UI Action

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Customer service agent can link the current case to a similar case

</td><td>

-   **Agent Workspace**: The Predictive Intelligence tab shows a list of similar cases ordered by the similarity score.
-   **Platform**: The Related Search Results section of the case form shows a list of similar cases ordered by the similarity score.

</td><td>

-   Agent Workspace: Select the More UI actions menu and select **Link to Case**.
-   Platform: Select the desired case in the search results list, then select **Link to Case**.

</td><td>

The current case is linked as a child of the similar case.

</td></tr><tr><td>

Customer service agent can copy resolution information from a resolved case to the current case

</td><td>

**Agent Workspace**: The Predictive Intelligence tab shows a list of resolved similar cases ordered by the similarity score.

</td><td>

Agent Workspace: Select the More UI Actions menu and select **Copy Resolution**.

</td><td>

Copies the resolution code and resolution notes from the similar case to the current case. **Note:** Be sure to save the current case record.

</td></tr><tr><td>

Customer service agent can propose a major case candidate**Note:** The Major Issue Detector similarity solution definition must be active.

</td><td>

**Agent Workspace**: The Predictive Intelligence tab shows a major issue recommendation with the following message: "We noticed that \(x\) similar cases have been created for \(y\) different accounts in the last \(z\) hours. Propose this as a major issue?"

</td><td>

Agent Workspace: Select the **Propose Major Case** link.

</td><td>

The current case is proposed as a major issue.

</td></tr><tr><td>

Major issue manager can associate the current case to a major case**Note:** The Major Issue Detector similarity solution definition must be active.

</td><td>

**Agent Workspace**: the Predictive Intelligence tab lists one or more major cases similar to the current case, ranked by similarity score.

</td><td>

Agent Workspace: Select the More UI Actions menu and select **Link to this major issue**.

</td><td>

The current case is added as a child to the major case.

</td></tr></tbody>
</table>**Related topics**  


[Similarity solutions](https://www.servicenow.com/docs/access?context=word-collection-similarity-solution&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)

