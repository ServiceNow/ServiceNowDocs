---
title: Edit an automation rule
description: Change which discovered AI assets a rule marks as managed, or update its name or description, by editing an existing automation rule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-configure-automation-rules.html
release: zurich
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Managing AI assets in bulk, Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Edit an automation rule

Change which discovered AI assets a rule marks as managed, or update its name or description, by editing an existing automation rule.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

You can edit an automation rule when your classification needs updating, for example to broaden or narrow the set of assets the rule marks as managed, to point the rule at a different table, or to correct the rule's name or description. You change a rule's conditions the same way you build them when you create a rule. For details about the available tables, fields, and condition logic, see [Create an automation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-create-automation-rule.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Automation rules**.

2.  On the rule you want to change, select the more actions icon and then select **Edit**.

    The **Edit automation rule** page opens with the rule's current settings.

3.  Update the **Rule name** or **Description** to make the rule easier to identify in the rules list.

4.  Change the records the rule evaluates by selecting a different **Table** in the **Define condition** section.

    For the available tables and the fields you can build conditions against, see [Create an automation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-create-automation-rule.md).

5.  Change which assets the rule marks as managed, add, modify, or remove conditions on the **Conditions** tab.

    Each condition consists of a **Field**, an **Operator**, and a value. Rows are joined by **and** or **or** connectors, which determine whether an asset must meet all conditions or any one of them. To remove a condition, select the delete icon on its row.

6.  Select **Activate this rule**.

7.  Select **Save**.

    Your changes are saved to the rule. If the rule is active, it runs with the updated settings at the next scheduled execution. To apply the changes immediately, select **Run now** from the rule's more actions menu.


