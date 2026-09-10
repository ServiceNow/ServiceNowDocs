---
title: Manually test an agentic AI asset
description: Manually test an AI agent or agentic workflow to verify it functions as defined and achieves the desired objectives.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/test-ai-asset-new.html
release: australia
topic_type: task
last_updated: "2026-06-06"
reading_time_minutes: 4
breadcrumb: [AI Agent Studio, Enable AI experiences]
---

# Manually test an agentic AI asset

Manually test an AI agent or agentic workflow to verify it functions as defined and achieves the desired objectives.

## Before you begin

If you don't have the roles necessary to pass the ACLs of the agentic AI asset and all of its tools, you will be notified that you don't have the necessary access and the test won't execute. The trace log can redirect you to the **Access Analyzer** for additional details.

Decide which records you will test against before you start. Identifiers like record numbers are not offered in the test dialog, and a test that refers to a record needs one that resolves on the instance. If your instance has no suitable records, you can load demo data.

Role required: sn\_aia.admin and either admin or at least one role required by the ACL of the agentic AI asset being tested and each of the ACLs of its downstream components.

## About this task

After you create an AI agent or agentic workflow, test it to verify the agentic AI asset functions as defined. A test shows what the agentic AI asset did, including which tools it called, in what order, and what it returned. There is no additional guidance on individual tests whether the agentic AI asset's behavior is intended and correct. You can run a manual test to evaluate the behavior of your agentic AI asset on a single test record, or you can run an automated evaluation to reveal patterns across multiple executions. See [Evaluate an agentic AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/launch-aia-eval.md) for more details about running an automated evaluation.

You can access the test interface from the node map view or from the guided setup. During a test, you can view a chat session, examine node and card expansions that show different agents or tools within an agentic AI asset, review the trace log containing execution information, and analyze test details.

## Procedure

1.  Navigate to the **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the agentic AI asset you want to test.

3.  In the node map view or guided setup, select **Run test**.

4.  Select a test type: **Single test** or **Evaluation**.

    **Single test** provides a snapshot of agentic behavior on a single test record. **Evaluation** reveals patterns of behavior across multiple executions in an automated way. For more information about running an evaluation, see [Evaluate an agentic AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/launch-aia-eval.md).

    **Note:** You can't test and evaluate the same agentic AI asset at the same time.

5.  Select the AI agent or agentic workflow you want to test from the dropdown.

6.  In the **Version** dropdown, select the version you want to test.

    See [Version control for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/version-control.md) for more information about creating and managing versions.

7.  Under **Objective for your test subject**, choose an objective or write your own.

    Describe what you want your agentic AI asset to accomplish. If the objective refers to a record, the identifier, such as name or number, has to be present on the instance. For example, "help me resolve incident INC0001234." If you invent a record that doesn't exist with that identifier, the run fails when the lookup returns nothing.

8.  Select **Run single test**.

    \[Omitted image "aias-test-modal.png"\] Alt text: Run a test modal showing test type selection between Single test and Evaluation, with objective options and text field to write custom objectives.


## Result

Your agentic AI asset begins to execute the test autonomously to achieve the objective you specified.

**Note:** There is a pause between starting the test and the first output while the chat session initializes. On a busy instance, this can take a noticeable amount of time, during which the panel shows the session opening but no agent activity. Wait for the first message rather than restarting.

During the test, you can view and analyze the following information:

-   A simulated chat session between the invoking user and the agentic AI asset.
-   The node map showing the agents and tools involved in solving the objective. Nodes and cards expand to display different agents within an agentic AI asset or different tools within an agentic AI asset.
-   The **Trace log** containing execution information about how the agentic AI asset processed the objective.

    The trace log lists each execution task, the messages exchanged, and every tool execution with its inputs and outputs. If there's a failure, read it backwards: find the first tool execution whose inputs or outputs are not what you expected. If you need the full record of an execution, open the run in the Execution Plans \[sn\_aia\_execution\_plan\] table using the sys\_id shown in **Test details**.

-   The **Analysis** tab with insights into the execution.

    The Analysis tab summarizes the issues found in the run, tagged by severity, and offers fixes you can apply in context. Check it before working through the trace log by hand. Low-level problems such as a misspelled field or variable name are reported here.

-   The **Test details** tab with specific information about the test run.

A run that reaches the end without an error means the agent executed and its tools returned. It does not necessarily mean that the agentic AI asset functioned as you intended. A run can also end having worked around tool errors, which still reads as a completed run. Judge the outcome from the detail rather than the status.

You can restart the testing process at any time by selecting **Run test**.

A test run stays open until you end it. While a test is running, any other tests or evaluations are blocked. Close the test panel and start a new run to clear the state, and check the **Activity** section if you're unsure whether an earlier run is still open.

