---
title: SFTP File Transfer workflow
description: The SFTP File Transfer activity pack includes a scoped workflow that uses multiple activities to manage files on SFTP servers.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [SFTP File Transfer activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# SFTP File Transfer workflow

The SFTP File Transfer activity pack includes a scoped workflow that uses multiple activities to manage files on SFTP servers.

The maximum activity count for the SFTP File Transfer workflow is set to 10,000. This allows the workflow to move up to 1000 files from one server to another.

## Accessing the workflow

-   Navigate to **Workflow** &gt; **Workflow Editor** and select the **Workflows** tab.
-   Click on the SFTP File Transfer workflow to open it.
-   Click the information icon in the workflow header to display the properties dialog box.

## Input variables

<table id="table_e23_hby_mt"><thead><tr><th>

Variable

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Source host

</td><td>

Name or IP address of the server containing the files you want to move.

</td><td>

 

</td></tr><tr><td>

Source port

</td><td>

Port number to use to communicate with the source server.

</td><td>

22

</td></tr><tr><td>

Source directory

</td><td>

Full path to the directory where the source files are located.

</td><td>

 

</td></tr><tr><td>

Source files

</td><td>

Names of specific source files to move. Separate the file names in this list with semi-colons. This field supports the use of wild cards. For information about how the values in this field are affected by options in other fields, see the section below the table.

</td><td>

 

</td></tr><tr><td>

Excluded files

</td><td>

Names of specific source files to exclude from the move. The system moves all other files found in the source directory or subfolders. Separate the file names in this list with semi-colons. This field supports the use of wild cards. For information about how the values in this field are affected by options in other fields, see the section below the table.

</td><td>

 

</td></tr><tr><td>

Target host

</td><td>

Name or IP address of the server to which the files are being moved.

</td><td>

 

</td></tr><tr><td>

Target port

</td><td>

Port number to use to communicate with the target host.

</td><td>

22

</td></tr><tr><td>

Datetime format

</td><td>

Timestamp format to apply when the `$[DateTime]` variable is used in the **Target directory** or **Target files** field. The system uses the current time from the instance to create timestamp values.

</td><td>

yyyy-MM-dd

</td></tr><tr><td>

Target directory

</td><td>

Path to the directory in the target host where the files are being moved. You can specify a target directory whose name includes the timestamp by adding the `$[DateTime]` variable to the directory name. For example, you might enter this path to a target directory: `/user/jacinto.gawron/documents/projects_$[DateTime]`. This produces the `projects_20150505` directory. When the timestamp variable is used, the system uses the format specified in the **Datetime format** field.

</td><td>

 

</td></tr><tr><td>

Target file

</td><td>

Format to use for target file names when a timestamp is added. You can configure the system to add the timestamp as a prefix to the file name or insert the timestamp into the name, using these variables:-   `$[DateTime]`: Current timestamp, using the format defined in the **Datetime format** field.
-   `$[SourceFile]`: Complete file name.
-   `$[SourceFile:Base]`: Base file name without the extension.
-   `$[SourceFile:Ext]`: File extension only.

 A target file name with the timestamp added as a prefix is expressed as: `$[DateTime]_$[SourceFile]`. This produces a file name that looks like this: `20150505_file1.txt`

 A target file name with the timestamp inserted into the name is expressed as: `$[SourceFile:Base]_$[DateTime]$[SourceFile:Ext]`. This produces a file name that looks like this: `file1_20150505.txt`

</td><td>

 

</td></tr><tr><td>

Apply move conditions

</td><td>

Check box to apply conditions to the file transfer. If this check box is selected, additional fields appear for setting conditions.

</td><td>

false

</td></tr><tr><td>

Minimum file size, in bytes

</td><td>

Condition that defines a target file's minimum size requirement. This setting can help determine if the file is valid. This field appears when the **Apply move conditions** check box is selected.

</td><td>

0

</td></tr><tr><td>

Maximum file size, in bytes

</td><td>

Condition that defines a target file's maximum size requirement. This field appears when the **Apply move conditions** check box is selected.

</td><td>

-1

</td></tr><tr><td>

File is not older than

</td><td>

Condition that sets the earliest acceptable date for this file's age range. The range starts at 00:00 \(midnight\) on the date specified. This field appears when the **Apply move conditions** check box is selected.

</td><td>

 

</td></tr><tr><td>

File is not newer than

</td><td>

Condition that sets the latest acceptable date for this file's age range. The range ends at 23:59 on the date specified. This field appears when the **Apply move conditions** check box is selected.

</td><td>

 

</td></tr><tr><td>

Include subfolders

</td><td>

Check box to move the files from subfolders in the source directory. For information about how your selection affects other fields in the form, see the section below the table.

</td><td>

 

</td></tr><tr><td>

Move order

</td><td>

Order in which the files are moved from the source to the target. The possible options are: -   **None** \(same order as files in the source directory\)
-   **By timestamp**
-   **By file name**
-   **By file size**

</td><td>

 

</td></tr><tr><td>

Sort order

</td><td>

Order in which the files are sorted in the target directory, using the option selected in the **Move order** field. Sorting options are **Ascending** and **Descending**.

</td><td>

desc

</td></tr><tr><td>

Maximum number of retries

</td><td>

Number of attempts the activity can make to connect to the target host or to move a file before timing out. When the retry limit to move a file or to connect to the host is exceeded, the system logs a failure. If the maximum number of failures is not exceeded, the system attempts to connect again or to move the next file named.

</td><td>

2

</td></tr><tr><td>

Time between retries, in seconds

</td><td>

Time, in seconds, between repeat attempts to connect to the target or to begin moving a file.

</td><td>

10

</td></tr><tr><td>

Maximum number of failures

</td><td>

Acceptable number of times the system can fail to connect to the target host or to move a file before it quits trying. A failure occurs when the number of configured retries is exceeded. Using the default settings, failure occurs when the system cannot connect to the target or move a file after two retries.

</td><td>

0

</td></tr><tr><td>

Duplicate file action

</td><td>

Action to take if a file being moved already exists in the target directory. The choices are:-   **Overwrite if file exists** \(default\)
-   **Rename with index**
-   **Do not move**

</td><td>

overwrite

</td></tr><tr><td>

Preserve file attributes

</td><td>

Check box to use the time stamp and mode information from the source files for the copied files. If this check box is cleared, the copied files have a current time stamp and mode.**Note:** This timestamp is a file attribute and is not appended to the file name.

</td><td>

false

</td></tr><tr><td>

Upon success, remove files from source

</td><td>

Check box to delete original files from the source directory when they are copied to the new location. Clear this check box to keep the source files in their current location in the source host.

</td><td>

false

</td></tr><tr><td>

Upon failure, keep moved files on target

</td><td>

Check box to keep any files on the target that were moved successfully, even if the entire file transfer operation ended in failure. If this check box is cleared, the system removes all successfully transfered files from the target when general failure occurs.

</td><td>

true

</td></tr><tr><td>

Credential tag for source

</td><td>

Specific Credential aliases for Orchestration activities this activity must use to run SSH commands on the source host.

</td><td>

 

</td></tr><tr><td>

Credential tag for target

</td><td>

Specific credential tag this activity must use to run SSH commands on the target host.

</td><td>

 

</td></tr></tbody>
</table>## File selection logic

When selecting the files to move from the source host, the system uses this logic:

-   If the **Source files** and **Excluded files** fields are empty, the system moves all the files in the source directory.
-   When the **Include subfolders** check box is selected, the following dependencies exist:
    -   If no files are specified in the **Source files** and **Exclude files** fields, the system moves all files in the source directory and all files in all subfolders of the source directory.
    -   If the **Source files** field contains file names, the system moves those files from their location on either the source directory or any of its subfolders.
    -   If the **Exclude files** field contains file names, the system moves all the files from the source directory and its subfolders except those excluded files.
-   When the **Include subfolders** check box is cleared, the system looks only in the source directory for files to move or exclude.

**Parent Topic:**[SFTP File Transfer activity pack](../concept/c_OrchestrationSFTPActivityPack.md)

