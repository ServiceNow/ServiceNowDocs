---
title: Proactive Action form
description: When creating a Proactive Triggers rule, the Proactive Action form includes the following fields.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Proactive Triggers reference, Proactive Triggers, Manage people and work, Conversational Interfaces]
---

# Proactive Action form

When creating a Proactive Triggers rule, the Proactive Action form includes the following fields.

<table id="table_pff_wh1_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the action that you want to associate with a rule.

</td></tr><tr><td>

Description

</td><td>

Description of the action to be applied.

</td></tr><tr><td>

Applies to

</td><td>

The set of end users to which this action applies. For example, you can apply an action to any **Any Users** or **Guest Users** user criteria. Use the lookup using list icon \(![Lookup using list con.](../image/look-up-icon.png)\) to select the user. The **Applies to** settings must be unique for the actions for each rule. To create a user criteria record, see [Create a user criteria record for Service Portal](https://www.servicenow.com/docs/access?context=create-user-criteria-record&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

 **Note:** If you don't specify a user, this rule is applied to all users.

</td></tr><tr><td>

Model Type

</td><td>

Topic type, either an **LLM** or **NLU/Keyword** value, that is associated with the Proactive Triggers action. This field is only applicable if Now Assist is installed and enabled.

</td></tr><tr><td>

Topic

</td><td>

List of Virtual Agent topics available. The selected topic runs when end users open the Proactive Triggers message.**Note:** Only the topics that are active and published appear in the list. System topics aren't included in the topics list.

\(For **Message that launches a virtual agent topic** actions only.\)

</td></tr><tr><td>

Active

</td><td>

Option to activate the action.

</td></tr><tr><td>

Order

</td><td>

Order of when a Proactive Triggers action is to be applied. If there's more than one action, the actions with lower numbers are applied first.

</td></tr><tr><td>

Rule

</td><td>

Rule to which this action applies.

</td></tr><tr><td>

Select variables from

</td><td>

Option for choosing from a list of variables to use in the message. Choices are:-   Trigger Type: References the trigger type table selected for the rule.
-   User: References the user table. Uses the attributes in the user table for the Proactive Triggers message.

</td></tr><tr><td>

Message

</td><td>

Text that the end users see when the action is applied. To enter the text, you can:-   Use the tools and options of the HTML editor.

**Note:** Support for using the link button may be included in future releases.

-   Use variables \(Trigger Type or User\).

</td></tr><tr><td>

Tagline

</td><td>

Text that the end users see above the buttons that you've created. The default tagline text is `Suggested for you`.\(For **Message that launches a selection of virtual agent topics** actions only.\)

</td></tr></tbody>
</table>**Parent Topic:**[Proactive Triggers reference](proactive-triggers-reference.md)

