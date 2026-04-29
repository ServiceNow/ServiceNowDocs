---
title: Configure investigative features
description: Configure investigative features to set advanced analytics features for a process.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [With Process Configuration Builder, Creating process configuration, Use, Process Mining, Platform Analytics]
---

# Configure investigative features

Configure investigative features to set advanced analytics features for a process.

## Before you begin

Role required: sn\_process\_mining\_power\_user or sn\_process\_mining\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the side of the page, select the Process configurations icon \(![Process configuration builder](../image/icon-process-config.png)\).

3.  Open a table from the **Configurations** tab.

    The **Process details** page is displayed. Select **Investigative features** from the side panel.

    If you’re proceeding from the **Recommendations setup** page, then you come to this page. For more information, see [Configure recommendations setup](reco-setup.md).

    The **Investigative features** page has four sections:

    -   Automated root cause analysis
    -   Cluster analysis
    -   Work notes analysis
    ![Investigative features in process configuration](../image/invest-features-config.png)

4.  Add fields that you want for automated root cause analysis in the **Automated root cause analysis** field.

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    Based on your inputs on the **Process details** page, you get recommendations for automated root cause analysis.

    When you set up the automated root cause analysis, you can initiate a root cause analysis in your project that is based on this table. For more information on running root case analysis, see [Run automated root cause analysis reports](run-view-arca.md).

    **Note:** If the automated root cause analysis isn’t set up in the process configuration, it isn’t available.

5.  Select an existing clustering definition in the **Intent and activity analysis** field.

    **Note:** Intent and activity analysis isn’t available unless specified in the process configuration. Also, if the Intent and Activity Analysis skill is not activated in Now Assist for Creator, then the section is not available for edit. For more information on Intent and Activity Analysis skill, see [Working with intent and activity analysis](../concept/nowass-intent-activity-analysis.md).

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    For more information about running a cluster analysis, see [Perform a cluster analysis](request-cluster-analysis.md).

    If there are no clustering analyses, select **New clustering definition**.

    Provide a name for the clustering analysis and provide fields that you want to use for your cluster analysis, and then select **Configure**.

    For more information, see [Configure a process for a clustering solution](process-configuration-clustering.md).

6.  Select **New clustering definition** if no clustering analysis is available.

    The **New clustering definition** dialog is displayed.

    1.  Provide a name for the clustering analysis.

    2.  Select fields that you want to use for your cluster analysis.

        Remember that records are grouped based on similarity of text in the selected fields.

    3.  Select **Configure**.

7.  Fill the details in **Transition work notes analysis** section.

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    For information on running work notes analysis, see [Perform work notes analysis](perform-worknotes-analysis.md).

    **Note:** Work notes analysis isn’t available unless it’s set up in the process configuration.

    You can use the Now Assist feature for work notes analysis even with 5-50 eligible work notes. If there are less than 25 eligible work notes, clustering isn’t performed. It puts all the work notes into one LLM call. Otherwise, clustering is performed before calling the LLM.

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

Select the users that you don’t want the notes from.

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

Select the length less than which the work notes are disregarded in the analysisThe default value is 5 words.

</td><td>

10

</td></tr><tr><td>

**Max work note length**

</td><td>

Select the length greater than which the work notes are disregarded in the analysis.The default value is 100 words.

</td><td>

50

</td></tr></tbody>
</table>8.  Select **Continue to impact metrics**.


**Parent Topic:**[Create process configuration using Process Configuration Builder](process-config-builder.md)

