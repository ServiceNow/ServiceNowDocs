---
title: Working with Teamspaces
description: Strategic Planning can be integrated with Project Portfolio Management's Teamspaces to access and manage relevant projects and demands with the corresponding planning item records.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Strategic Planning with PPM, Agile 2.0, and SAFe, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Working with Teamspaces

Strategic Planning can be integrated with Project Portfolio Management's Teamspaces to access and manage relevant projects and demands with the corresponding planning item records.

You must activate a teamspace plugin to use the teamspace feature. The following teamspace plugins are available:

-   Project Management TeamSpace 1 \(com.snc.ppm\_teamspace\_1\)
-   Project Management TeamSpace 2 \(com.snc.ppm\_teamspace\_2\)
-   Project Management TeamSpace 3 \(com.snc.ppm\_teamspace\_3\)
-   Project Management TeamSpace 4 \(com.snc.ppm\_teamspace\_4\)
-   Project Management TeamSpace 5 \(com.snc.ppm\_teamspace\_5\)

The teamspaces installed with these plugins contain the same components, but the components have different prefixes. For example, teamspace 1 includes a project table named **Teamspace\_1 Project \[tsp1\_project\]** and teamspace 5 includes a project table named **Teamspace\_5 Project \[tsp5\_project\]**.

Also, the corresponding teamspace role must be added to the Strategic Planning admin \(sn\_align\_core.apw\_admin\) role. For example, tsp1\_portfolio\_manager for teamspace1, tsp2\_portfolio\_manager for teamspace2 and so on.

To integrate teamspaces with Strategic Planning records:

1.  Create one alignment integration for all the teamspaces. On the alignment side, create extended tables to store individual teamspace table data \(like TSP1 Portfolio \[sn\_align\_core\_tsp1\_portfolio\], TSP1 Demand \[sn\_align\_core\_tsp1\_demand\], TSP2 Project \[sn\_align\_core\_tsp2\_project\], and so on\).
2.  In the alignment integration, map the extended tables you have created in Step 1, to the respective teamspace tables \(like tsp1\_portfolio, tsp1\_demand, tsp2\_project, and so on\).

![Strategic Planning with teamspaces.](../../apw-internal-integrations/images/for-teamspaces.png "Integration with Teamspaces")

**Related topics**  


[Create a table map](../../apw-internal-integrations/task/create-custom-table-maps-for-custom-planning-items.md)

