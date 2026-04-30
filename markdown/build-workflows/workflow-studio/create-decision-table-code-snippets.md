---
title: Create decision table code snippets
description: Create code snippets of published decision tables in Workflow Studio to execute the decision table from any script and make it easier to replace hard-coded logic with decisions.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using decision tables, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create decision table code snippets

Create code snippets of published decision tables in Workflow Studio to execute the decision table from any script and make it easier to replace hard-coded logic with decisions.

## Before you begin

If you have draft authoring enabled, you must publish your decision table to be able to copy a code snippet of the table. If draft authoring is not enabled, save your decision table to access this feature.

The ability to copy code snippets for a decision table enables you to quickly insert the table into your script without having to author the code using API documentation. For more information about the Decision table API, see [DecisionTableAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=DecisionTableAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

Role required: none

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Open a published decision table.

4.  Select the Decision table menu options icon \(![](../image/dec-table-menu-options.png)\) and select **Create Code Snippet**.

    Two code snippets are generated. The first code snippet calls the GetDecision\(\) API, which returns only the first result that matches the inputs and specifications in the decision table. The second code snippet calls the GetDecisions\(\) API, which returns a list of all the results that match your inputs.

5.  Select either **Return first decision that matches** or **Return all decisions that match** depending on which code snippet you need.

6.  Select **Copy Code**.

7.  If you want to copy the other code snippet, select **OK** to close the confirmation message, and copy the code from the other option.

8.  Insert the code snippet into your script where you want to call the decision table and define the data to use for each input variable.


**Parent Topic:**[Using decision tables](../concept/using-decision-builder.md)

