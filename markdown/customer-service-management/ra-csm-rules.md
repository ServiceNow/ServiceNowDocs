---
title: Rules in Recommended Actions
description: A rule is a set of conditions that applies to a context. A rule shows recommendations to agents with certain roles for records that meet certain conditions.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Rules in Recommended Actions

A rule is a set of conditions that applies to a context. A rule shows recommendations to agents with certain roles for records that meet certain conditions.

Creating a rule includes the following steps:

-   Selecting the user roles that can see the recommendations associated with the rule.
-   Defining the conditions that apply to the context recordsand context inputs.
-   Creating recommendations for the rule. A recommendation is a way to suggest a helpful action to an agent. A rule can have multiple recommendations.

The Recommended Actions application includes one context record, case context, that you can use to create recommendations for cases. For example, following are some guidance recommendations:

-   Case field level recommendations: This rule includes one recommendation to predict a value for the **Assignment group** field on the Case form.
-   Case side panel recommendations: This rule includes recommendations to view and attach a knowledge article to a case and to attach and add a link to a knowledge article in a comment, work note, or email.

## Apply rules to tables extended from the context table

The rule created in the parent context are inherited by the extended context when you select the [Apply to tables extended from the context table](ra-csm-rules.md#apply-context-extended-table) check box in a rule. The rules inherited from the parent context appear in the Inherited Rules related list of the extended context. Therefore, the recommendations of these rules are passed on to the extended context. Along with the recommendations of the context table, the recommendations of the active rules from the parent context are inherited by the extended context.

## Rule form

The Rule form provides information about the rule, including a description, the selected user roles, and conditions that apply to the table in the associated context.

When you create a rule, provide this information and save the record. After saving, you can see the Recommendations related list.

You can access the rule records by navigating to **All** &gt; **Recommended Actions** &gt; **Rules**. New rules can only be created from within a context. For more information, see [Create a rule](../task/ra-csm-rules-create.md).

<table id="table_urf_5cf_ztb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the rule.

</td></tr><tr><td>

Context

</td><td>

The context that this rule is associated with. This field is auto-populated from the Context form.

</td></tr><tr><td>

Roles

</td><td>

The user roles that can see recommendations for this rule.

</td></tr><tr><td>

Description

</td><td>

A brief description of the rule.

</td></tr><tr><td>

Advanced Condition

</td><td>

The conditions that apply to the records from the context table.If a context input is available for the context, you can build conditions on it along with the context table.

</td></tr><tr><td>

Fields affecting this rule

</td><td>

Fields from the context table that need to be monitored. Changes to these fields generate recommended actions of the type field recommendation for unsaved records.

</td></tr><tr><td>

Active

</td><td>

When enabled, the rule is active.

</td></tr><tr><td id="apply-context-extended-table">

Apply to tables extended from the context table

</td><td>

When enabled, the rule is applied to tables that are extended from the context table.

</td></tr><tr><td>

Order

</td><td>

Determines the order in which the rule is applied.

</td></tr></tbody>
</table>**Related topics**  


[Create a rule in Recommended Actions](../task/ra-csm-rules-create.md)

