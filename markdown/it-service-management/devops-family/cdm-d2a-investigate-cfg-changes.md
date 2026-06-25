---
title: Investigate an alert that involves a change to config data
description: A high percentage of alerts occur due to errors in config data. If the chain of events that resulted in an alert includes a change request that involves the same CI as the alert, then you can use a variety of tools to isolate the config changes that might have caused the alert.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-family/cdm-d2a-investigate-cfg-changes.html
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Using DevOps Config, DevOps Config, IT Service Management]
---

# Investigate an alert that involves a change to config data

A high percentage of alerts occur due to errors in config data. If the chain of events that resulted in an alert includes a change request that involves the same CI as the alert, then you can use a variety of tools to isolate the config changes that might have caused the alert.

## Before you begin

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

Roles required: Both cdm\_viewer and evt\_mgmt\_user.

## About this task

You work in the **Config changes** tab while investigating the causes of an alert. The tab includes several tools that enable you to visualize the series of config changes that might have led to the alert. You can filter, sort, and organize config data to help you identify problematic changes to the configuration data item key:value pairs \(CDIs\).

## Procedure

1.  Use either of the following methods to view an alert:

    -   On the home page \(\[Omitted image "cdm-icon-home.png"\] Alt text: homepage icon\) of the Service operations workspace, select an alert.
    -   On the list page \(\[Omitted image "cdm-icon-list.png"\] Alt text: list page icon\) of the Service operations workspace, navigate to **Alerts** and then select an alert.
    The top five most likely causes of the alert are listed in the Cause section on the **Overview** tab. If the chain of events that resulted in the alert includes a change request that involves the same CI as the alert, then that CHG record appears in the list.

    \[Omitted image "cdm-probable-root-causes-subtab.png"\] Alt text: CHG record listed on the Changes tab

2.  On the **Changes** tab, select a change request.

    The change request opens. If the change request involved a change to config data because a CDM snapshot was deployed, then the **Config changes** tab appears.

3.  On the **Config changes** tab, work with the information in the Investigate configuration changes section.

    \[Omitted image "cdm-config-changes-tab-timeline.png"\] Alt text: View the timeline of released snapshots on the Config changes tab

<table id="table_vy2_dhb_vtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application

</td><td>

The CDM application that is affected by the alert.

</td></tr><tr><td>

Deployable

</td><td>

The CDM deployable whose snapshot was deployed.

</td></tr><tr><td>

Snapshot

</td><td>

The CDM snapshot that was deployed.

 To open the snapshot on a new tab in the Service Operations Workspace, select the snapshot.

</td></tr><tr><td colspan="2">

Snapshot deployment timeline

</td></tr><tr><td>

Date range / Start date / End date

</td><td>

The time period that the timeline displays. By default, the timeline displays the period that includes the alert, the target snapshot \(the snapshot that is associated with the change request\), and the five most recently deployed snapshots.

 Specify a predefined period in the **Date range** box or use the calendar tools to specify custom start and end times.

</td></tr><tr><td>

Timeline / Show legend

</td><td>

The timeline displays snapshot deployments and the alert.

 Select **Show legend** to view the icons that identify snapshots and events on the timeline.

 In addition to the snapshot that immediately precedes the current \(target\) snapshot, you can compare the target snapshot to any earlier snapshot that appears on the timeline. To view additional snapshots, change the date range.

 Use the zoom icons \(\[Omitted image "cdm-icon-zoom.png"\] Alt text: zoom icons\) to shrink or grow the portion of the date range that appears on the timeline. Zoom does not change any of the other timeline settings. Use the left and right arrows to view items that have scrolled out of view.

 Select a snapshot to view its name, associated change record, and deployment date. Select the link to open the associated change request.

 \[Omitted image "cdm-snapshot-click-on-timeline.png"\] Alt text: Select a snapshot to view more information

 Select an alert to view its alert ID and creation date.

 \[Omitted image "cdm-alert-click-on-timeline.png"\] Alt text: Select an alert to view more information

</td></tr><tr><td>

Reference snapshot / Target snapshot

</td><td>

