---
title: Test a decision table in Workflow Studio
description: Test your decision table in Workflow Studio before publishing to verify the rules provide the desired outcome for a given set of input data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/test-decision-table-in-decision-builder.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-07-22"
reading_time_minutes: 1
breadcrumb: [Decision tables, Decision tables, Workflow Studio, Build workflows]
---

# Test a decision table in Workflow Studio

Test your decision table in Workflow Studio before publishing to verify the rules provide the desired outcome for a given set of input data.

## Before you begin

You can only test saved decision tables. Create a table with at least one input and result, save it, and then test it. Alternatively, test an existing saved table.

Role required: admin, decision\_table\_admin, decision\_table\_reader, Change manager, or delegated developer

**Note:** Test decision table inputs within the specified maximum input limits. For example, if the limit is 40 characters, confirm that inputs do not exceed this length to avoid incorrect results.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  Select **Test**.

5.  If the table has draft authoring enabled and it has already been published, select whether to test the draft or published version from the **What to test** list.

6.  From the **How to execute** list, select whether to return only the first matching decision or all matching decisions.

7.  Enter input data to test.

8.  Select **Test**.


## Result

The results display, showing either no results or the decisions where your input data matches the conditions. Run additional tests by changing the test parameters and selecting **Test** again.

**Parent Topic:**[Decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/using-decision-builder.md)

