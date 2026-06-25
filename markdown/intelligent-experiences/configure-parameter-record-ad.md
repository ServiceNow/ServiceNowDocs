---
title: Enable AI agents to securely access parameters in AI Desktop Actions
description: Enable AI agents to securely access stored values, such as credentials and other input data, through Desktop Action Parameter records. Parameters protect sensitive values and provide dynamic inputs to desktop actions during agent execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/configure-parameter-record-ad.html
release: australia
topic_type: concept
last_updated: "2026-05-25"
reading_time_minutes: 4
breadcrumb: [Defined desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# Enable AI agents to securely access parameters in AI Desktop Actions

Enable AI agents to securely access stored values, such as credentials and other input data, through Desktop Action Parameter records. Parameters protect sensitive values and provide dynamic inputs to desktop actions during agent execution.

Only users with the sn\_aia.admin role can create Parameter records. Parameter records store the names of values that an AI agent accesses during desktop action execution. A separate Parameter record is required for each distinct value.

## Parameter record settings

Each Parameter record includes two fields that control how parameter values are stored and retrieved at execution time.

<table id="table_rgx_bfn_3jc"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shared - selected

</td><td>

Makes the parameter available to all users. When selected, only one Parameter Value record can be created under the parameter, and only a user with the sn\_aia.admin role can create it. During execution, the agent always uses the single Parameter Value record regardless of which user triggered the agent.For example, use this setting for a service account or shared API key that all agents use to connect to the same system.

</td></tr><tr><td>

Shared - not selected

</td><td>

Enables multiple users with the sn\_aia.admin or now\_assist\_panel\_user role to create Parameter Value records under the Parameter record to store values. Only one Parameter Value record can be created per user for each Parameter record. If multiple users must trigger the same AI agent, each user must create a Parameter Value record for their own credentials or inputs.

 During execution, the agent retrieves the Parameter Value record that belongs to the user who triggered the agent.

 For example, use this setting when each user connects with their own credentials, such as individual usernames and passwords for an internal application.

</td></tr><tr><td>

Mark As Sensitive

</td><td>

Encrypts values of all associated Parameter Value records. The agent decrypts the value at execution time. When not selected, values are passed to the agent as plain text.For example, enable this setting for passwords, API keys, or any value that should not be visible in plain text in the instance.

</td></tr></tbody>
</table>**Important:**

The **Shared** and **Mark As Sensitive** fields can only be edited when there are no associated Parameter Value records.

## Map parameters to inputs of on-screen task desktop action

In the Design workspace of the AI Desktop Actions application, you can select the **Use parameter** check box for desktop action inputs that must retrieve values from the parameter records during execution.\[Omitted image "ad-use-parameters-check.png"\] Alt text: Use parameter property in the AI Desktop Actions application.

In AI Agent Studio, when you add a desktop action tool that contains inputs configured for parameters, the **Map parameters** section appears in the modal. Each input configured for a parameter is listed by step name and description, with a **Parameter record** drop-down. \[Omitted image "ad-map-parameters-aia.png"\] Alt text: Map parameters section in the desktop action tool modal.

The following rules apply to parameter mapping:

-   All inputs configured for parameters must be mapped to a Parameter record before the desktop action can be saved.
-   The same Parameter record can be mapped to multiple inputs.
-   Each input can only be mapped to one Parameter record.

**Note:** If you specify values for inputs configured for parameters in the agent instructions or in the Now Assist panel, the mapped parameter values override them.

**Important:**

If you update a desktop action in AI Desktop Actions client application after mapping its inputs in AI Agent Studio, the agent continues to use the previous mapping until you reopen the tool configuration and save it again.

If you rename an input in the desktop action, the agent treats it as a new input and the existing mapping for that input is removed. You must remap the renamed input before the desktop action can be saved.

## SSH parameter example

**Note:**

The following example applies to SSH connector, background task desktop actions. For on-screen task desktop actions, parameter values are supplied through the **Map parameters** section in AI Agent Studio and aren't referenced in agent instructions.

Only users with the sn\_aia.admin role can create Parameter records for SSH desktop actions. To store both a username and a password, the AIA admin must create two separate Parameter records, one for the username \(for example, `un_username_group`\) and one for the password \(for example, `un_password_group`\).

Users with the sn\_aia.admin or now\_assist\_panel\_user role can then create Parameter Value records under each Parameter record to store the values. Only one Parameter Value record can be created per user for each Parameter record.

## AI Agent instructions during execution

The following example shows how an AI agent instruction can reference stored parameter names:

`Connect to SSH server and retrieve my session info. Here are my details:```

-   `IP address: 172.27.50.123`
-   `Port: 22`
-   `Retrieve the user name stored in "un_username_group" and the password stored in "un_password_group" parameter records.`

**Note:** When triggering an AI agent, explicitly specify in your instructions whether the credentials are provided directly or stored in Parameter records. If Parameter records are used, clarify that the record names are for reference only and that the agent must retrieve the username and password from those records.

Verify that you use the exact names of the Parameter records. Parameter record names are case sensitive. For example, "UserName" and "username" are treated as different values.

**Related topics**  


[Create a Desktop action parameter record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuration-ssh-username-password-ad.md)

[Create a parameter value record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-parameter-value-record.md)

