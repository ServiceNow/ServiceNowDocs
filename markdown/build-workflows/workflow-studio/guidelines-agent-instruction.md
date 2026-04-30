---
title: Guidelines for writing AI agent instructions
description: Review the guidelines to write affective instructions for the AI agents to complete your Agentic Playbooks activity.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-10-13"
reading_time_minutes: 1
breadcrumb: [Reference, Agentic Playbooks, Playbooks, Explore, Workflow Studio, Build workflows]
---

# Guidelines for writing AI agent instructions

Review the guidelines to write affective instructions for the AI agents to complete your Agentic Playbooks activity.

<table id="table_urm_mwq_ygc"><thead><tr><th>

Guideline

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provide step-by-step instructions

</td><td>

Break down complex operations into individual steps.If you need to perform operations like count, high, or low, write each operation out, step by step.

</td></tr><tr><td>

Verify that all columns can be queried

</td><td>

Check the Knowledge Graph to confirm that the columns can be queried

</td></tr><tr><td>

Use specific column names

</td><td>

-   Make sure column names are correct in your instruction.
-   If agent doesn't understand the column value that you're giving, try to give an example. For example, if an agent returns a sys\_id instead of a number, you could tell the agent to Retrieve Incident numbers like INC000081.

</td></tr><tr><td>

Write conversationally

</td><td>

Write instructions in plain English.

</td></tr><tr><td>

Use meaningful names and labels for activities and other nodes

</td><td>

Rename tables and other nodes for clarity. For example, if a table named **abcd** contains employee data, rename it to **Employees**.**Note:** This is especially important if you are using custom Knowledge Graph for the workflow.

</td></tr><tr><td>

Test and revise instructions

</td><td>

Test your instructions and check for accurate AI agent behavior for your use cases.

</td></tr><tr><td>

Emphasize critical steps

</td><td>

Highlight important steps to ensure they are not skipped. Use keywords like Mandatory, Required, or Important.

</td></tr><tr><td>

Specify query operations

</td><td>

Using the keyword Query helps our data gathering AI agent to pick the more effective Knowledge Graph over the AI search.

</td></tr></tbody>
</table>**Parent Topic:**[Agentic Playbooks reference](agentic-playbook-reference.md)

