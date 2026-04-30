---
title: Case action summary and post case review assignment rules
description: Use assignment rules to assign case action summaries and post case review documents to customer service agents.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customer Service case digests, Configure case digests, Configure case management, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Case action summary and post case review assignment rules

Use assignment rules to assign case action summaries and post case review documents to customer service agents.

The Case Digests plugin includes two assignment rules:

-   **Auto assign the CAS to case agent**
-   **Auto assign the PCR to case agent**

When an agent clicks either **Send Case Action Summary** or **Create Post Case Review** on a case record, the system creates the corresponding record and automatically assigns it to that agent.

The system administrator can modify these assignment rules or define different rules to assign case action summary and post case review records. The system populates the **Assigned to** field on the Case Action Summary or Post Case Review form with the user determined by the assignment rule. If there are no active assignment rules, the **Assigned to** field remains blank and the record can be assigned manually.

If using the provided assignment rules that auto assign the records to the same agent:

-   The agent clicks **Send Case Action Summary** or **Create Post Case Review** on the Case form.
-   The corresponding record opens with the agent's name in the **Assigned to** field.
-   The record state is **In Progress**.

If using assignment rules that do not auto-assign the records to the same agent:

-   The agent clicks **Send Case Action Summary** or **Create Post Case Review** on the Case form.
-   The corresponding records are created but are not displayed.
-   If assigned to another agent, the **Assigned to** field displays the agent's name and the state updates to **In Progress**.
-   If unassigned, the record remains in the **New** state.

