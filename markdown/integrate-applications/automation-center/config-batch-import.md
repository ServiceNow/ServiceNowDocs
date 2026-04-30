---
title: Configure batch import for data
description: Configure batch import of data to specify the pagination method for importing large data sets.
locale: en-US
release: yokohama
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring data import, Create an automation source, Working with Connection Manager, Using Automation Center, Automation Center, Data and Automation]
---

# Configure batch import for data

Configure batch import of data to specify the pagination method for importing large data sets.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

Proceed from the **Select an action** section. For information on selecting a spoke, see [Select an action](select-action.md).

## Procedure

1.  Provide the details on the form.

<table id="id_jw3_jvk_4tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action details

</td><td>

Review input and output details to customize the data flow for your specific needs.

</td></tr><tr><td>

Select output type

</td><td>

Select the output type value from the list. Only actions that have the output type as "array.output" have a value displayed here.

</td></tr><tr><td>

Select batch import method

</td><td>

Select a batch import method.The right batch import method helps to manage data efficiently. Batching can help improve performance, handle errors, and ensure data freshness in large imports.

The following batch import methods are available:

-   **None**: Import data in a single request. Select this if you do not want to use the pagination method provided in Automation Center.
-   **Offset**: Import data in batches using an offset value.
-   **Time based**: Import data in batches based on time intervals.
-   **Token based**: Import data in batches using a continuation token.


</td></tr><tr><td>

Generate flow template

</td><td>

Select this button to generate a flow.After the flow is generated, edit it to set up input parameters and pagination for large imports.

-   Establish the necessary input parameters \(static or dynamic\): For example, when you import automation records from a third-party tool, send a dynamic value such as Automation Status, or a static value such as "Retry Limit = 3".
-   Link pagination for large data sets: For example, if you have 1,000 or more automation records, setup the pagination to process 100 records per page by indicating both the page number and page size.


</td></tr></tbody>
</table>    The flow is generated and you are guided to edit the flow.

2.  Select **Continue to edit flow**.

    The Workflow Studio page is displayed.

    **Note:** Edit the flow as per your requirement. For information on editing a flow, see [Edit flow in Workflow Studio](cm-edit-flow-ac.md).

    Do not activate the flow at this point.

3.  Select **Verify flow** to verify if the flow is correct.

    This step verifies if the selected action is available in the flow.

4.  Select **Save and continue**.

    The **Verify and test** section is displayed.


-   **[Edit flow in Workflow Studio](cm-edit-flow-ac.md)**  
Edit the flow to confirm that the pagination is implemented correctly. This confirms that the data is imported correctly.

**Parent Topic:**[Configuring data import](../concept/configure-data-import.md)

