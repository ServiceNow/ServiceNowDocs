---
title: Create a recommendation in Recommended Actions
description: Create a recommendation with an action type of guidance, field recommendation, or guided decision tree to suggest helpful actions to agents.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Create a recommendation in Recommended Actions

Create a recommendation with an action type of guidance, field recommendation, or guided decision tree to suggest helpful actions to agents.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, or admin

## About this task

You select an action type and action as part of creating a recommendation. The next steps depend on the action type that you select. For example, guidances and field recommendations need action inputs as a next step, while guided decision trees don’t.

For the AI search resource generator, you can select guidances only as action types in the Search result mapping related list. You must map the fields from the search source table with guidance action inputs for AI search or fields from the genius result configuration with guidance action inputs for genius results.

Then you define the action inputs, which are the parameters that enable agents to complete an action. You can select static values for inputs or use a resource generator to supply values.

**Note:** New recommendations can only be created inside the rules.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**.

2.  Select a context.

3.  Select a rule in the Rules related list.

4.  In the Recommendations related list, select **New**.

5.  Select the type of recommendation to create from the New Recommendation screen.

    -   A specific action to take or information to review \(guidance\)
    -   A guided flow to follow \(guided decision tree\)
    -   A field value to use \(field value recommendation\)
    A new Recommendation form is displayed with the **Rule**, **Context**, and **Action type** fields auto populated.

6.  In the **Name** field, enter a name for the recommendation.

7.  In the **Action** field, select an action.

    The available actions are determined by the selection in the **Action type** field.

    1.  In the **Action** field, select the lookup icon.

        In the resulting pop-up window, the **Table name** field is auto populated with the table that stores the available actions for the selected action type.

    2.  In the **Document** field, select the desired action by clicking the lookup icon.

        You can also create an action of type guidance, field recommendation, or guided decision tree. For more information, see [Creating guidance and field recommendation in Recommended Actions](../concept/ra-csm-config-recommendations.md).

    3.  Select **OK**.

    4.  Save the record to display the Action inputs form section.

        After selecting the action type and action, saving the record displays the required action inputs.

8.  In the **Resource generator** field, select or create a resource generator and then save the record.

    For more information, see [Create a resource generator in Recommended Actions](ra-csm-resource-generators-create.md). Guidances and field value recommendations can use resource generators to find relevant resources for the action inputs.

    The **Action type**, **Action**, and **Recommendation hint** fields are not available for AI search resource generator. You can select the action type as a guidance and an action when you configure the search result mapping for AI search. For more information, see [Map AI search results with guidance inputs in Recommended Actions](ra-create-search-result-mapping-for-ai-search.md).

9.  For guidances and guided decision trees: in the **Recommendation hint** field, enter a hint text.

    The hint explains to agents why a recommendation is being suggested.

10. Select a group in the **Group** field to show relevant recommendations together.

    **Note:** You might need to configure the Recommendation form to display the **Group** field. This field is available by default for ITSM Workforce Optimization users.

11. Define the action inputs.

    Action types and actions need inputs. These parameters enable agents to complete an action. You can choose static values for action inputs or you can use a resource generator to supply values.

<table id="choicetable_gx1_2sx_f5b"><tbody><tr><td id="d64258e308">

**Use a static value**

</td><td>

Enter the value in the field in the input field or use the lookup icon to select a value from the list.

</td></tr><tr><td id="d64258e317">

**Use a pill picker**

</td><td>

1.  Select the pill picker next to the field.
    -   The context is available in the pill picker.
    -   If you selected a **Resource generator**, the outputs from the generator are available in the pill picker.
    -   If an active context input is available for a context, the context input appears in the pill picker.
2.  Select the outputs from the pill picker.


</td></tr></tbody>
</table>12. Select **Update**.


