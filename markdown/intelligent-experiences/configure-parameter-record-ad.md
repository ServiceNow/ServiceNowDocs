---
title: Enable AI agents to securely access SSH parameters in AI Desktop Actions
description: Enable AI agents to securely access credentials, such as usernames and passwords, through Desktop Action Parameter records. This approach protects sensitive values during desktop action execution without exposing them in agent instructions.Create a Parameter record with a name that you can reference in your instructions so the AI agent can securely sign in to the SSH server and execute commands.Create Parameter Value records for storing the actual username and password values so that AI agents can securely connect to the SSH server.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-02-16"
reading_time_minutes: 3
breadcrumb: [Defined desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# Enable AI agents to securely access SSH parameters in AI Desktop Actions

Enable AI agents to securely access credentials, such as usernames and passwords, through Desktop Action Parameter records. This approach protects sensitive values during desktop action execution without exposing them in agent instructions.

**Note:** Currently, Parameter and Parameter Value records are only supported for SSH connector, background task desktop actions.

Only the users with the sn\_aia.admin role can create Parameter records for various parameters that the AI agent securely accesses during desktop action execution. To store both a username and a password, the AIA admin must create two separate Parameter records, one for the username "un\_username\_group" and one for the password "un\_password\_group".

Then, users with the sn\_aia.admin or now\_assist\_panel\_user role can create Parameter Value records under the Parameter record to store the values. For example, under the "un\_username\_group" Parameter record, users can create a Parameter Value record to store usernames and under the "un\_password\_group" Parameter record, users can create a Parameter Value record to store passwords. Only one Parameter Value record can be created per user for each Parameter record. If multiple users need to trigger the same AI agent, each user must create a Parameter Value record for their own credentials.

You can create Parameter records only for username and password. For any other SSH parameters, provide the values either in the agent instructions or in your instructions in the Now Assist panel.

## AI Agent instructions during execution

The following example shows how an AI agent instruction can reference stored parameter names:

`Connect to SSH server and retrieve my session info. Here are my details:```

-   `IP address: 172.27.50.123`
-   `Port: 22`
-   `Retrieve the user name stored in "un_username_group" and the password stored in "un_password_group" parameter records.`

**Note:** When triggering an AI agent, explicitly specify in your instructions whether the credentials are provided directly or stored in Parameter records. If Parameter records are used, clarify that the record names are for reference only and that the agent must retrieve the username and password from those records.

Ensure that you use the exact names of the Parameter records. Parameter record names are case sensitive. For example, "UserName" and "username" are treated as different values.

**Parent Topic:**[Configuring AI Desktop Actions for defined path desktop actions](ad-defined-path-da.md)

## Create Parameter records for SSH credentials

Create a Parameter record with a name that you can reference in your instructions so the AI agent can securely sign in to the SSH server and execute commands.

### Before you begin

Perform this task in the ServiceNow instance.

Ensure that you have an active SSH server.

Role required: sn\_aia.admin

### Procedure

1.  Navigate to **All** &gt; **AI Desktop Actions** &gt; **Desktop Action Parameters**.

2.  Select **New** to create a Parameter record.

3.  Enter the name and description.

    For example, un\_username\_group or un\_password\_group

4.  Select **Submit**.


## Store username and password values in the Parameter Value records

Create Parameter Value records for storing the actual username and password values so that AI agents can securely connect to the SSH server.

### Before you begin

Perform this task in the ServiceNow instance.

Role required: sn\_aia.admin or now\_assist\_panel\_user

### Procedure

1.  Navigate to **All** &gt; **AI Desktop Actions** &gt; **Desktop Action Parameters**.

2.  Select a Parameter record from the list.

3.  Create a parameter value record.

    1.  In the Desktop action parameter values related list, select **New**.

    2.  Fill in the following fields.

<table id="table_wl1_zbw_h3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for this Parameter Value record that stores user name or password.

</td></tr><tr><td>

User

</td><td>

Read-only. Name of the user who creates this record.**Note:** Only user with the sn\_aia.admin role can edit this field and assign this record to any other user.

</td></tr><tr><td>

Is sensitive

</td><td>

Option to encrypt the value

</td></tr><tr><td>

Value

</td><td>

Value such as user name or password for connecting to the SSH server.

</td></tr></tbody>
</table>    3.  Select **Submit**.


