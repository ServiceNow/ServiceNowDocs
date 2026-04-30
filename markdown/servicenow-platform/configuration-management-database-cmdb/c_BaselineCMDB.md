---
title: Baseline CMDB
description: CMDB baseline provides capabilities that help you understand and control the changes that have been made to your configuration items \(CIs\) in the CMDB.You can create a baseline for a CI to track updates to the CI over time.You can see the changes that have been made to a CI or any first level related CIs by configuring the CI form layout to display the CMDB Baseline diff field. This field is labeled Baseline differences on the form.Use the baseline CMDB properties to configure how many changes and relationships for a CI can appear in the baseline diff for the CI.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Baseline CMDB

CMDB baseline provides capabilities that help you understand and control the changes that have been made to your configuration items \(CIs\) in the CMDB.

-   You can create a baseline, which is a snapshot of your configuration items in the CMDB. You can review the changes that have been made to that configuration item since a previous baseline. Multiple baselines may be created and the system tracks the changes that have been made per baseline.

    Creating a baseline captures the attributes of the CI as well as all first-level relationships for the CI. Any changes to the base CI or to any related CIs are captured and displayed. Newly created CIs are not automatically added to a baseline.

-   Associate a configuration item with a task, a change or change task, and to propose changes to the CI after the change is complete. You can record changes, and these changes are not applied to the CI immediately but are delayed until the change is complete.

    When the change is complete, you can choose to apply the proposed changes which makes all changes previously proposed and associates the changes with the task.

    For information about planning and implementing a baseline CMDB, see the [CMDB Baseline life-cycle best practices and Diff Formatter troubleshooting \[KB0829681\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0829681) knowledge base article.


## Create a CMDB baseline

You can create a baseline for a CI to track updates to the CI over time.

### Before you begin

Role required: ecmdb\_admin and itil

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Baselines** &gt; **Baselines**.

2.  Click **New**.

3.  Enter a **Name** for the baseline.

    By default, the cmdb\_ci table is selected so that the record creates the baseline for all configuration items in the system.

4.  To limit the baseline to specific CIs, select a different **Table** or choose **Conditions** that a CI must meet for it to have a baseline entry.

    For example, you might create a baseline for the Database table with the condition **\[Location\] \[is\] \[&lt;configured location&gt;\].**

5.  Click **Submit**.

    The creation of a baseline is time consuming and occurs in the background. A message at the top of the record list notifies you that your baseline has been scheduled and you will receive an email when the process is complete.


## Display baseline differences

You can see the changes that have been made to a CI or any first level related CIs by configuring the CI form layout to display the CMDB Baseline diff field. This field is labeled Baseline differences on the form.

### Before you begin

Role required: itil

### About this task

Changes are displayed only for the cmdb\_ci table and child tables. You can change the **com.cmdb.baseline.max\_changes** system property to limit the number of relationships and changes that appear in a baseline diff section on a CI form \(set to 100 by default\).

### Procedure

1.  Open a CI record.

2.  Select the baseline you want to see for this CI from the choice list.

    The field displays the details of any changes that were made to the current record for the selected baseline, or indicates that no changes were made.

    ![Baseline differences](../image/DetailsOfBaselineDifferences.png "Details of baseline differences")

3.  To add a relationship to the CI, click the green plus icon in the **Related Items** toolbar.

    The new relationship appears below the toolbar. For more information about the Related Items toolbar and how to control the display, see [CI relations formatter](c_CIRelationsFormatterNG.md).

4.  Update a related CI and see the changes displayed as **Basic attribute changes** in the current CI record.

    ![Basic attribute changes in baseline differences.](../image/BasicAttributeChanges.png "Basic Attribute Changes")


### What to do next

To improve performance and prevent memory issues when showing large amounts of baseline differences data on CI forms, complete the following steps:

1.  Set the system property **com.cmdb.baseline.entry.attachment** to true.
2.  Manually run once the **CMDB Baseline convert XML to attachment** fix script. For information about running a fix script, see [Run fix scripts](https://www.servicenow.com/docs/access?context=t_RunFixScripts&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Properties for baseline CMDB

Use the baseline CMDB properties to configure how many changes and relationships for a CI can appear in the baseline diff for the CI.

These properties are available for baseline CMDB. To view and edit these properties, the admin role is required.

<table id="table_uwy_fwz_mhb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum number of changes and relationships for a CI that can appear in the baseline diff for the CI.

 com.cmdb.baseline.max\_changes

</td><td>

-   Type: integer
-   Default value: 100
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Baseline Properties**

</td></tr><tr><td>

com.cmdb.baseline.entry.attachment

</td><td>

Lets you manually run the **CMDB Baseline convert XML to attachment** fix script. Setting this property to true and then running the **CMDB Baseline convert XML to attachment** fix script, enables improved performance when showing large amounts of baseline differences data on CI forms.

 When false, the CMDB Baseline Diff component uses legacy methods which might fail to load large amounts of baseline differences data.

 -   Type: true \| false
-   Default value: false
-   Location: [Add to System Properties \[sys\_properties\]](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) table.
-   Learn more: [Baseline CMDB](c_BaselineCMDB.md#)

</td></tr></tbody>
</table>