---
title: Configure investigative features
description: Configure investigative features to set advanced analytics features for a process.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [With Process Configuration Builder, Creating process configuration, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure investigative features

Configure investigative features to set advanced analytics features for a process.

## Before you begin

Role required: sn\_process\_optimization\_power\_user or sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the side of the page, select the Process configurations icon \(![Process configuration builder](../image/icon-process-config.png)\).

3.  Open a table from the **Configurations** tab.

    The **Process details** page is displayed. Select **Investigative features** from the left bar.

    If you’re proceeding from the **Process details** page, then you come to this page. For more information, see [Configure process details](process-details.md).

    The **Investigative features** page has four sections:

    -   Automated root cause analysis
    -   Cluster analysis
    -   Work notes analysis
    -   Automation Discovery
    ![Investigative features in process configuration](../image/invest-features-config.png)

4.  Add fields that you want for automated root cause analysis in the **Automated root cause analysis** field.

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    Based on your inputs in the **Process perspectives** section on the **Process details** page you’ll get recommendations for automated root cause analysis.

    When you set up the automated root cause analysis, you can initiate a root cause analysis in your project that is based on this table. For more information on running root case analysis, see [Run automated root cause analysis reports](run-view-arca.md).

    **Note:** The automated root cause analysis won’t be available if it is not set up in the process configuration.

5.  Select an existing clustering definition in the **Cluster analysis** field.

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    For more information about running a cluster analysis, see [Perform a cluster analysis](request-cluster-analysis.md).

    If there are no clustering analysis, select **New clustering definition**.

    Provide a name for the clustering analysis and provide fields that you want to use for your cluster analysis, and then select **Configure**.

    **Note:** Cluster analysis won't be available unless the clustering definition is selected in the process configuration.

    For more information, see [Configure a process for a clustering solution](process-configuration-clustering.md).

6.  Select **New clustering definition** if no clustering analysis is available.

    The **New clustering definition** dialog is displayed.

    1.  Provide a name for the clustering analysis.

    2.  Select fields that you want to use for your cluster analysis.

        Remember that records are grouped based on similarity of text in the selected fields.

    3.  Select **Configure**.

7.  Fill the details in **Work notes analysis** section.

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    For information on running work notes analysis, see [Perform work notes analysis](perform-worknotes-analysis.md).

    **Note:** Work notes analysis won't be available unless it is set up in the process configuration.

<table id="table_wmj_zsq_ndc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

**Fields containing work notes**

</td><td>

Select the fields that contain the work notes.

</td><td>

Work notes

</td></tr><tr><td>

**Exclude notes from these users**

</td><td>

Select the users you do not want the notes from.

</td><td>

System users and bots

</td></tr><tr><td>

**Work note time range**

</td><td>

Select the time duration during which the work note must occur to be related to a process step.The default value is 120.

</td><td>

100

</td></tr><tr><td>

**Min work note length**

</td><td>

Select the length less than which the work notes will be disregarded in the analysisThe default value is 5 words.

</td><td>

10

</td></tr><tr><td>

**Max work note length**

</td><td>

Select the length greater than which the work notes will be disregarded in the analysis.The default value is 100 words.

</td><td>

50

</td></tr></tbody>
</table>8.  Fill the details in the **Automation Discovery** section.

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    **Note:** This section is available only when Automation Discovery is available.

    Automation Discovery helps to identify automation opportunities within your processes. You can use the automation discovery reports to implement or improve automation solutions like Virtual Agent \(VA\) or Agent assist. These reports are available on the **Automation Opportunities** tab in the Process Mining workspace.

    For information on configuring Automation Discovery, see [Configure Automation Discovery](config-finding-def-auto-disc.md).

    |Field|Description|
    |-----|-----------|
    |**Turn on automation discovery**|Select the field if you want to use the Automation Discovery feature.|
    |**Field used to surface automation opportunities**|Select the fields for automation opportunities.|
    |**Taxonomy**|Select a taxonomy that will categorize your records using pre-built automation opportunities rather than grouping them into clusters.|
    |**Auto-run with mining**|Select this field if you want to automatically run the automation discovery job every time you mine a project.|

9.  Select **Continue to impact metrics**.


**Parent Topic:**[Create process configuration using Process Configuration Builder](process-config-builder.md)

