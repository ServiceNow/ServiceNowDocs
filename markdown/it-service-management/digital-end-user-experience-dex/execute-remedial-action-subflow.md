---
title: Execute a remedial action subflow
description: Use the Execute remedial action subflow to run a DEX remedial action on a device, and test it in Workflow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/digital-end-user-experience-dex/execute-remedial-action-subflow.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 2
keywords: [remedial action, subflow, Workflow Studio, device remediation]
breadcrumb: [Trigger remedial actions from flows, DEX remedial actions, Configure, Digital End-User Experience, IT Service Management]
---

# Execute a remedial action subflow

Use the Execute remedial action subflow to run a DEX remedial action on a device, and test it in Workflow Studio.

## Before you begin

-   The remedial action is active. To create a custom remedial action, see [Create a remedial action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/digital-end-user-experience-dex/create-remedial-action.md).
-   The target device is online.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Remedial Actions Framework** &gt; **Administration** &gt; **Remedial actions**.

2.  Select the sys ID of the remedial action.

3.  In the Remedial Action parameters related list on the remedial action record, record the column name of each required parameter.

4.  Navigate to **All** &gt; **Configuration** &gt; **Computers**.

5.  Select the device to run the remedial action on, and copy the sys ID of its computer configuration item \(CI\).

    **Warning:** Copy the sys ID of the `cmdb_ci_computer` record, not the sys ID of the agent record.

6.  To track the run, copy the sys ID of a remedial action origin from **All** &gt; **Remedial Actions Framework** &gt; **Administration** &gt; **Remedial action origins**.

    The origin is used to track the run in the remedial action execution record. Each run creates a remedial action execution record.

7.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

8.  Open the list of subflows and filter it by the application - DEX Application and Device Health and the Name **Execute remedial action**.

9.  Open the **Execute Remedial Action** subflow.

10. Select **Test**.

11. Enter the inputs that you prepared.

    |Input|Value to enter|
    |-----|--------------|
    |device\_id|The sys ID of the computer CI.|
    |remedial\_action\_id|The sys ID of the remedial action.|
    |action\_params|A JSON object that maps the column name of each remedial action parameter to its value. If the remedial action has no parameters, enter `{}`.|
    |origin\_sys\_id \(optional\)|The sys ID of the remedial action origin.|

    For example, the `action_params` value for a remedial action with two parameters looks like this:

    ```
    {
      "first_parameter_name": "value",
      "second_parameter_name": "value"
    }
    ```

    **Warning:** The JSON must be formatted correctly. Formatting errors prevent the run.

12. Run the test.

    The subflow triggers the remedial action on the device and waits for the action to complete.

13. Review the subflow outputs.

    If the remedial action completes successfully, the outputs show the message Remedial action completed successfully and a status of completed. For all outputs and messages, see [Execute remedial action subflow inputs and outputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/digital-end-user-experience-dex/execute-remedial-action-subflow-reference.md).


## Result

The remedial action runs on the device, and the subflow outputs report the outcome.

## What to do next

To review the execution record, see [View remedial action execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/digital-end-user-experience-dex/view-remedial-action-execution.md).

**Parent Topic:**[Trigger remedial actions from flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/digital-end-user-experience-dex/Trigger-ra-flow.md)

