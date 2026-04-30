---
title: Configuring Guided Decisions for Public Sector Digital Services
description: Create structured troubleshooting processes for your agents through the ServiceNow Guided Decisions Experience application. Help your agents solve complex issues in a consistent way.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-02-01"
reading_time_minutes: 3
breadcrumb: [Agent tools, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configuring Guided Decisions for Public Sector Digital Services

Create structured troubleshooting processes for your agents through the ServiceNow® Guided Decisions Experience application. Help your agents solve complex issues in a consistent way.

The Guided Decisions Experience application is a tool for authoring and running decision tree flows. A decision tree walks an agent through a troubleshooting process based on a record context. The process asks a series of questions and the agent provides the answers. Based on those answers, the agent receives guidance on the next steps to take in the resolution process. Agents can resolve complex issues faster and more efficiently. .![Guided Decisions psds](../image/psds_config-guided_decisions.png)

Guided Decisions is a decision authoring and execution capability within the scope of the Public Sector Digital Services application. A guided decision guides Public Sector Digital Service agents and managers through a troubleshooting process based on the context of the case they are working on. It asks them questions based on previous answers and gives guidance on the next step in the resolution process. Guided decisions consist of decision trees. A decision tree is a multi-step process consisting of questions, answers, and guidance. Decision trees contain nodes representing one or more questions and the associated decision or guidance paths. Based on the answers, each decision tree leads to an outcome, which can be guidance, a follow-up question, or another decision tree. Public Sector Digital Service agents interact with decision trees as part of a playbook within a case. The playbook containing the guided decision is displayed in the case based on the conditions set up. Public Sector Digital Service agents work through the guided decision, and complete actions suggested in the guidance. To read more about guided decisions, visit the Docs Site for Configuring Guided Decisions.

Recommend prioritized next best actions to agents

-   Recommend both guidance and guided decision trees as next best actions to agents
-   Dynamically rank next best actions based on frequency and priority of recommendations
-   Quickly develop and deploy new guidance via configuration

## Scenarios for using decision trees

Rapidly construct and deploy guided decision trees. Improve the admin experience with an easy, intuitive, non-technical builder interface Reduce build time by rapidly constructing, validating and testing guided decision trees Drive better decisions by passing contextual info seamlessly from decision tree into guidances. Decision trees can help agents resolve the following types of customer issues:

-   Troubleshoot a faulty device, such as a laptop that doesn't work. Use a decision tree to find the cause and provide a fix for the customer.
-   Review a refund request. Use a decision tree to determine whether the customer is eligible for a refund, which can include checking for exceptions and creating tasks.
-   Reset a customer's password. Use a decision tree to walk the agent through the process, such as verifying the customer's identity, trying other options, and, if needed, resetting the password.

## Guided Decisions features

-   Reuse values in a decision tree by linking inputs in question and guidance nodes. You can also link inputs of a child tree to a parent tree.
-   Link an activated decision tree to your current decision tree to reuse other decision trees and reduce effort in creating new ones. The linked decision tree acts as a child tree to the current decision tree.
-   Enable users to edit their responses in the previous question nodes or a guidance node.

    In a nested decision tree, users can navigate back to the previous node of a parent tree from a child tree.


## Guided Decisions experiences

The Guided Decisions Experience application provides two different experiences for creating and editing decision trees: through the Decision Tree Builder or the Core UI.

## Setting up the Guided Decisions Experience application

As an admin, set up the Guided Decisions Experience application to enable users to create and run decision trees.

## Creating and using decision trees

Users with the decision tree author role \(decision\_tree\_author\) create decision trees. After creating a decision tree, the decision tree is implemented by adding it to a recommended action, playbook, or Service Portal. master.

Agents interact with decision trees as part of a Recommended Actions or as part of a playbook within a record, such as a case.

Customers and end-users interact with decision trees on Service Portal.

For guided decisions that are added to playbooks, agents can work through the decision trees and complete actions suggested in the guidance as part of a playbook stage or activity. How the agent interacts with the decision tree depends on the playbook configuration. master.

## Request apps from the ServiceNow Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

