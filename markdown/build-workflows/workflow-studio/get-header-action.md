---
title: Get Email Header action
description: Access an email header value as a data pill in a flow.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Get Email Header action

Access an email header value as a data pill in a flow.

## Roles and availability

Available as a Workflow Studio core action. Process analysts use the flow\_designer role to add an action to a flow and define configuration details.

## Fields

<table id="table_fdl_yhf_kcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email Record

</td><td>

Record from the Email \[sys\_email\] table.

</td></tr><tr><td>

Target Header

</td><td>

Header from the email record. Upon completion of the action, the header value is added as a data pill in the flow.**Note:** If multiple headers have the same name, the action gets the value of the first header that appears.

 This input requires a string value matching an email header name. ServiceNow provides several dedicated email headers.

-   X-ServiceNow-Source
-   X-ServiceNow-SysEmail-Version

</td></tr></tbody>
</table>## Example

In the following example, a process owner adds the Get Email Header action under an inbound email trigger. In the **Email Record** field, the user selects to get an email header from the email that triggered the flow. In the **Target Header** field, the user selects to get the X-ServiceNow-Source header from the email.

![Get Email Header action example](../images/get-email-header-example-configuration.png)

Testing the flow with a sample email record produces the header value as a data pill.

![Sample header value with a unique notification ID.](../images/get-email-header-example-execution-details.png)

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

