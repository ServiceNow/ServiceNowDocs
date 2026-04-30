---
title: Proactive Rule form
description: When creating a Proactive Triggers rule, the Proactive Rule form includes the following fields.
locale: en-US
release: xanadu
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Proactive Triggers reference, Proactive Triggers, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Proactive Rule form

When creating a Proactive Triggers rule, the Proactive Rule form includes the following fields.

<table id="table_fdr_hvz_5vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new rule that you want to create.

</td></tr><tr><td>

Type

</td><td>

Proactive Triggers conversation type for end users. Choices are:-   Virtual Agent

Rules are triggered when the Virtual Agent is available.

-   Live Agent only

Rules are triggered when the web client is configured to live agent only. You can configure the web client to live agent only from the Service Portal. For instructions, see [Configure Agent Chat in a portal](https://www.servicenow.com/docs/access?context=configure-va-in-sp&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).


</td></tr><tr><td>

Description

</td><td>

Rule description.

</td></tr><tr><td>

Order

</td><td>

Order of when a Proactive Triggers rule is to be applied. If there’s more than one rule, the rules with lower numbers for a particular delay time are applied first.

</td></tr><tr><td>

Active

</td><td>

Option to activate the rule.

</td></tr><tr><td class="sub-head" colspan="2">

When to run the trigger

</td></tr><tr><td>

Frequency

</td><td>

How often the rule should be applied. Choices are:-   Every time: Every time an end user visits the page.
-   Once per visit: Every time an end user visits a page per user log in.
-   Once per user: Applies the rule only the first time that an end user visits the page. With this frequency setting, you must clear the rule's history if you want to run this rule again for a user. For more information about clearing the rule history, see [Multiple Proactive Triggers rules and actions](../concept/multiple-rules-and-actions.md).

</td></tr><tr><td>

Delay time

</td><td>

Time to wait before the rule is applied. Choices are:-   None
-   10 seconds
-   20 seconds
-   30 seconds
-   1 minute
-   3 minutes

</td></tr><tr><td class="sub-head" colspan="2">

What initiates the trigger

</td></tr><tr><td>

Trigger type

</td><td>

System API or web browsing URL for the type of trigger. Select the lookup list icon \(![Lookup using list icon.](../image/look-up-icon.png)\) to view your default choices.

 If enabled, your default system API choice is **Search Event**. This trigger type triggers an action when no search results are found on the Service Portal or Employee Service Center.

**Tip:** Ensure that your Proactive Trigger business rule \(**Proactive Trigger on Search**\), trigger type \(**Search Event**\), rule \(**Search - No Search Result**\), and action \(**No Search Result Message**\) have the **Active** option turned on so that this rule runs effectively. These parameters default to inactive.

 Your default web browsing URL choices are:

 -   **Catalog item**: Triggers an action based on the catalog item's reference fields.
-   **Knowledge**: Triggers an action based on the knowledge article's reference fields.
-   **Portal home**: Triggers an action based on the portal home page's reference fields.
-   **URL**: Triggers an action based on the defined URL.

Define the URL components as shown in this example.

![URL trigger type format example.](../image/url-trigger-type.png)

**Important:**

    -   If you're using the Virtual Agent web client outside of the ServiceNow instance \(for example, as part of a third-party website\), use the URL trigger type. Don't use any of the other trigger types.
    -   The URL trigger type applies only if no other available trigger types match the URL.

 If you don’t see the trigger type that you need using the lookup list icon \(![Lookup using list icon.](../image/look-up-icon.png)\), you can create your own custom trigger type. For more information about custom trigger types, see [Create custom trigger types](../task/create-custom-trigger-types.md).

</td></tr><tr><td>

Conditions

</td><td>

Conditions that must be met for the trigger type to run as defined by the admin. Conditions vary by trigger type. Specify the Proactive Triggers conditions that you want to use.For more information about using conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

 **Note:** Rule conditions are case-sensitive and must match. For example, if you want to use the name of a catalog item, such as the iPhone condition, entering "iphone" doesn't give you the results that you want.

![Proactive Triggers conditions.](../image/specify-conditions.png)

**Note:** When specifying the conditions that must be met for a trigger type, be careful not to specify conflicting trigger types and conditions. Conflicting URL trigger types and conditions can cause errors. For more information, see [Manage Proactive Triggers](../concept/manage-proactive-triggers-2.md).

</td></tr><tr><td>

Advanced conditions

</td><td>

Option for using scripts to define the condition.![Specify advanced conditions.](../image/specify-advanced-conditions.png)

</td></tr><tr><td>

Find available agent

</td><td>

Option to check for any available live agents.

</td></tr></tbody>
</table>**Parent Topic:**[Proactive Triggers reference](proactive-triggers-reference.md)

