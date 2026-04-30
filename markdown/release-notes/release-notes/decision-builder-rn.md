---
title: Decision tables in Workflow Studio release notes
description: The ServiceNow Workflow Studio application provides an intuitive interface that you can use to create and manage decision tables. By changing the rules and conditions in a decision table, you can more efficiently meet changing business requirements. Workflow Studio was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Decision tables in Workflow Studio release notes

The ServiceNow® Workflow Studio application provides an intuitive interface that you can use to create and manage decision tables. By changing the rules and conditions in a decision table, you can more efficiently meet changing business requirements. Workflow Studio was enhanced and updated in the Xanadu release.

## Workflow Studio highlights for the Xanadu release

-   Create a decision table inline while authoring a flow or subflow in Workflow Studio.
-   Use decision tables directly in your playbooks in Workflow Studio. Add the **Make a Decision - First Match** activity with inputs from your playbook to manage complex decisions.
-   In large decision tables, scroll within the table to see more rows.
-   Rank the order in which decision rows are read in your table, and reorder rows as needed.

See [Exploring decision tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) for more information.

**Important:** Workflow Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Workflow Studio to Xanadu

Workflow Studio is automatically installed on your instance. However, Workflow Studio is a ServiceNow Store application, so to get the latest features, you must update your version manually to the most recent version. As of Washington DC Patch 3, updating Workflow Studio automatically updates all its application dependencies such as Workflow Studio, playbook, and Decision Builder. You can no longer see or update the individual application dependencies of Workflow Studio from the ServiceNow Store or the list of plugins.

## New in the Xanadu release

-   **[Create a decision table in a flow](https://www.servicenow.com/docs/access?context=create-decision-table-flow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Create a decision table directly in your flow to add decisions quickly using the flow's inputs.

-   **[Create a decision table in a subflow](https://www.servicenow.com/docs/access?context=create-decision-table-subflow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Create a decision table directly in your subflow to add decisions quickly using the flow or subflow's inputs.

-   **[Create a decision table in a Playbook](https://www.servicenow.com/docs/access?context=make-decision-first-match-activity&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Add a decision table directly in a Playbook to manage complex business logic using the **Make a Decision - First Match** activity. Add inputs from the playbook and manage other actions based on the results of your decision tables.

-   **[Rank and reorder decision table rows](https://www.servicenow.com/docs/access?context=modify-decision-table-rules&version=xanadu&pubname=xanadu-build-workflows&section=reorder-decision-row&ft:locale=en-US)**

    Determine or change the sequence in which your decision rules are evaluated by reordering the rows in a decision table. Type a new value in the **Rank** column to easily change decision row order.


## Changed in this release

-   **Theme updates**

    Some details in the decision table UI have been updated to follow standard ServiceNow AI Platform themes.

-   **Usability enhancement for scrolling within decision tables**

    In large decision tables, scroll within the table to see more rows. Note that the headers stay at the top of the table.


## Localization information

The Localization Framework is integrated in decision tables. However, because editing in Excel doesn’t support localization, you cannot use this feature in any instance that doesn't use English.

## Related ServiceNow applications and features

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Integrate workflow authoring, configuring, and monitoring into a single page experience.

-   **[Exploring flows](https://www.servicenow.com/docs/access?context=exploring-flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Flows automate a repeatable multi-step process. When the flow trigger conditions are met, the flow runs a sequence of reusable actions and flow logic to complete the process.

-   **[Exploring playbooks](https://www.servicenow.com/docs/access?context=process-automation-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Workflow Studio playbooks enable process owners to author cross-enterprise workflows and create a single, unified process. Build the underlying processes for playbooks that Playbook Experience agents and fulfillers use.


**Parent Topic:**[Workflow Studio release notes](../now-platform-app-engine/workflow-studio-rn.md)

