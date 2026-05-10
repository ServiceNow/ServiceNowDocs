---
title: Create an SFTP activity
description: Create an activity that executes basic SFTP commands on a remote server.You use execution parameters to create the input process script in the Preprocessing form.Use these parameters to create a post-processing script, payload parsing, and tagging.Use the input variables you created to configure the command that Orchestration executes on the SFTP target.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, Workflow Data Fabric]
---

# Create an SFTP activity

Create an activity that executes basic SFTP commands on a remote server.

## Before you begin

Roles required: activity\_creator or workflow\_admin

## About this task

You can create a custom activity that manages files and directories on a target host or copies a file from one SFTP server to another. The file content is streamed through a MID Server, which avoids having to store the data on the hard drive of the MID Server host machine.

**Note:** This activity requires the credentials of a user who can execute SFTP commands on the source host. The [Copy File](../../orchestration-activities/reference/r_CopyFileActivity.md) activity, provided in the activity pack, requires separate credentials to access the target host.

## Procedure

1.  Create a [custom activity](create-custom-activities.md).

    This action creates a custom activity using a template.

2.  After setting up [general properties](../reference/General-Flds-Templates.md) and [creating input variables](CreateInputVariables.md#), configure the SFTP Execution Command.

<table id="choicetable_zmw_zbr_vz"><tbody><tr><td id="d579262e120">

**Command**

</td><td>

Type of activity to create. The choices are:-   Copy file
-   Create directory
-   Get file list
-   Remove file or directory
-   Rename file or directory
-   Set file attributes
 **Note:** The fields that display on the form depend on the command you select.

</td></tr><tr><td id="d579262e155">

**Source host**

</td><td>

Name or IP address of the server containing the files targeted by the activity.

</td></tr><tr><td id="d579262e164">

**Source port**

</td><td>

Port number to use to communicate with the source server. The default port number is **22**.

</td></tr><tr><td id="d579262e176">

**Source file path**

</td><td>

Full path to a file \(`/temp/test_data_file.txt`\) or directory \(/`temp/test_dir`\) on a source host depending on the selected command. Field available on following commands: -   Copy file
-   Remove file or directory
-   Set file attributes


</td></tr><tr><td id="d579262e203">

**Source directory**

</td><td>

Path to the directory where the source files are located. Field available on following commands: -   Create directory
-   Get file list


</td></tr><tr><td id="d579262e222">

**Source files**

</td><td>

Names of specific source files to include in the file transfer. Separate the file names with semi-colons. This field supports a semi-colon separated list of wild-card patterns. For example: `*.txt; a?cd.pdf.` If this field is blank, all files are included. Field available on following command: Get file list**Note:** For information about how the values in this field affect options in other fields, see the logic explanation which follows.

</td></tr><tr><td id="d579262e237">

**Is a directory**

</td><td>

If checked, specifies the file path is a directory. Field available on following command: Remove file or directory

</td></tr><tr><td id="d579262e246">

**Credential tag for source**

</td><td>

Specific credential tag this activity must use to run SFTP commands on the source host.

</td></tr><tr><td id="d579262e255">

**Credential tag for target**

</td><td>

Specific credential tag this activity must use to run SFTP commands on the target host. Field available on following command: Copy file

</td></tr><tr><td id="d579262e264">

**Excluded files**

</td><td>

Names of specific source files to exclude from the file transfer. The activity acts on all other files found in the source directory or subfolders. Separate the file names with commas. This field supports comma-separated list of wild-card patterns. For example: `*.txt, a?cd.pdf.`. Field available on following command: Get file list **Note:** For information about how the values in this field affect options in other fields, see the logic explanation which follows.

</td></tr><tr><td id="d579262e279">

**Include subfolders**

</td><td>

If checked, includes the files from subfolders in the source directory. Field available on following command: Get file list **Note:** For information about how your selection affects other fields in the form, see the logic explanation which follows.

</td></tr><tr><td id="d579262e292">

**Target host**

</td><td>

Name or IP address of the server to which the files are being transferred. Field available on following command: Copy file

</td></tr><tr><td id="d579262e301">

**Target port**

</td><td>

Port number to use to communicate with the target host. The default port number is **22**. Field available on following command: Copy file

</td></tr><tr><td id="d579262e313">

**Target file path**

</td><td>

Full path to a file on a target host. Field available on following commands: -   Copy file
-   Rename file or directory


</td></tr><tr><td id="d579262e331">

**Suffix for temporary file**

</td><td>

If a file exists on a target host, this command enables a temporary suffix to use for a file name. If this field contains a value, the activity first copies the source file to a temporary file on the target host using **targetFilePath + tempFileSuffix** as the name. Upon completion, the activity renames the file to the actual target file name. If this field is blank, the activity copies the source file directly to the target file and overwrites it, if it exists. Field available on following command: Copy file

</td></tr><tr><td id="d579262e343">

**UID**

</td><td>

User ID attribute to apply to a file or directory. The UID and GID values must be set together as a pair or they are ignored. The UID and GID numbers are internal values returned by the Get File List activity. Typically, you first use the Get File List activity to return a list of files and their attributes. Then you can move a file from a source host to a target host and set the source file attributes on the target file. This flow is demonstrated in the [SFTP File Transfer workflow](../../orchestration-activities/reference/r_SFTPWorkflow.md). Field available on following command: Set file attributes

</td></tr><tr><td id="d579262e359">

**GID**

</td><td>

Group ID attribute to apply to a file or directory. The UID and GID values must be set together as a pair or they are ignored. The UID and GID numbers are internal values returned by the Get File List activity. Typically, you first use the Get File List activity to return a list of files and their attributes. Then you can move a file from a source host to a target host and set the source file attributes on the target file. This flow is demonstrated in the [SFTP File Transfer workflow](../../orchestration-activities/reference/r_SFTPWorkflow.md). Field available on following command: Set file attributes

</td></tr><tr><td id="d579262e376">

**Permissions**

</td><td>

File or directory permissions to set for the user and group specified. This value must be expressed as an integer, such as **16877**, which defines these permissions: **rwxr-xr-x**. The permissions numbers are internal values returned by the Get File List activity. Typically, you first use the Get File List activity to return a list of files and their attributes. Then you can move a file from a source host to a target host and set the source file attributes on the target file. This flow is demonstrated in the [SFTP File Transfer workflow](../../orchestration-activities/reference/r_SFTPWorkflow.md). Field available on following command: Set file attributes

</td></tr><tr><td id="d579262e398">

**Access timestamp**

</td><td>

Override the timestamp when the file or directory was last accessed. The access and modification timestamps must be set together as a pair. Field available on following command: Set file attributes

</td></tr><tr><td id="d579262e407">

**Modification timestamp**

</td><td>

Override the timestamp when the file or directory was last modified. The access and modification timestamps must be set together as a pair. Field available on following command: Set file attributes

</td></tr><tr><td id="d579262e416">

**Size in bytes**

</td><td>

Size of a file, expressed in bytes. Field available on following command: Set file attributes

</td></tr><tr><td id="d579262e425">

**Required MID Server capabilities**

</td><td>

MID Server with the appropriate [MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ConfigureCapabilities.md) for connecting to the source and target servers.

</td></tr></tbody>
</table>    The system uses this logic to determine which files to move from the source host:

    -   If the Source files field is empty, the system selects all the files in the source directory. Otherwise, it only selects those files whose names match one of the file name patterns given in the field.
    -   If the Excluded files field is empty, the system excludes nothing. Otherwise, it excludes those files whose names match one of the file name patterns given in the field.
    -   The exclude rule has a higher preference than the include rule. If a file name matches one of the file name patterns in the Excluded files field, it does not get into the selection regardless of the include rule.
    -   When the Include subfolders check box is cleared, the system looks only in the source directory for files to include or exclude. Otherwise, it looks in the source directory and any of its subfolders for files to include or exclude.
    **Note:** You can map parameter values in a test payload to variables in the **Outputs** tab automatically. See [automap output variables](automap-output-variable-inputs.md).


## What to do next

-   Use [auto-mapping](automap-output-variable-inputs.md) to generate outputs and parsing rules \(recommended for JDBC\)
-   If you do not use auto-mapping, you can manually [create output variables](t_CreateAnOutputVariable.md#) and [create parsing rules](t_CreateAParsingRule.md#)

**Parent Topic:**[Orchestration custom activity templates](../concept/c_ActivityDesignerComponents.md)

## SFTP template execution parameters

You use execution parameters to create the input process script in the **Preprocessing** form.

For descriptions of the command fields, see [Configure the SFTP execution command](t_CreateAnSFTPActivity.md#).

**Note:** You must use the `executionParam.` prefix with all variables in this table.

<table id="table_wl1_yxc_dr"><thead><tr><th>

Name

</th><th>

Variable

</th><th>

Type

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Command

</td><td>

command

</td><td>

String

</td><td>

Identifies the function of this activity. The possible commands are: -   Copy file
-   Create directory
-   Get file list
-   Remove file or directory
-   Rename file or directory
-   Set file attributes

</td></tr><tr><td>

Source

</td><td>

source

</td><td>

String

</td><td>

Identifies the source host.

</td></tr><tr><td>

Source port

</td><td>

source\_port

</td><td>

Integer

</td><td>

Identifies the port used to communicate with the source host.

</td></tr><tr><td>

Source directory

</td><td>

source\_directory

</td><td>

String

</td><td>

Path to the source directory of the files to be moved.

</td></tr><tr><td>

Source files

</td><td>

source\_files

</td><td>

String

</td><td>

Names of the files on the source to be moved.

</td></tr><tr><td>

Excluded files

</td><td>

excluded\_files

</td><td>

String

</td><td>

Lists the files excluded from the operation.

</td></tr><tr><td>

Source file path

</td><td>

source\_file\_path

</td><td>

String

</td><td>

Path to the source files to be moved.

</td></tr><tr><td>

Target host

</td><td>

target\_host

</td><td>

String

</td><td>

Identifies the target host.

</td></tr><tr><td>

Target port

</td><td>

target\_port

</td><td>

Integer

</td><td>

Identifies the port used to communicate with the target host.

</td></tr><tr><td>

Target directory

</td><td>

target\_directory

</td><td>

String

</td><td>

Full path to the target directory on the target host.

</td></tr><tr><td>

Target file path

</td><td>

target\_file\_path

</td><td>

String

</td><td>

Full path to a file or directory on the source host or on the target host. For example, this value is used in the [Rename File or Directory](../../orchestration-activities/reference/r_RenameFileOrDirectoryActivity.md) activity in the activity pack.

</td></tr><tr><td>

Temp file postfix

</td><td>

temp\_file\_postfix

</td><td>

String

</td><td>

Temporary file name extension used by the Copy File activity when moving a file. If this field contains an extension, the source file is copied to a temporary file using **target file name + temp\_file\_postfix**, before being renamed to the actual target file. If this field is blank, the source file is copied directly to the target file.

</td></tr><tr><td>

Is directory

</td><td>

is\_directory

</td><td>

Boolean

</td><td>

Indicates whether the given file path is a directory.

</td></tr><tr><td>

Include subfolders

</td><td>

include\_subfolders

</td><td>

Boolean

</td><td>

Indicates whether the system looks into subfolders of the source directory for files to include and exclude.

</td></tr><tr><td>

File attribute uid

</td><td>

file\_attribute\_uid

</td><td>

Integer

</td><td>

User ID associated with a file or directory.

</td></tr><tr><td>

File attribute gid

</td><td>

file\_attribute\_gid

</td><td>

Integer

</td><td>

Group ID associated with a file or directory.

</td></tr><tr><td>

File attribute permissions

</td><td>

file\_attribute\_permissions

</td><td>

Integer

</td><td>

File or directory permissions for the user and group specified.

</td></tr><tr><td>

File attribute atime

</td><td>

file\_attribute\_atime

</td><td>

Integer

</td><td>

Access time stamp from the file attributes.

</td></tr><tr><td>

File attribute mtime

</td><td>

file\_attribute\_mtime

</td><td>

Integer

</td><td>

Modification time stamp from the file attributes.

</td></tr><tr><td>

File attribute size

</td><td>

file\_attribute\_size

</td><td>

Integer

</td><td>

Size of the file, in bytes.

</td></tr><tr><td>

Source credential tag

</td><td>

source\_credential\_tag

</td><td>

String

</td><td>

[Credential aliases for Orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/c_AssignCredsOrchActivities.md) used to run the command on the source host.

</td></tr><tr><td>

Target credential tag

</td><td>

target\_credential\_tag

</td><td>

String

</td><td>

Credential tag used to run the command on the target host.

</td></tr><tr><td>

MidCapabilities

</td><td>

midCapabilities

</td><td>

String \(comma separated\)

</td><td>

List of required MID Server capabilities.

</td></tr></tbody>
</table>## SFTP post-processing parameters and payload parsing

Use these parameters to create a post-processing script, payload parsing, and tagging.

<table id="table_xlq_3n5_cr"><thead><tr><th>

Name

</th><th>

Variable

</th><th>

Type

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Output

</td><td>

output

</td><td>

String

</td><td>

Contains output data returned by the query.

</td></tr><tr><td>

EccSysId

</td><td>

eccSysId

</td><td>

String

</td><td>

Contains the Reference ID associated with the ECC Queue input message.

</td></tr><tr><td>

ErrorMessages

</td><td>

errorMessages

</td><td>

String

</td><td>

Contains the error messages returned from the query. If no error messages are returned, this value is null.

</td></tr><tr><td>

Tags

</td><td>

tags

</td><td>

Hashmap of tag values returned from the SSH command

</td><td>

Contains the tags used to extract output using the SSH commands. The tag output is delimited by double percentage signs, as in `%%tagname%% … %%`. Set up the command using the following format:```
%%tagname1%%
output1 line 1
output1 line 2
…
%%

%%tagname2%%
output2 line 1
output2 line 2
…
%%
```

The tags returned are JavaScript hashmap objects in which each key is prefixed with `tag` appended with the tagname.```
{"__text__": "", 
"tagtagname1":"output1 line1\noutput1 line2\n", 
"tagtagname2":"output2 line1\noutput2 line2\n"}
```

</td></tr></tbody>
</table>## Configure the SFTP execution command

Use the input variables you created to configure the command that Orchestration executes on the SFTP target.

### Before you begin

Create the input variables you need in the **Inputs** form before you can advance to the **Execution Command** stage.

Role required: activity\_creator, admin

**Note:** You can test the JDBC connection between the MID Server and the target without having to run the activity in a workflow context. For details, see [test template outputs](CreateInputVariables.md#).

### Procedure

1.  Drag variables from the list of inputs and drop them into command fields.

    The system formats the variable in the proper syntax for the command.

    ![In this example, the Create directory command displays in the Command field.](../image/SFTPExecutionCommand.png "SFTP execution command")

2.  Complete the fields shown in the table.

<table id="table_zmv_v25_cr"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Command

</td><td>

Type of activity to create. The choices are:-   Copy file
-   Create directory
-   Get file list
-   Remove file or directory
-   Rename file or directory
-   Set file attributes
 **Note:** The fields displayed on the form depend on the command selected.

</td><td>

All

</td></tr><tr><td>

Source host

</td><td>

Name or IP address of the server containing the files targeted by the activity.

</td><td>

All

</td></tr><tr><td>

Source port

</td><td>

Port number to use to communicate with the source server. The default port number is **22**.

</td><td>

All

</td></tr><tr><td>

Source file path

</td><td>

Full path to a file on a source host.

</td><td>

-   Copy file
-   Remove file or directory
-   Set file attributes


</td></tr><tr><td>

Source directory

</td><td>

Path to the directory where the source files are located.

</td><td>

-   Create directory
-   Get file list


</td></tr><tr><td>

Source files

</td><td>

Names of specific source files to include in the management action. Separate the file names in this list with semi-colons. This field supports the use of wild cards. If this field is blank, all files are included. For information about how the values in this field are affected by options in other fields, see the section below the table.

</td><td>

Get file list

</td></tr><tr><td>

Is a directory

</td><td>

Check box that determines if the specified file path is a directory.

</td><td>

Remove file or directory

</td></tr><tr><td>

Credential tag for source

</td><td>

Specific [Credential aliases for Orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/c_AssignCredsOrchActivities.md) this activity must use to run SFTP commands on the source host.

</td><td>

All

</td></tr><tr><td>

Credential tag for target

</td><td>

Specific credential tag this activity must use to run SFTP commands on the target host.

</td><td>

Copy file

</td></tr><tr><td>

Excluded files

</td><td>

Names of specific source files to exclude from the management action. The activity acts on all other files found in the source directory or subfolders. Separate the file names in this list with semi-colons. This field supports the use of wild cards. For information about how the values in this field are affected by options in other fields, see the section below the table.

</td><td>

Get file list

</td></tr><tr><td>

Include subfolders

</td><td>

Check box to manage the files from subfolders in the source directory. For information about how your selection affects other fields in the form, see the section below the table.

</td><td>

Get file list

</td></tr><tr><td>

Target host

</td><td>

Name or IP address of the server to which the files are being transferred.

</td><td>

Copy file

</td></tr><tr><td>

Target port

</td><td>

Port number to use to communicate with the target host. The default port number is **22**.

</td><td>

Copy file

</td></tr><tr><td>

Target file path

</td><td>

Full path to a file on a target host.

</td><td>

-   Copy file
-   Rename file or directory


</td></tr><tr><td>

Suffix for temporary file

</td><td>

Temporary suffix to use for a file name if the file already exists on a target host. If this field contains a value, the activity deletes the duplicate target file if it exists, and then copies the source file to a temporary file using **targetFilePath + tempFileSuffix** as the name. Upon completion, the activity renames the file to the actual target file name. If this field is blank, the activity copies the source file directly to the target file and overwrites it, if it already exists.

</td><td>

Copy file

</td></tr><tr><td>

UID

</td><td>

User ID attribute to apply to a file or directory. The UID and GID values must be set together as a pair or they are ignored.

</td><td>

Set file attributes

</td></tr><tr><td>

GID

</td><td>

Group ID attribute to apply to a file or directory. The UID and GID values must be set together as a pair or they are ignored.

</td><td>

Set file attributes

</td></tr><tr><td>

Permissions

</td><td>

File or directory permissions to set for the user and group specified. This value must be expressed as an integer, such as **16877**, which defines these permissions: **rwxr-xr-x**. The permissions number is an internal value returned by the Get File List activity. Typically, you first use the Get File List activity to return a list of files and their attributes. Then you can move a file from a source host to a target host and set the source file attributes on the target file. This is demonstrated in the [SFTP File Transfer workflow](../../orchestration-activities/reference/r_SFTPWorkflow.md).

</td><td>

Set file attributes

</td></tr><tr><td>

Access timestamp

</td><td>

Override the timestamp when the file or directory was last accessed. The access and modification timestamps must be set together as a pair.

</td><td>

Set file attributes

</td></tr><tr><td>

Modification timestamp

</td><td>

Override the timestamp when the file or directory was last modified. The access and modification timestamps must be set together as a pair.

</td><td>

Set file attributes

</td></tr><tr><td>

Size in bytes

</td><td>

Size of a file, expressed in bytes.

</td><td>

Set file attributes

</td></tr><tr><td>

Required MID Server capabilities

</td><td>

MID Server with the appropriate [MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ConfigureCapabilities.md) for connecting to the source and target servers. By default, the system selects an SSH MID Server.

</td><td>

All

</td></tr></tbody>
</table>    The system uses this logic to determine which files to move from the source host:

    -   If the **Source files** field is empty, the system select all the files in the source directory. Otherwise, it only selects those files whose names match one of the file name patterns given in the field.
    -   If the **Excluded files** field is empty, the system excludes nothing. Otherwise, it excludes those files whose names match one of the file name patterns given in the field.
    -   The exclude rule has a higher preference than the include rule. A file whose name matches one of the file name patterns in the **Excluded files** field does not get into the selection, even though it would be selected by the include rule.
    -   When the **Include subfolders** check box is cleared, the system looks only in the source directory for files to include or exclude. Otherwise, it looks in the source directory and any of its subfolders for files to include or exclude.
3.  Click **Save**.

4.  Click **Continue** to advance to the **Outputs** stage.