The target snapshot is the snapshot that is associated with the change request. \(The alert can be associated with multiple change requests, each of which is associated with a target snapshot\). Most often, the target snapshot immediately precedes the alert.

 By default, the system selects the snapshot that immediately preceded the target snapshot as the reference snapshot.

 While investigating the cause of the alert, you can use the **Reference snapshot** list to select any snapshot that precedes the reference snapshot in the selected date range on the timeline. \(Snapshots on the timeline after the target snapshot do not appear in the list.\) If you select a different reference snapshot, select **Compare** to generate the list of differences between the two selected snapshots. The difference information appears in the Configuration changes section.

 For any snapshot on the timeline, follow these steps to open it in the Service Operations workspace.

1.  Choose the target snapshot or select a snapshot in the **Reference snapshot** list.
2.  Select **Open snapshot**.


</td></tr></tbody>
</table>4.  Now work with the information in the Configuration changes section on the **Config changes** tab.

    When the **Config changes** tab opens, the system immediately identifies the differences in the CDIs between the reference snapshot and the target snapshot. The Configuration changes section displays the differences.

    The letters in the following illustration identify the tools you can use to analyze the data.

    \[Omitted image "cdm-configuration-changes-section-annotated.png"\] Alt text: Tools in the Configuration changes section

    -   **A. Navigation panel**

        The navigation panel displays the node structure of the snapshot. Select a node to view its contents in the data panel. Nodes that include changed CDIs \(either directly or in descendent nodes\) are annotated with **added**, **deleted**, or **edited**, as appropriate. Use the **Search** field to search for text in the navigation panel.

    -   **B: Data panel**

        The data panel displays groups of CDIs for the selected node. By default, the root node is selected in the node tree, and the list includes all CDIs for both snapshots. Select a node in the navigation panel to display CDIs for only that node and its descendents. You can switch from this list view of the config data to a script view, as described in [G: Script view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-d2a-investigate-cfg-changes.md).

        Expand and close groupings with the expand icon \(\[Omitted image "cdm-icon-expand.png"\] Alt text: expand icon\). If a selection includes more than 50 CDIs, then CDIs are organized into groups of 50.

    -   **C: Diff only**

        Select **Diff only** to view only CDIs that differ between the two snapshots.

    -   **D: Filter the types of changes that should appear in the list**

        The condition builder icon \(\[Omitted image "icon-filters.png"\] Alt text: condition builder icon\) appears when you point to the **Actions** column name in the list view. Select the icon to specify the types of config data changes that should appear in the list.

        |Filter|Meaning|
        |------|-------|
        |\(empty\)|\[Not used.\]|
        |--|No difference in this CDI between the reference and target snapshots.|
        |Added|The CDI was added to the target snapshot.|
        |Deleted|The CDI was deleted from the target snapshot.|
        |Changed|The value of the CDI was changed in the target snapshot.|

    -   **E: Filter the list based on CDI names and values**

        The condition builder icon \(\[Omitted image "icon-filters.png"\] Alt text: condition builder icon\) appears when you point to the **Key label** column in the list view. Select the icon to filter the list of config data changes that should appear in the list.

        The sort indicator icon \(\[Omitted image "cdm-icon-sort-list.png"\] Alt text: sort indicator icon\) indicates that CDIs are sorted alphabetically by the label of the key.

        \[Omitted image "cdm-filter-list.png"\] Alt text: Filter lists of changes

    -   **F: Find nodes with a particular kind of change**

        In the list view, select the find icon \(\[Omitted image "cdm-icon-find-page.png"\] Alt text: find icon\) and specify the type of change to isolate.

        \[Omitted image "cdm-find-page-in-list.png"\] Alt text: Find nodes with a particular kind of change

    -   **G: Script view**

        -   The data initially appears in list form. Select **Script view** to view the config data as code.
        -   Differences are indicated by symbols next to the line number.
            -   Deletions are indicated by -
            -   Additions are indicated by +
            -   Edits are indicated by the pencil icon \(\[Omitted image "icon-edit-pencil.png"\] Alt text: pencil icon\) plus notes in the in-line text, as shown in this "Diff only" example.
        -   Conversions from text to array: In the example, because the data structure of the `googleApiKey` CDI changed from a text value to an array, the text form is deleted and the array form is added.
        \[Omitted image "cdm-configuration-changes-script-view.png"\] Alt text: The script view includes symbols that indicate the type of change


