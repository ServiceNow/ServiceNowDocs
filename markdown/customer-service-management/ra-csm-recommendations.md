---
title: Recommendations in Recommended Actions
description: A recommendation is a way to suggest a helpful action to an agent. A recommendation includes the action and any relevant resources and inputs.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Recommendations in Recommended Actions

A recommendation is a way to suggest a helpful action to an agent. A recommendation includes the action and any relevant resources and inputs.

There are three types of recommendations that are provided to agents:

-   **Guidance**: An action that an agent can take or information that they can share.
-   **Decision tree**: A guided flow to troubleshoot an issue and provide a solution.
-   **Field recommendation**: A recommended value to use for a field.

## Creating a recommendation

When you create a recommendation, you can select the type from the New Recommendation screen. This screen lists the available types.

![New Recommendation screen that presents available recommendation types.](../image/ra-new-recommendation-screen.png)

Selecting a type on the New Recommendation screen takes you to the Recommendation form. The selected type is added to the **Action type** field on the Recommendation form.

## Recommendation form

The Recommendation form provides information about a recommendation, including the selected action and any inputs and resource generators that the action requires.

When you create a recommendation, you select an action type and an action. The next steps depend on the action type that you select. For example, guidances and field recommendations require action inputs while decision trees don’t.

When you create a recommendation, provide this information and save the record. After saving, you can see the Action inputs form section. Inputs are parameters that go into an action and enable agents to complete that action. You can select relevant inputs manually, from the context record, context inputs,or from the resource generator.

You can access the recommendation records by navigating to **All** &gt; **Recommended Actions** &gt; **Recommendations**. New recommendations can be created only inside the rules. For more information, see [Create a recommendation](../task/ra-csm-recommendations-create.md).

<table id="table_ic2_qzz_ztb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule

</td><td>

The name of the rule for the context. This field is read-only.

</td></tr><tr><td>

Context

</td><td>

The name of the context that the **Rule** belongs to. This field is read-only.

</td></tr><tr><td>

Name

</td><td>

The name of the recommendation.

</td></tr><tr><td>

Action type

</td><td>

The type of recommendation:-   Guidance
-   Decision tree
-   Field recommendation

This field is automatically filled with the selection from the New Recommendation screen.

</td></tr><tr><td>

Action

</td><td>

The action to select for the recommendation. The available actions are determined by the selection in the **Action type** field.You can also create an action for the selected action type of guidance, decision tree, or field recommendation.

</td></tr><tr><td>

Resource generator

</td><td>

The resource generator to select from the Resource generators list. You can also create a resource generator.

 Guidances and field recommendations can use resource generators to find relevant resources for the action inputs.

 If you change the value in the **Resource generator** field, you must save the recommendation to use the resource generator.

</td></tr><tr><td>

Recommendation hint

</td><td>

Text that tells the agent why a recommendation is being suggested. Hints apply to action types of guidance and decision tree.The hint appears at the top of the action cards in the Recommended Actions side panel.

</td></tr><tr><td>

Order

</td><td>

The order of the recommendations inside the rule.

</td></tr><tr><td>

Active

</td><td>

When enabled, the recommendation is active.

</td></tr><tr><td>

Action inputs

</td><td>

Action types and actions require inputs. These inputs are the parameters that enable agents to complete an action. You can choose static values for action inputs, or you can use a resource generator to supply values.If a context input is available for the context, it appears in the pill picker of the fields in Action inputs section.

</td></tr><tr><td>

Group

</td><td>

Group created by a defined grouping strategy that displays relevant recommendations together.**Note:** You might need to configure the Recommendation form to display the **Group** field. This field is available by default for Workforce Optimization for ITSM users.

</td></tr></tbody>
</table>**Note:** The **Action type**, **Action**, and **Recommendation hint** fields aren’t shown for the AI search resource generator. You can configure the **Action type** and **Action** fields, and mapping between AI search outputs and guidance actions inputs in the Search result mapping related list.

