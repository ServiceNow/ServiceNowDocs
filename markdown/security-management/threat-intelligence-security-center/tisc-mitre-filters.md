---
title: Investigation Canvas MITRE Filters
description: MITRE filters enable you to create and save filters for Tactics, Techniques, and Procedures \(TTPs\) associated with specific adversaries and other MITRE technique attributes.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-23"
reading_time_minutes: 3
breadcrumb: [Investigation canvas and MITRE ATT&amp;CK, Working with Investigation Canvas, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Investigation Canvas MITRE Filters

MITRE filters enable you to create and save filters for Tactics, Techniques, and Procedures \(TTPs\) associated with specific adversaries and other MITRE technique attributes.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

Analysts can use the filters available on the MITRE card to filter specific actor TTPs that are relevant to adversaries involved in the investigation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

4.  Open any case.

5.  Go to **Investigation Canvas** tab.

6.  Select **Filters** to create filters for Tactics, Techniques, and Procedures \(TTPs\) associated with specific adversaries and other MITRE technique attributes.

7.  Fill in the necessary values in the filter panel to apply your desired filters.

    The MITRE filter panel enables you to filter and visualize MITRE ATT&amp;CK techniques based on selected criteria such as Groups, Malware, Tools, Tags, and Priority.

<table id="table_bld_4lg_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Saved Filters

</td><td>

Analysts can save specific criteria as **Saved Filters** for reuse. Filters saved by an analyst are user-specific.**Note:** For example, if Analyst X saves a filter configuration, it will only be visible to Analyst X. When another analyst log in and view the filter drop down, they will not see the filters saved by others.

This ensures that each user can create and manage personalized views without affecting or being affected by other users' filter preferences.

</td></tr><tr><td>

Filter Name

</td><td>

Name of the filter.

</td></tr><tr><td>

MITRE Group

</td><td>

Indicates the MITRE Group. Select one or more groups to filter techniques associated with them.

</td></tr><tr><td>

MITRE Malware

</td><td>

Indicates the MITRE Malware. Select one or more malware items to filter techniques associated with them.

</td></tr><tr><td>

MITRE Tools

</td><td>

Indicates the MITRE Tools. Select one or more tools to filter techniques associated with them.

</td></tr><tr><td>

TISC Tags

</td><td>

Indicates the TISC tags. Select one or more tags to filter techniques based on their classification.

</td></tr><tr><td>

Priority of Techniques

</td><td>

Indicates the priority level of techniques. You can select one or more options to filter techniques based on their assigned priority.

</td></tr><tr><td>

Clear All

</td><td>

Allows you to clear the inputs entered in the filter panel.

</td></tr><tr><td>

Save as New Filter

</td><td>

Saves the criteria entered in the filter panel as a new saved filter.**Note:** Saved filter name should be unique.

</td></tr><tr><td>

Save Current Filter

</td><td>

Saves changes to the criteria in the currently selected saved filter.You can also rename a filter using this option.

**Note:** Saved filter name should be unique.

</td></tr><tr><td>

Apply

</td><td>

This option allows you to apply the changes to your filters in the MITRE card.

</td></tr><tr><td>

Delete

</td><td>

Select this option to remove a selected saved filter.When you click the **Delete** button next to a saved filter, a confirmation message appears if you are sure you want to delete this filter. Confirming this action will permanently remove the saved filter.

To remove an individual field value within the filter panel, click the **Delete \(trash\)** icon next to that specific field.

</td></tr></tbody>
</table>    By applying filters using these values, the MITRE matrix is dynamically updated to display only those techniques associated with the selected attributes. This focused view enables analysts to concentrate more on the most relevant Tactics, Techniques, and Procedures \(TTPs\) during investigations.

    In addition, analysts can further narrow down TTPs using filters for malware, tools, tags, and priority levels.

    ![MITRE Filters](../image/tisc-mitre-filter-panel.png)

8.  Select **Save as New Filter** to save your filter criteria.

9.  Select **Apply** to apply the changes.


## Filtering by MITRE Group

Select a MITRE group as APT32 \(G1001, see the following screen shot\). When you apply this filter, the MITRE matrix updates to display only those techniques that are directly linked to the selected group.

![Investigation Canvas - MITRE filters example](../image/tisc-investigation-mitre-filter-example.png)

This focused view helps analysts to concentrate specifically on the Tactics, Techniques, and Procedures \(TTPs\) associated with the selected threat group.

When you apply the filter, a few techniques in the matrix are displayed in blue text, while other techniques appear in gray.

![TISC Investigation Canvas MITRE Techniques and sub-techniques.](../image/tisc-investigation-canvas-mitre-colors.png)

The visual representation on the MITRE Framework indicates how techniques and sub-techniques relate to the applied filters and investigation context.

-   **Blue text:** Techniques or sub-techniques shown in blue text indicate those that match the filter criteria.
-   **Blue text in bold with blue border:** Techniques or sub-techniques displayed in bold blue text with a blue border indicate those that match the filter criteria and are associated with one or more nodes on the canvas.
-   **Gray card:** Parent techniques are displayed in gray when they do not directly match the filter criteria \(which means they are not linked to the selected group\) but are shown to represent the parental relationship to linked sub-techniques that match the filter criteria.

**Parent Topic:**[Investigation canvas and MITRE ATT&amp;CK](../concept/investigation-and-mitre.md)

