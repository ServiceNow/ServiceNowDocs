---
title: Execute remedial action subflow inputs and outputs
description: The Execute Remedial Action subflow runs a DEX remedial action on a device. This topic describes its inputs, outputs, the conditions that prevent a run, and its messages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/execute-remedial-action-subflow-reference.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 2
keywords: [remedial action, subflow, subflow inputs, subflow outputs]
breadcrumb: [Trigger remedial actions from flows, Creating DEX remedial actions, Configure, Digital End-User Experience, IT Service Management]
---

# Execute remedial action subflow inputs and outputs

The Execute Remedial Action subflow runs a DEX remedial action on a device. This topic describes its inputs, outputs, the conditions that prevent a run, and its messages.

## Inputs

The following table describes the inputs that you provide to the Execute Remedial Action subflow. For the procedure, see [Execute a remedial action subflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/execute-remedial-action-subflow.md).

|Input|Required|Description|
|-----|--------|-----------|
|device\_id|Yes|The sys ID of the computer CI \(`cmdb_ci_computer`\) of the device to run the remedial action on.|
|remedial\_action\_id|Yes|The sys ID of the remedial action \(`sn_reacf_remedial_action`\) to run.|
|action\_params|Yes|A JSON object that maps the column name—not the label—of each remedial action parameter to its value. If the remedial action has no parameters, enter `{}`.|
|origin\_sys\_id|No|The sys ID of the remedial action origin \(`sn_reacf_remedial_action_origin`\). The origin is used to track the run in the remedial action execution record.|

## Outputs

<table id="table_nkl_jh5_5kc"><thead><tr><th>

Output

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status\_code

</td><td>

The result of the run: -   Success \(the remedial action ran and the subflow received its result\)
-   Failed \(the subflow didn't run the remedial action—see conditions that prevent a run\)
-   Timeout \(the remedial action started, but the subflow stopped waiting for the result after 15 minutes\)

</td></tr><tr><td>

error\_message

</td><td>

The message that explains a Failed or Timeout result. For details, see [Messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/execute-remedial-action-subflow-reference.md).

</td></tr><tr><td>

output

</td><td>

A JSON object with the details of the run, including the parameters used, the message, and the status that the device reported.

</td></tr></tbody>
</table>## Conditions that prevent a run

The subflow doesn't run the remedial action when any of the following conditions apply:

-   The remedial action ID is not valid, or the remedial action is inactive.
-   The device ID is not valid.
-   The remedial action isn't supported for the operating system of the device.
-   The device is offline.
-   The action parameters aren't valid.

## Messages

The following table describes the messages that the subflow can return.

|Message|Meaning|
|-------|-------|
|Remedial action completed successfully.|The remedial action finished on the device.|
|Remedial action failed to execute.|The remedial action ran on the device but failed.|
|Remedial action was cancelled.|The remedial action was cancelled before it finished.|
|Target device is not reachable \(offline\). Remedial action can't be executed on an offline device.|The device was offline, so the subflow didn't run the remedial action.|
|Remedial action triggered successfully but execution monitoring timed out.|The subflow started the remedial action but stopped waiting for the result after 15 minutes.|
|Remedial action is not available. It may be inactive or the provided ID is invalid. Verify the remedial action configuration and try again.|The remedial action ID is not valid, or the remedial action is inactive.|
|Remedial action is not supported for the target device's operating system.|The remedial action doesn't support the operating system of the device.|

For status values, see [Outputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/execute-remedial-action-subflow-reference.md).

