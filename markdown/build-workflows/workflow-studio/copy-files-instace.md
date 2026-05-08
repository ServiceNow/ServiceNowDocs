---
title: Copy Files To This Instance
description: Attaches the specified files in the SFTP server to the specified record in ServiceNow instance.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [SFTP step, Steps, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Copy Files To This Instance

Attaches the specified files in the SFTP server to the specified record in ServiceNow instance.

<table id="table_ypp_krp_nnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connections

</td></tr><tr><td>

Connection

</td><td>

Type of connection to use to connect to the source SFTP server.-   **Define Connection Inline**: Define connection information within the action step.
-   **Use Connection Alias**: Define connection information using the Connection Alias table. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action.

 To learn more about connections and credentials, see Introduction to credentials, connections, and aliases.

</td></tr><tr><td>

Connection Alias

</td><td>

Connection &amp; Credential alias record that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action. To learn more about connections and credentials, see credentials, connections, and aliases. The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. This field is available when **Use Connection Alias** is selected from the Connection list.

</td></tr><tr><td>

Credential Alias

</td><td>

Credential alias that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials when using an action in multiple environments. Likewise, if the credential information changes, you don't need to update your custom action. To learn more about connections and credentials, see credentials, connections, and aliases. The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. This field is available when **Define Connection Inline** is selected from the Connection list.**Note:** The SFTP step requires a credential record that supports either SSH private key credentials or SSH credentials. This step does not support Windows credentials where the **Use MID Server service account** option is selected.

</td></tr><tr><td>

Host

</td><td>

Name or IP address of the SFTP server to which the files you should be copied. This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Port

</td><td>

Port number to communicate with the server. This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see Configure a MID Server cluster.


 This field is available when **Define Connection Inline** is selected from the Source Connection list.

</td></tr><tr><td>

MID Server

</td><td>

Specific MID Server to run the SFTP step. This field is available when **Specific MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Cluster

</td><td>

Data pill for the MID Cluster you want to use. This field is available when **Define Connection Inline** is selected from the Source Connection list, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr><tr><td>

MID Application

</td><td>

Option to use a MID Server to run the SFTP step. This field is available when **Define Connection Inline** is selected from the Connection list and **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

Capabilities

</td><td>

Capability of the MID Server. Select **SSH**. This field is available when **Define Connection Inline** is selected from the Connection list and **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Server

</td><td>

Data pill of the required MID Server. This field is available when **Define Connection Inline** is selected from the Connection list and **Specific MID Server** is selected from the MID Selection list.

</td></tr><tr><td colspan="2">

SFTP Files To Copy

</td></tr><tr><td>

Source Path

</td><td>

Path of the directory that contains the files you want to copy. For example, `/root/doc/`.

</td></tr><tr><td>

Include Files

</td><td>

List of target files to copy. This is a semicolon separated list that accepts wild cards, such as `*.txt`.**Note:** If no value is provided, subfolders in the specified directory are copied.

</td></tr><tr><td>

Exclude Files

</td><td>

List of target files that should not be copied. This is a semicolon separated list that accepts wild cards, such as `*.txt`.

</td></tr><tr><td>

Maximum File Size \(KB\)

</td><td>

Maximum size of the file that can be copied.

</td></tr><tr><td>

Maximum Number of Files

</td><td>

Maximum number of files that can be copied in a request.

</td></tr><tr><td colspan="2">

Attach Files To This Target Record

</td></tr><tr><td>

Target Record

</td><td>

Record in ServiceNow instance to which you want to attach the files.

</td></tr><tr><td>

Table

</td><td>

ServiceNow table in which the target record is saved.

</td></tr><tr><td colspan="2">

Retry Policy

</td></tr><tr><td>

Enable Retry Policy

</td><td>

Option to enable the retry policy. For more information, see [Retry policy](../concept/retry-policy.md#).

</td></tr><tr><td>

Override Default Policy for Alias

</td><td>

Option to override the default retry policy. This option is not applicable when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Retry Policy

</td><td>

Default retry policy associated with **Connection Alias**. If **Override Default Policy for Alias** is selected, you can override the default retry policy and select another existing retry policy based on your requirement.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[SFTP step](sftp-step.md)

