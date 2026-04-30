---
title: Configure worknotes analysis
description: Configure worknotes analysis for a process table to view the worknotes analysis for a project based on that process table.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Worknotes analysis, Analyzing and getting process insights, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure worknotes analysis

Configure worknotes analysis for a process table to view the worknotes analysis for a project based on that process table.

## Before you begin

**Note:**

-   You can create one configuration for one process table.
-   Role required:
    -   The sn\_process\_optimization\_admin and sn\_process\_optimization\_power\_user roles can associate work note analysis definition with a project, but can’t create a definition.
    -   The sn\_process\_optimization\_analyst role can view a work note analysis definition, but can’t create, edit, associate, or delete a definition.

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Process Configurations**.

2.  Select a table from the list if you want to configure worknotes analysis for a table available in the list.

    If you don’t have the table listed, select **New**. For more information, see [Create process configuration record for the table](create-process-config.md).

    ![Configure Worknotes Analysis](../image/worknotes-configure.png)

3.  In the **Work Note Analysis** tab, fill in the fields.

<table id="table_ug1_3sp_5bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work Note Field

</td><td>

Select the work notes field that will be considered for analysis. The available options are:-   None: The analysis will not be available.
-   Additional comments: The analysis is available and the comments are visible to the requester.
-   Work notes: The analysis is available and the comments are visible only to the fulfiller.


</td></tr><tr><td>

Include Comment Field for Analysis

</td><td>

Select if you want to analyze the comments along with notes.

</td></tr><tr><td>

Work Note Time Range \(in seconds\)

</td><td>

Enter the time interval in seconds for retrieving work notes before and after the transition. For example, if you specify 60 seconds, then the analysis will capture work notes posted 60 seconds before and after the transition time. This helps to capture recent and relevant work notes for analysis.

</td></tr><tr><td>

System Generated Users

</td><td>

Enter user names that are associated with system-generated work notes to exclude work notes or comments created by those specific system users. System-generated work notes often lack explanations for transitions.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Worknotes analysis](../concept/worknotes-analysis.md)

