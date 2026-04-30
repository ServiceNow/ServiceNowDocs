---
title: Configuring Guided Decisions
description: Create structured troubleshooting processes for your agents through the ServiceNow Guided Decisions Experience application. Help your agents solve complex issues in a consistent way.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configuring Guided Decisions

Create structured troubleshooting processes for your agents through the ServiceNow® Guided Decisions Experience application. Help your agents solve complex issues in a consistent way.

The Guided Decisions Experience application is a tool for authoring and running decision tree flows. A decision tree walks an agent through a troubleshooting process based on a record context. The process asks a series of questions and the agent provides the answers. Based on those answers, the agent receives guidance on the next steps to take in the resolution process. Agents can resolve complex issues faster and more efficiently. For more information, see [Decision trees in Guided decision](decision-trees-in-guided-decisions.md).

## Scenarios for using decision trees

Decision trees can help agents resolve the following types of customer issues:

-   Troubleshoot a faulty device, such as a laptop that doesn't work. Use a decision tree to find the cause and provide a fix for the customer.
-   Review a refund request. Use a decision tree to determine whether the customer is eligible for a refund, which can include checking for exceptions and creating tasks.
-   Reset a customer's password. Use a decision tree to walk the agent through the process, such as verifying the customer's identity, trying other options, and, if needed, resetting the password.

For an example of end-to-end configuration of a decision tree for a specific scenario, see [Example configuration of a decision tree](example-decision-tree.md).

## Guided Decisions features

-   Reuse values in a decision tree by linking inputs in question and guidance nodes. You can also link inputs of a child tree to a parent tree.
-   Link an activated decision tree to your current decision tree to reuse other decision trees and reduce effort in creating new ones. The linked decision tree acts as a child tree to the current decision tree.
-   Enable users to edit their responses in the previous question nodes or a guidance node.

    In a nested decision tree, users can navigate back to the previous node of a parent tree from a child tree.


## Guided Decisions experiences

The Guided Decisions Experience application provides two different experiences for creating and editing decision trees: through the Decision Tree Builder or the Core UI.

-   Create a graphical diagrammatic representation of nodes and their paths in a troubleshooting process through the Decision Tree Builder. For more information, see [Decision trees in Decision Tree Builder](decision-trees-in-gdb.md).
-   Use forms and lists and edit existing decision trees through the Core UI. For more information, see [Decision trees in Core UI](decision-trees.md).

## Setting up the Guided Decisions Experience application

As an admin, set up the Guided Decisions Experience application to enable users to create and run decision trees by completing the following setup tasks:

-   [Install the Guided Decisions Experience application](../task/install-guided-decisions-exp-app-new.md).
-   [Assign roles to Guided Decisions users](../reference/components-installed-with-guided-decisions.md#section_jym_wrd_ywb) - Use roles to control access to Guided Decisions features and information.
-   [Install the Recommended Actions application](../task/install-recommended-actions-cs-app.md) - Enables decision trees to be run as recommended actions.

## Creating and using decision trees

![Flowchart displaying process of creating decision trees, implementing them, and then using them by different persona.](../image/gd-flowchart.png)

Users with the decision tree author role \(decision\_tree\_author\) create decision trees. After creating a decision tree, the decision tree is implemented by adding it to a recommended action, playbook, or Service Portal. For more information, see the following topics:

-   [Create a decision tree in Decision Tree Builder](../task/configure-decision-trees-gdb.md)
-   [Edit a decision tree in Core UI](../task/configure-decision-trees.md)
-   [Add Guided Decisions to playbooks](../task/add-guided-decision-playbook.md)
-   [Add Guided Decisions to Recommended Actions](../task/add-guided-decisions-to-recommended-actions.md)
-   [Add Guided Decisions to Service Portal](../task/add-guided-decisions-service-portal.md)

Agents interact with decision trees as part of a [recommended action](nba.md) or as part of a playbook within a record, such as a case.

Customers and end-users interact with decision trees on Service Portal.

For guided decisions that are added to playbooks, agents can work through the decision trees and complete actions suggested in the guidance as part of a playbook stage or activity. How the agent interacts with the decision tree depends on the playbook configuration. For more information, see the following topics:

-   [Use Guided Decisions in playbooks to resolve cases](../task/use-guided-decisions.md)
-   [Use Guided Decisions in recommended actions to resolve cases](../task/use-guided-decisions-ra.md)

## Request apps from the ServiceNow Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

