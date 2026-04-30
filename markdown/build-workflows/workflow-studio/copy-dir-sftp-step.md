---
title: Copy Directory
description: Copies a directory from the source SFTP server to the target SFTP server.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [SFTP step, Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Copy Directory

Copies a directory from the source SFTP server to the target SFTP server.

**Note:** If you wish to use the Managed File Transfer feature while copying a directory, activate the ServiceNow IntegrationHub Action Step - MFT \(com.glide.hub.action\_step.mft\) plugin.

## Fields

<table id="table_k5k_qnj_kjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connections

</td></tr><tr><td>

Source Connection

</td><td>

Type of connection to use to connect to the source SFTP server.-   **Define Connection Inline**: Define connection information within the action step.
-   **Use Connection Alias**: Define connection information using the Connection Alias table. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action.

 To learn more about connections and credentials, see [Introduction to credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Source Connection Alias

</td><td>

Connection &amp; Credential alias record that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action. To learn more about connections and credentials, see [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US). The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. This field is available when **Use Connection Alias** is selected from the Source Connection list.

</td></tr><tr><td>

Target Connection

</td><td>

Type of connection to use to connect to the target SFTP server.-   **Define Connection Inline**: Define connection information within the action step.
-   **Use Connection Alias**: Define connection information using the Connection Alias table. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action.

 To learn more about connections and credentials, see [Introduction to credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Target Connection Alias

</td><td>

Connection &amp; Credential alias record that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action. To learn more about connections and credentials, see [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Source Credential alias

</td><td>

Credential alias that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials when using an action in multiple environments. Likewise, if the credential information changes, you don't need to update your custom action. To learn more about connections and credentials, see [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US). The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. This field is available when **Define Connection Inline** is selected from the Source Connection list.**Note:** The SFTP step requires a credential record that supports either SSH private key credentials or SSH credentials. This step does not support Windows credentials where the **Use MID Server service account** option is selected.

</td></tr><tr><td>

Host

</td><td>

Name or IP address of the SFTP server that contains the files you wish to copy.

</td></tr><tr><td>

Port

</td><td>

Port number to communicate with the server.

</td></tr><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


 This field is available when **Define Connection Inline** is selected from the Source Connection list.

</td></tr><tr><td>

MID Application

</td><td>

Option to use a MID Server to run the SFTP step. This field is available when **Define Connection Inline** is selected from the Source Connection list and **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

Capabilities

</td><td>

Capability of the MID Server. Select **SSH**. This field is available when **Define Connection Inline** is selected from the Source Connection list and **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Server

</td><td>

Data pill of the required MID Server. This field is available when **Define Connection Inline** is selected from the Source Connection list and **Specific MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Cluster

</td><td>

Data pill for the MID Cluster you want to use. This field is available when **Define Connection Inline** is selected from the Source Connection list, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr><tr><td colspan="2">

Command Details

</td></tr><tr><td>

Source Path

</td><td>

Full path to the file in the source server you wish to copy. For example, `/root/doc/tempwsdl.rtf`.

</td></tr><tr><td>

Target Path

</td><td>

Full path to the file in the target server you wish to copy the contents. For example, `/root/doc/attribute.rtf`. In this case, the contents of the tempwsdl.rtf are copied to the file, attribute.rtf.

</td></tr><tr><td>

Include Files

</td><td>

List of target files to remove. This is a semicolon separated list that accepts wild cards, such as `*.txt`.**Note:**

-   If no value is provided, subfolders in the specified directory are deleted.
-   If a value is provided, subfolders are not deleted even if they are empty.

</td></tr><tr><td>

Exclude Files

</td><td>

List of target files that should not be removed. This is a semicolon separated list that accepts wild cards, such as `*.txt`.**Note:**

-   If no value is provided, subfolders in the specified directory are deleted.
-   If a value is provided, subfolders are not deleted even if they are empty.

</td></tr><tr><td>

Include Subfolders

</td><td>

Option to copy subfolders in the source directory.

</td></tr><tr><td colspan="2">

Managed File Transfer

</td></tr><tr><td>

Target File Name

</td><td>

Name of the target file.

</td></tr><tr><td>

Target Directory Name

</td><td>

Name of the target directory.

</td></tr><tr><td>

Datetime Format $\{DateTime\}

</td><td>

Format in which the date and time should be appended to the file name upon copying to the target server.

</td></tr><tr><td>

Preserve File Attributes

</td><td>

Option to preserve the file attributes upon copying files to the target directory.

</td></tr><tr><td>

Apply Move Conditions

</td><td>

Option to specify conditions while moving files.

</td></tr><tr><td>

Minimum File Size \(Bytes\)

</td><td>

Minimum size requirements to move files.**Note:** This field is available when **Apply Move Conditions** is enabled.

</td></tr><tr><td>

Maximum File Size \(Bytes\)

</td><td>

Maximum size requirements to move files.**Note:** This field is available when **Apply Move Conditions** is enabled.

</td></tr><tr><td>

File is Newer than

</td><td>

Files created after this date are moved.**Note:** This field is available when **Apply Move Conditions** is enabled.

</td></tr><tr><td>

File is Older than

</td><td>

Files created before this date are moved.**Note:** This field is available when **Apply Move Conditions** is enabled.

</td></tr><tr><td>

Move Order

</td><td>

Order in which the files should be moved.**Note:** This field is available when **Apply Move Conditions** is enabled.

</td></tr><tr><td>

Sort Order

</td><td>

Order in which the files should be sorted.**Note:** This field is available when **Apply Move Conditions** is enabled.

</td></tr><tr><td>

Duplicate File Action

</td><td>

Action to be performed when a duplicate file exists in the target directory.**Note:** This field is available when **Apply Move Conditions** is enabled.

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

</td></tr><tr><td colspan="2">

Managed File Transfer Error Cleanup

</td></tr><tr><td>

Upon Failure, Remove Files on Target

</td><td>

Option to remove files from the target SFTP server when the copy command fails.

</td></tr><tr><td>

Upon Success, Remove Files from Source

</td><td>

Option to remove files from the source SFTP server when the copy command is executed successfully.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[SFTP step](sftp-step.md)

