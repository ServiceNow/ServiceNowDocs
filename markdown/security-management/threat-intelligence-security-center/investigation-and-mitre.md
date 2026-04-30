---
title: Investigation canvas and MITRE ATT&amp;CK
description: In the investigation canvas, view the MITRE ATT&amp;CK techniques and sub-techniques which are associated to all the nodes in the canvas.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Working with Investigation Canvas, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Investigation canvas and MITRE ATT&amp;CK

In the investigation canvas, view the MITRE ATT&amp;CK techniques and sub-techniques which are associated to all the nodes in the canvas.

**Important:** In the framework, the techniques and sub-techniques that are associated with the nodes in the canvas are highlighted.

Role required: sn\_sec\_tisc.analyst

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.
2.  Click the **Threat Analyst Workbench** icon.
3.  Go to **Case Management** &gt; **All Cases**. All the cases are displayed.
4.  Select any case.
5.  Go to **Investigation Canvas** tab.
6.  On the investigation canvas, use the **Resizeable panels divider handle** to drag to view the MITRE ATT&amp;CK framework.
7.  Select the required MITRE ATT&amp;CK matrix from the **Matrix** drop-down list. The MITRE ATT&amp;CK Framework shows different levels of tactics and techniques association.
    -   The top row displays all the tactics that are present in the selected **Matrix**. By default, all the tactics display the count of the total techniques and sub-techniques present for that corresponding tactics. You can use the **Refresh** icon to reload the MITRE ATT&amp;CK framework and view the latest associations.
    -   Under each tactic, the framework displays all the techniques that are present as a relationship to that corresponding tactic.
    -   The framework displays the sub-techniques that are present under each technique. Expand each technique to view the sub-techniques.
8.  View the MITRE ATT&amp;CK techniques and sub-techniques related to all the nodes \(entities\) in the canvas.
9.  Click on one or more node\(s\) to view the associated MITRE ATT&amp;CK techniques and sub-techniques related to those selected node\(s\) in the canvas.
10. Use **View Controls** to view the associated MITRE ATT&amp;CK techniques and sub-techniques of the selected node\(s\). From the controls lists:
    -   Select **Show ID** to view the techniques and sub-techniques MITRE IDs.
    -   Select **Show Sub Techniques** to view all the sub-techniques. When you select this option, all the techniques are shown in the expanded view. The expanded view of the technique shows all the sub-techniques that are present for that corresponding technique.
    -   Select **Show Only Associated Techniques** to view only MITRE techniques that are associated to the nodes in the canvas. When you select this option, each tactic shows the total number of associated techniques and sub-techniques.
11. Click on the pop out icon to view the MITRE ATT&amp;CK Framework in a larger space.

**Important:**

-   Whenever you add or remove a node, the MITRE ATT&amp;CK framework gets refreshed automatically and you can also use the refresh icon to do a manual refresh.
-   Whenever you filter the specific types of nodes, even then the MITRE ATT&amp;CK framework gets refreshed.

-   **[Investigation Canvas MITRE Filters](../task/tisc-mitre-filters.md)**  
MITRE filters enable you to create and save filters for Tactics, Techniques, and Procedures \(TTPs\) associated with specific adversaries and other MITRE technique attributes.

**Parent Topic:**[Working with Investigation Canvas](tisc-investigation-canvases.md)

