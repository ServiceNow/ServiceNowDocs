---
title: Recommended Actions
description: Use Recommended Actions to display relevant actions to agents based on a context of a record or recommend a value for a field.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Recommended Actions

Use Recommended Actions to display relevant actions to agents based on a context of a record or recommend a value for a field.

## Action types in Recommended Actions

<table id="table_bdn_g3y_zyb"><thead><tr><th>

Action type

</th><th>

Description

</th><th>

Use cases

</th></tr></thead><tbody><tr><td>

**Guidance**

</td><td>

A guidance is an action that an agent can take or information that an agent can share.

-   Guidances appear as cards in the contextual side panel in a workspace.
-   Agents can access these cards by selecting the Recommended Actions icon in the side panel.
-   Agents can perform the action by selecting the button on the card.

</td><td>

-   Mary created a case to report an issue with a router. The agent assigned to this case is recommended to apply a resolution from a solved case to resolve the customer issue. The resolution notes and a resolution code from the solved case are copied into the Closure Information section of the current case.
-   Paul, who has an account with StellarVest bank created a case to report a loss of credit card. The agent assigned to this case is recommended to create a work order to dispatch a new credit card for Paul.

</td></tr><tr><td>

**Field recommendation**

</td><td>

A field recommendation is a value that is recommended for a field. Depending on the configuration, the recommended field values are auto-filled or shown as messages underneath the fields for the new records. The recommended field values are shown as messages only underneath the fields for the existing records.

-   You can configure the fields with the text and values that appear in the messages.
-   You can also configure a confidence threshold to auto-fill a recommended value.
-   You can configure a preference to auto-fill a recommended value.

</td><td>

-   An agent wants to reassign the case to a different team who is better equipped to resolve a customer issue. A field recommendation can recommend the assignment group based on the text in the case short description.
-   While interacting with a customer, an agent creates a case on behalf of the customer. Based on the short description the agent enters in the case form, the values for the fields **Product**, **Assignment group**, and **Assigned to** are recommended to the agent.

</td></tr><tr><td>

**Decision tree**

</td><td>

A decision tree is a guided flow for agents to follow. A decision tree is a multi-step process that asks a series of questions. Based on the answers that an agent enters, a guidance is provided.**Note:** The Guided Decisions application \(sn\_gd\_core\) is required to create decision trees.

</td><td>

Rina created a case to report that their phone isn’t charging. The agent assigned to the case is recommended to use a decision tree that asks a series of questions to troubleshoot the issue with the phone and provides a guidance in the end.

</td></tr></tbody>
</table>Actions of the type **Guidance** and **Guided Decision Tree** are displayed as cards within the contextual side panel.

![Guidance cards recommending the agent to view and attach a knowledge article or attach and add the link in comment as primary action](../image/ra-guidance-type.png "Recommended actions - guidance card")

Actions of the type **Field Recommendation** are auto-filled in the fields or appear as messages under the fields on a record form. Agents can follow the recommendations and select these field values.

![Case form showing highlighted field recommendations under the appropriate fields. For example, based on short description, service desk is the recommended field for assignment group.](../image/ra-field-recommendations-short-desc.png "Field recommendation messages in the Incident form")

For more information, see [Creating guidance and field recommendation in Recommended Actions](ra-csm-config-recommendations.md).

## Elements for configuring recommended actions

Configuring a recommended action is a multi-step process that involves:

-   **Context**

    A context enables agents to see recommended actions for a record in that table when certain rules are met. For more information, see [Contexts in Recommended Actions](ra-csm-contexts.md).

-   **Context input**

    A context input enables you to utilize the entities other than the context table to define rules, recommendations, and resource generators so that recommendations are updated dynamically as the context changes. For more information, see [Context inputs in Recommended Actions](ra-csm-dynamic-context-inputs.md).

-   **Rule**

    A rule is a set of conditions that applies to a context and determines when a recommended action appears for records in the context table. For more information, see [Rules in Recommended Actions](ra-csm-rules.md).

-   **Recommendation**

    A recommendation is a way to suggest an action to an agent. You can create recommendations with action types of guidance and field recommendation. For more information, see [Recommendations in Recommended Actions](ra-csm-recommendations.md).

-   **Resource generators**

    Resource generators provide helpful information for guidance and field recommendations. The resource generators use decision table, flow, scripts, Predictive Intelligence framework, or AI search capabilities to generate resources. For example, a resource generator can provide a knowledge article link that can then be used as a recommended action for a case. For more information, see [Resource generators in Recommended Actions](ra-csm-resource-generators.md).

-   **Arbitration parameters**

    Arbitration parameters determine the frequency of issues or the priority order of the recommended actions so that agents get the guidance that they must help resolve customer issues.


