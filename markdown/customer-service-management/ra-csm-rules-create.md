---
title: Create a rule in Recommended Actions
description: Create a rule for a context that determines when recommended actions are made available to agents.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Create a rule in Recommended Actions

Create a rule for a context that determines when recommended actions are made available to agents.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, or admin

## About this task

New rules can be created from the context records only.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**.

2.  Select a context.

3.  In the Rules related list, click **New**.

4.  Select the rule that you want to update.

5.  Enter a name and a description for the rule.

6.  In the **Roles** field, select the user roles that can see recommendations for this rule.

7.  Click **Done** on the Roles pop-up window.

8.  In the **Advanced Condition** field, use the condition builder to add one or more conditions that apply to the records for this context.

    Agents can see recommendations for the records in the context table that meet this criteria.

    If a context input is available for the context, you can build conditions on it along with the context table.

9.  Enable the **Apply to tables extended from the context table** check box, so that the rule and its recommendations are applied to tables that are extended from the context table.

    For more information, see [Apply rules to tables extended from the context table](../concept/ra-csm-rules.md#section_rules-apply-extended-tables).

10. In the **Fields affecting this rule** field, add fields from the context table that must be monitored for changes.

    Changes to these fields generate recommended actions of the type field recommendation for unsaved records.

11. Fill in the remaining fields on the form, as needed.

    For more information about these fields, see [Rule form](../concept/ra-csm-rules.md#section_rnp_zsz_ztb).

12. Click **Submit**.


