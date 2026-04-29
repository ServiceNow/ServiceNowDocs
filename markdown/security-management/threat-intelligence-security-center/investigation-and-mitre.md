---
title: Investigation canvas and MITRE ATT&amp;CK
description: In the Investigation Canvas, you can view the MITRE ATT&amp;CK techniques and sub-techniques associated with all nodes currently present on the canvas.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Investigation Canvas, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Investigation canvas and MITRE ATT&amp;CK

In the Investigation Canvas, you can view the MITRE ATT&amp;CK techniques and sub-techniques associated with all nodes currently present on the canvas.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

4.  Open any case.

5.  Go to **Investigation Canvas** tab.

6.  On the investigation canvas, use the **Resizeable panels divider handle** to drag to view the MITRE ATT&amp;CK framework.

7.  Select the required MITRE ATT&amp;CK matrix from the **Matrix** drop-down list.

    ![Investigation Canvas MITRE Framework.](../image/tisc-investigation-canvas-mitre.png)

    The MITRE ATT&amp;CK Framework shows different levels of tactics and techniques association.

    1.  The top row displays all the tactics present in the selected MITRE ATT&amp;CK matrix.

    2.  By default, each tactic shows the count of total techniques and sub-techniques associated with it.

    3.  Use the **Refresh** icon to reload the MITRE ATT&amp;CK framework and view the latest technique-tactic associations.

    4.  View the MITRE ATT&amp;CK techniques and sub-techniques related to all the nodes \(entities\) in the canvas.

    5.  Click on one or more node\(s\) to view the associated MITRE ATT&amp;CK techniques and sub-techniques related to those selected node\(s\) in the canvas.

        **Important:** In the framework, the techniques and sub-techniques that are associated with the nodes in the canvas are highlighted.

8.  Select **Filters** to enable you to create and save filters for TTPs associated with specific adversaries and other MITRE technique attributes.

    For more information on the MITRE Filtering options, see [Investigation Canvas MITRE Filters](../task/tisc-mitre-filters.md).

9.  Use **View Controls** for advanced filtering options.

    Once you select the appropriate filter, it will display only the MITRE ATT&amp;CK techniques and sub-techniques associated with the selected node\(s\). The options in the **View Controls** list are:

    -   **Show ID**: Displays the unique technique ID \(for example `T1059`\) on each card for easy reference.
    -   **Show Sub Techniques**: Displays the sub-techniques. This option automatically expands the parent technique cards to display their sub-techniques, without requiring manual expansion.
    -   Select **Show Only Associated Techniques**: Displays only the techniques that are currently linked to nodes on the investigation canvas, hiding any irrelevant techniques even if they meet the filter criteria. When this option is selected, each tactic displays the total count of associated techniques and sub-techniques currently linked to the canvas.
10. Click on the pop out icon to view the MITRE ATT&amp;CK Framework in a larger space.

    **Important:**

    -   Whenever you add or remove a node, the MITRE ATT&amp;CK framework refreshes automatically. You can also use the refresh icon to perform a manual refresh at any time.
    -   Whenever you filter specific types of nodes, the MITRE ATT&amp;CK framework refreshes automatically to reflect the changes.

-   **[Investigation Canvas MITRE Filters](../task/tisc-mitre-filters.md)**  
MITRE filters enables you to create and save filters for Tactics, Techniques, and Procedures \(TTPs\) associated with specific adversaries and other MITRE technique attributes.

**Parent Topic:**[Working with Investigation Canvas](tisc-investigation-canvases.md)

