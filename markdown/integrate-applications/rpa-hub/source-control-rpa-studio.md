---
title: Resolve conflicts when merging changes from multiple sources of the same activity
description: Resolve conflicts when merging changes from multiple sources of the same activity by using the Source Control option in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/source-control-rpa-studio.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Resolve conflicts when merging changes from multiple sources of the same activity

Resolve conflicts when merging changes from multiple sources of the same activity by using the **Source Control** option in RPA Desktop Design Studio.

## Before you begin

If you're not connected to a ServiceNow instance, click the Connection Manager icon under the **Design** tab to connect to an existing instance. For more information, see [Set up RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/set-up-rpa-studio.md).

Create an activity. For more information, see [Create and use an activity in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-activity-rpa-studio.md).

Role required: none

## Procedure

1.  Open the project that has the activity that you want to resolve conflicts in.

2.  In the Project Explorer pane, navigate to **Activities**.

3.  Right-click the activity and select **Source Control**.

4.  In the COMPARE PROCESSES dialog box, under the Remote section, select any of the following source types to open the automation project from the **Source** field.

<table id="choicetable_kpm_xyv_prb"><thead><tr><th align="left" id="d92276e134">

Option

</th><th align="left" id="d92276e137">

Action

</th></tr></thead><tbody><tr><td id="d92276e143">

**Remote**

</td><td>

1.  Click the Open Project icon \(\[Omitted image "connection-manager-icon.png"\] Alt text: Open Project icon.\).
2.  In the Open Project dialog box, select a package name and a version.
3.  Click **Open**.
4.  Click **Save** to save the Project in the default location.
5.  From the Select a Document version list, select a package version.


</td></tr><tr><td id="d92276e182">

**Local**

</td><td>

1.  Click **Browse**.
2.  In the Open dialog box, select a project.
3.  Click **Open**.


</td></tr></tbody>
</table>    The changes are highlighted in the COMPARE PROCESSES dialog box as shown in the following example. If changes are added, they appear in green. If the changes are removed, they appear in red. If the changes are modified, they appear in yellow.



5.  Under the Local section, select any of the following options for resolving conflicts from the **In conflict** field:

    -   Select **Keep current items** to retain the changes in the Local section.
    -   Select **Replace** to replace the highlighted changes in the Local section with the highlighted changes in the Remote section.
6.  In the CONFIRM dialog box, click **OK**.

7.  Click **Merge with current**.


**Parent Topic:**[Using automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/rpa-studio-use.md)

