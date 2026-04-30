---
title: View similar case recommendations
description: The similar case recommendation feature allows customer service agents to quickly find similar cases that can provide helpful information about a current case. This feature can also provide recommendations about cases that may be related to major issues.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use Task Intelligence for Customer Service, Automate and optimize, Using Customer Service Management, Customer Service Management]
---

# View similar case recommendations

The similar case recommendation feature allows customer service agents to quickly find similar cases that can provide helpful information about a current case. This feature can also provide recommendations about cases that may be related to major issues.

By performing a contextual search based on a case’s short description, the system generates a list of similar records. This provides agents with a list of cases that are similar to the current case. These similar cases may provide helpful details or resolution information for the current case. Task Intelligence can also suggest potential major issues and major cases.

With the similar case recommendation feature, customer service agents can:

-   Identify cases similar to the current case.
-   Copy resolution notes from resolved cases to the current case.
-   Link the current case to a similar case.
-   View a list of open and resolved cases similar to the current case and submit the current case as a major case candidate. Three similar open and resolved cases are displayed in the list of results.
-   View one or more similar major cases, that are displayed first in the list of results. Agents can use an available action and link the current case as a child to a major case.

When using these similarity models in the workspace, the agent can open a case record, select the **Recommendations** tab in the contextual side panel, and then select the **Suggested actions** sub tab to see the following:

-   One for propose major case and one for similar major case card \(if enabled\).
-   Up to three similar open case cards \(number of cards displayed is customer configurable\).
-   Up to three similar resolved case cards \(number of cards displayed is customer configurable\).

Order of cards displayed in Suggested actions:

-   Similar major case \(if there is a major case\)
-   Propose major case
-   Similar resolved cases
-   Similar open cases

Actions on cards:

-   Propose major case: The current case is proposed as a major issue.
-   Copy resolution notes: Copies resolution nodes from similar case to current case \(does not copy resolution code\).
-   Link case: The current case is linked as a child of the similar case.

Any changes made to the current case and saved will trigger a refresh of the recommendations, checking for both new and obsolete recommendations.

Plugins: The configuration for the similar case recommendation feature is included with the Customer Service plugin \(com.sn\_customerservice\). The similar case recommendation feature has a dependency on Major Issue Management – activate the Major Issue Management plugin \(com.sn\_majorissue\_mgt\).

For more info, see [Similar case user actions](../reference/similar-cases-user-actions.md)

