---
title: Working with Investigation Canvas
description: The Investigation Canvas is a key significant feature, which provides more valuable information for the Threat Intelligence \(TI\) analysts. It provides a structured framework by mapping one to one or one to many relationships and visualizing information related to observables, indicators of compromise \(IOCs\), or entities.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Working with Investigation Canvas

The Investigation Canvas is a key significant feature, which provides more valuable information for the Threat Intelligence \(TI\) analysts. It provides a structured framework by mapping one to one or one to many relationships and visualizing information related to observables, indicators of compromise \(IOCs\), or entities.

By using the investigation canvas, threat analysts can effectively:

-   **Map Relationships**: Visualize node connections between various entities such as observables, indicators of compromise \(IOCs\), threat actors, attack patterns, affected assets, and more. Each object on the investigation canvas is represented by a specific color, along with its object type, node type, and status. The status reflects the object's reputation such as **Suspicious**, **Low**, or **Critical** for observables and other object types. Indicators are displayed with their associated threat severity to help prioritize analysis.
-   **Link cases or canvases**: Link a case or canvas to enhance the analysis and provide a more comprehensive view of the threat landscape within the case management.
    -   The linking feature enables analysts dynamically add or remove nodes. This also populates the existing relationships between the nodes to the canvas.
    -   Temporary Relationship graphs by saving relationships separately within the context of the Investigation Canvas.
-   **MITRE technique associations**: Associate or remove MITRE techniques with nodes directly on the canvas and provide analysis on the MITRE kill chain card.

## Entry Points for the investigation canvas

1.  **First entry point: New Blank Canvas**: This entry point should allow the analysts to open a new and blank canvas without any nodes or links.
2.  **Second Entry Point: Open Canvas in Case Investigation**:
    1.  This entry point opens an existing investigation case and allows to edit, modify, and rename the canvas.
    2.  A new canvas with existing artifacts as nodes.

-   **[Working with Actions on the Investigation Canvas](tisc-canvas-actions.md)**  
This section describes the various actions that you can perform on the investigation canvas.
-   **[Linking an existing case from Investigation Canvas](../task/tisc-link-existing-case-canvas.md)**  
Use this section to link an existing case from the investigation canvas.
-   **[Creating a Case and Linking from Investigation Canvas](../task/tisc-link-case.md)**  
Use this section to create and link a case\(s\) from an investigation canvas.
-   **[Linking Canvas from a Case](../task/tisc-link-canvas-from-case.md)**  
Use this section to link a canvas from a case.
-   **[Create an investigation canvas](../task/tisc-create-canvas.md)**  
Create a new canvas to add observables from threat intelligence library.
-   **[Adding a new node to the canvas](../task/tisc-add-node-canvas.md)**  
Use this section to create and add new entities, including observables or objects, directly from the investigation canvas.
-   **[Investigation canvas and MITRE ATT&amp;CK](investigation-and-mitre.md)**  
In the investigation canvas, view the MITRE ATT&amp;CK techniques and sub-techniques which are associated to all the nodes in the canvas.

**Parent Topic:**[Threat Analyst Workbench](threat-analyst-workbench.md)

**Related topics**  


[Workbench Overview](workbench-overview.md)

[Creating cases using Threat Analyst Workbench](create-cases-using-threat-analyst-workbench.md)

[Create case task using Threat Analyst Workbench](../task/tisc-create-case-task.md)

[Add artifacts to case\(s\) or case task\(s\)](../task/add-artifacts-to-a-case-s.md)

[Run Enrichment Actions within a case](../task/run-enrichment-results.md)

[View Case Reports](../task/view-case-reports.md)

[Create a security incident from a TISC case](../task/tisc-create-si-case.md)

[Upload Secure File Attachments](../task/secure-file-attachments.md)

