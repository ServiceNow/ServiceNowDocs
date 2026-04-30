---
title: Test a decision table in Workflow Studio
description: Test your decision table in Workflow Studio before publishing to make sure the rules provide the desired outcome for a given set of input data.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using decision tables, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Test a decision table in Workflow Studio

Test your decision table in Workflow Studio before publishing to make sure the rules provide the desired outcome for a given set of input data.

## Before you begin

You can only test saved decision tables. You can either create a table with at least one input and result and then save and test it, or you can test an existing table that has been saved.

Role required: admin, decision\_table\_admin, decision\_table\_reader, Change manager, or delegated developer

**Note:** Test decision table inputs within the specified character limits. For example, if the limit is 40 characters, ensure inputs do not exceed this length to avoid incorrect results.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  Select **Test**.

5.  If the table has draft authoring enabled and it has already been published, select whether to test the draft or published version from the **What to test** drop-down list.

6.  From the **How to execute** drop-down list, select whether you want to return only the first decision where your input matches the conditions or all decisions where your input matches the conditions.

7.  Enter input data to test.

8.  Select **Test**.


## Result

The results of the test are displayed, showing either no results or one or all of the decisions where your input data matches the conditions. You can run additional tests on the table by changing the test parameters and inputs, and selecting **Test** again.

**Parent Topic:**[Using decision tables](../concept/using-decision-builder.md)

