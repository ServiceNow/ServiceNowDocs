---
title: Set rule-based finding definitions using Classic view
description: Configure rule-based finding definitions to deliver discovered insights to your Summary and Insights page.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting improvement opportunities from Classic view, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Set rule-based finding definitions using Classic view

Configure rule-based finding definitions to deliver discovered insights to your Summary and Insights page.

## Before you begin

-   You can create one configuration per table for each project based on a process.
-   You can create a rule-based finding definition from the Process Configurations page or the Projects page.
-   Role required:
    -   The sn\_process\_optimization\_admin and sn\_process\_optimization\_power\_user roles can create a finding definition for a project.
    -   The sn\_process\_optimization\_analyst role can view a finding definition for a project, but can’t create, edit, or delete a definition.

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Projects** &gt; **All Projects**.

2.  Select a project.

3.  Select **New** under the **Project Finding Definitions**.

4.  On the form, fill in the fields.

    For a description of the field values, see [Rule-based finding definition form from Classic view](../reference/finding-def-form.md).

5.  Select **Submit**.


## What to do next

-   Create finding rules. For steps on this process see [Configure finding rules](configure-finding-rule.md).
-   Create finding constraints. For steps on this process, see [Configure finding constraints](configure-finding-constraint.md).

-   **[Configure finding rules](configure-finding-rule.md)**  
Configure finding rules for your finding definition. Finding rules define what record criteria triggers your finding definitions.
-   **[Configure finding constraints](configure-finding-constraint.md)**  
Configure finding constraints for your finding definition. In addition to finding rules, finding constraints further narrow down the scope of your finding definitions using metrics like duration and relation constraints.
-   **[Example use case: a-b-a transitions](aba-example.md)**  
Use finding rules to identify when records return to a previous state.

**Parent Topic:**[Setting improvement opportunities from Classic view](../concept/impr-opp-classic-project.md)

