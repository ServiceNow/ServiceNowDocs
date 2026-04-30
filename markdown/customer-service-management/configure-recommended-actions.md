---
title: Configuring the Recommended Actions application
description: As an admin, configure the Recommended Actions application to display relevant actions to your agents based on a record context.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-10-17"
reading_time_minutes: 2
breadcrumb: [Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Configuring the Recommended Actions application

As an admin, configure the Recommended Actions application to display relevant actions to your agents based on a record context.

## Recommended actions

You can configure recommended actions by following these steps.

<table id="table_jm3_lm4_15b"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Create a context](../task/ra-csm-contexts-create.md)

</td><td>

A context enables agents to see recommendations for records from a specific table, such as the Case table.

</td></tr><tr><td>

[Create a rule for a context](../task/ra-csm-rules-create.md)

</td><td>

A rule is a set of conditions that applies to a context and determines when a recommended action appears.

 When you create a rule:

-   Select conditions that apply to the context table.
-   Select the roles that have access to the recommended actions.

**Note:** New rules can only be created from within a context.

</td></tr><tr><td>

[Create a recommendation for a rule](../task/ra-csm-recommendations-create.md)

</td><td>

A recommendation is a way to suggest an action to an agent.

 Create a recommendation by selecting one of the recommendation types available on the New Recommendation screen:

-   Guidance
-   Guided decision tree
-   Field recommendation

**Note:** New recommendations can only be created from within a rule.

</td></tr></tbody>
</table>## Action types

With the Recommended Actions application, you can create the following types of actions for agents to take.

<table id="table_nxk_y1t_c5b"><thead><tr><th>

Action type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Guidance

</td><td>

An action that an agent can take or information that they can share. For example, a guidance can recommend that an agent can view and attach a knowledge article to a case or create a work order.

</td></tr><tr><td>

Guided decision tree

</td><td>

A guided flow to follow. A decision tree is a multi-step process that includes a series of questions and answers and results in guidance.

</td></tr><tr><td>

Field recommendation

</td><td>

A recommended value to use for a field. For example, this type of action can recommend the assignment group based on the text in the case short description.

</td></tr></tbody>
</table>For more information, see [Creating guidance and field recommendation in Recommended Actions](ra-csm-config-recommendations.md).

## Resource generators

Configure resource generators to provide information that you can use as inputs to actions such as guidances and field recommendations. Configuration of decision trees do not require resource generators. For more information, see [Create a resource generator in Recommended Actions](../task/ra-csm-resource-generators-create.md).

## Arbitration parameters

Configure arbitration parameters to determine the frequency of issues or the priority order of the recommended actions so that agents get the guidance that they need to help resolve customer issues. For more information, see [Configure the arbitration parameters in Recommended Actions](configure-nba-arbitration-param.md).

