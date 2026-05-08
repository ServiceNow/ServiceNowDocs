---
title: Data Stream action design considerations
description: Follow these considerations when creating a Data Stream action and when adding a Data Stream action to a flow to prevent errors and performance issues.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Data Stream actions and pagination, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Data Stream action design considerations

Follow these considerations when creating a Data Stream action and when adding a Data Stream action to a flow to prevent errors and performance issues.

## Considerations when creating a Data Stream action

Create Data Stream actions with these considerations in mind.

-   **Write pagination logic according to third-party requirements**

    Evaluate and understand the format required by your third-party endpoint. For example, you may need to write a script that sets the built-in `getNextPage` variable to true as long as there is a `nextPage` token in the response. If the response does not contain the token, then set the variable to false. Access variables in script using bracket or dot notation. For example, `variables['getNextPage']`. This variable only accepts the Boolean data type. The default value is false.

-   **Ensure that preprocessing scripts do not call a MID Server or pause the action.**

    Data Stream actions require a constant connection to the response stream. They do not support preprocessing scripts that pause the action to call a MID Server or pause the action to wait for a condition or duration. A preprocessing script that pauses the action for any reason returns an error message.

-   **Convert pagination variable data types to perform math operations**

    Pagination variables only support the string data type. To perform math operations, you must convert the value to an integer, perform any required operations, then convert it back to a string.

    ```
    variables['offset'] = (parseInt(variables['offset']) + parseInt(variables['limit'])).toString();
    ```

-   **Ensure that the pagination script has an end condition**

    Avoid infinite loops in pagination requests by creating a condition that sets the `getNextPage` variable to false. Cancel any long-running flows. Always test Data Stream actions before using them in production.

-   **Clear configuration page options carefully**

    Clearing an option in a configuration page removes the step from the Data Stream outline and deletes all data associated with the step.

-   **Consider the size of each page returned**

    When configuring pagination options, try to ensure that the size of each page returned is under one GB. This ensures that flow designers who use the action won't encounter size limit issues when retrieving data from a MID Server. If the action returns more than one GB of data per page, the flow designer may need to increase the attachment size limit. For more information, see [MID Server support for Data Stream actions](dsa-on-mid.md).


**Note:**

-   Nesting Data Stream actions is not supported.
-   When using the retry policy, ensure that you are aware of these considerations:
    -   Only a fixed time interval strategy is honoured for the data stream actions.
    -   The total delay \(count multiplied by the interval\) can't exceed 30 seconds. For example, if you want retry for a maximum of 3 times, the maximum delay for each retry is 10 seconds.
    -   Data stream step doesn’t go into the waiting state during retry.

## Considerations when adding a Data Stream action to a flow

Add a Data Stream action to a flow with these considerations in mind.

-   **Do not add actions with wait conditions to a Data Stream For Each logic block**

    You cannot add an action that pauses the flow to a Data Stream For Each flow logic block. Data Stream actions require a constant connection to the response stream. For example, you cannot use the Ask for Approval or Wait for Condition actions within Data Stream For Each flow logic.

    Some actions and steps always pause a flow and cannot be added to Data Stream For Each flow logic blocks. However, some actions and steps may pause the flow depending on how they are configured. Check the action configuration to ensure it does not pause the flow at runtime.

<table id="table_mwj_dgw_3jb"><tbody><tr><td rowspan="4">

**Always pauses the flow \(unsupported with Data Stream actions\)**

</td><td>

Ask for Approval action

</td></tr><tr><td>

Ask for Approval step

</td></tr><tr><td>

Wait for Condition action

</td></tr><tr><td>

Wait for Condition step

</td></tr><tr><td rowspan="3">

**May pause the flow depending on configuration**

</td><td>

Create Catalog Task action

</td></tr><tr><td>

Create Task action

</td></tr><tr><td>

Create Task step

</td></tr></tbody>
</table>-   **Do not add actions that run on the MID Server to a Data Stream For Each logic block**

    Some actions and steps always run on a MID Server and cannot be added to Data Stream For Each flow logic blocks. However, some actions and steps may run on a MID Server depending on how they are configured. Check the action configuration to ensure it does not run on the MID Server at runtime.

<table id="table_r4b_thw_3jb"><tbody><tr><td rowspan="3">

**Always runs on a MID Server \(unsupported with Data Stream actions\)**

</td><td>

JDBC step

</td></tr><tr><td>

PowerShell step

</td></tr><tr><td>

SSH step

</td></tr><tr><td rowspan="3">

**May run on a MID Server depending on configuration**

</td><td>

REST step

</td></tr><tr><td>

Script step

</td></tr><tr><td>

SOAP step

</td></tr></tbody>
</table>-   **Turn off reporting when consuming a large number of records in the For Each logic block**

    Iterating over a large number of records can be resource intensive, especially when the For Each logic block includes complex actions for each iteration. To avoid performance issues, turn off reporting using the **com.snc.process\_flow.reporting.level** system property. For more information, see Workflow Studio flow system properties.


**Parent Topic:**[Data Stream actions and pagination](data-stream-actions.md)

