---
title: Create an automation rule
description: Set the conditions for automatically marking discovered AI assets as managed by creating a custom automation rule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-create-automation-rule.html
release: australia
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Managing AI assets in bulk, Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Create an automation rule

Set the conditions for automatically marking discovered AI assets as managed by creating a custom automation rule.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

An automation rule queries a table for AI assets that meet the conditions you define and marks the matching assets as managed. Once activated, the rule runs at the next scheduled execution. To run a rule immediately after creating it, use the **Run now** action from the rules list.

You can create up to 10 rules and have up to 5 active at a time. If you reach the active rule limit, deactivate an existing rule before activating a new one.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Automation rules**.

2.  Select **Create rule**.

3.  Identify the rule by entering a **Rule name** and an optional **Description**.

    Use a name that reflects what the rule does, such as *Mark all generative AI systems as Managed*. The description appears in the rules list and helps other AI stewards understand the rule's purpose.

4.  In the **Define condition** section, select the **Table** the rule queries against.

    Choose the table that holds the records you want to evaluate:

    -   **Asset** — Use to write conditions against AI asset records, such as asset state, asset type, or creation date.
    -   **Asset Usage** — Use to write conditions against asset usage records, such as how an asset has been used over time.
    The available fields are the same for both tables. The table selection determines the records the rule evaluates, not the conditions you can build.

5.  On the **Conditions** tab, build the criteria that an asset must meet for the rule to mark it as managed.

    1.  Select a **Field** from the table.

    2.  Select an **Operator** and enter or select the value to compare against.

    3.  To add another condition row, select **+ Add group**.

        New rows are joined to the previous row by an **and** connector by default, requiring an asset to meet all conditions to qualify. To branch the logic so an asset qualifies if it meets either condition, select **or** on the connector between the rows.

6.  On the **Sort by** and **Group by** tabs, configure how the rule's results are ordered or grouped when the rule runs.

7.  To run the rule at the next scheduled execution after saving, select **Activate this rule**.

    Leave this option clear if you want to review the rule in the rules list before activating it. You can activate the rule later by selecting **Activate** from the **Actions** menu on the rule's row.

8.  Select **Save**.

    The rule appears in the **Automation rules for Managed assets** list. If you activated the rule, it runs at the next scheduled execution. To run it immediately, select **Run now** from the rule's **Actions** menu.


