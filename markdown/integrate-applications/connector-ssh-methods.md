---
title: Secure Shell \(SSH\) connector methods
description: The Secure Shell \(SSH\) connector methods establish an SSH connection, execute commands over the established connection, and disconnect the session.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Secure Shell \(SSH\) connector, Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Secure Shell \(SSH\) connector methods

The Secure Shell \(SSH\) connector methods establish an SSH connection, execute commands over the established connection, and disconnect the session.

## Connect

Establishes an SSH connection. Provide the information required to connect to a remote machine.

Select the settings icon \(![Settings icon](../image/component-settings-icon.png)\) to choose the authentication type.

Supported authentication types are Password, KeyboardInteractive, and KeyFileAuthentication.![The authentication type configuration window displaying the Password, KeyboardInteractive, and KeyFileAuthentication as authentication types.](../image/ssh-connector-auth-types.png)

Password is the default authentication type.

<table id="table_wwq_k31_g5b"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

HostName

</td><td>

Host name of the remote server or IP address.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Username

</td><td>

User name of the SSH account.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Password

</td><td>

Secure string representation of the password. Password of the SSH account.

 You can use the SecureStringEncode component to encode the secure string password as mentioned in the following example. For more information, see [Use the SecureStringEncode component](../task/use-security-encryption-securestringencode.md).

![SecureStringEncode component is connected to the Connect method to pass the encoded password.](../image/ssh-connect-pwd-example.png "Connect method with Password parameter")

 After you perform this task, you can connect to the remote server.

</td><td>

Data In

</td><td>

SecureString

</td></tr><tr><td>

Port

</td><td>

Optional. The port number for the SSH connection. Default value is 22.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

CreateShell

</td><td>

Optional. If True, a shell stream is created on successful connection. Any command that is executing on this connection uses the shell.If False, any command that is executing on this connection does not the shell.

Default value is True.

</td><td>

Data In

</td><td>

Boolean

</td></tr><tr><td>

KeyboardInteractiveAuth

</td><td>

Password as a challenge. If True, the server prompts the client for password to verify the user's identity. Value provided in the password parameter is shared as a response from client.

This parameter appears only when **KeyboardInteractive** is selected from the Authentication Type.

</td><td>

Data In

</td><td>

Boolean

</td></tr><tr><td>

KeyFilepath

</td><td>

Path of the private key.This parameter appears only when **KeyFileAuthentication** is selected from the Authentication Type.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Passphrase

</td><td>

Optional. If private key is encrypted using Passphrase, same value is provided inside the Passphrase parameter to use the private key.This parameter appears only when **KeyFileAuthentication** is selected from the Authentication Type.

</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>## RunCommand

After establishing an SSH connection, execute commands over the established connection using the RunCommand method.

<table id="table_pkx_t12_b2c"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Command

</td><td>

Commands that must be executed on the remote SSH server, such as messages or scripts, can be valid shell commands or executable commands that the remote server can understand.For example, `echo hello`.

![Command entered as "echo hello" in the Command parameter RunCommand method](../image/ssh-run-command-example.png "RunCommand method - Command parameter")

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Timeout

</td><td>

Optional. The parameter that specifies the maximum time \(in seconds\) to wait for the command's output from the SSH server when using an interactive shell.Default value is 30.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

Return

</td><td>

The result of the executed command.For example, after executing the automation, in the Data Preview of Return parameter, "hello" is displayed.

![Data previews as hello, after the command is executed](../image/ssh-run-command-return-example.png "Return parameter of RunCommand method")

</td><td>

Data Out

</td><td>

String

</td></tr></tbody>
</table>## Disconnect

After executing commands, disconnect the established connection using the Disconnect method.

The following example shows the entire automation after adding the Disconnect method.

![SSH connector automation workflow example.](../image/ssh-disconnect-example.png "Disconnect method")

**Parent Topic:**[Secure Shell \(SSH\) connector](../concept/ssh-connector.md)

