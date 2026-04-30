---
title: Create a report definition
description: You can create a new KPI Composer report definition directly from the relevant artifact in the Data Definition tab. Fill the report definition with the necessary information for creating a report.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Defining indicators and reports, Design your Performance Analytics solution with KPI Composer, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a report definition

You can create a new KPI Composer report definition directly from the relevant artifact in the Data Definition tab. Fill the report definition with the necessary information for creating a report.

## Before you begin

You have an existing [KPI Composer project](../concept/kpi-composer-projects.md) with a complete draft of the [KPI tree](../concept/design-kpi-tree.md#) in the Analytics tab. You also need technical knowledge of Reporting.

Role required: sn\_kpi\_composer.admin or admin to link to an existing report, sn\_kpi\_composer.user for other functionality. Responsible users and users with edit access also can use any functionality other than linking to an existing report.

## Procedure

1.  Navigate to **All** &gt; **KPI Composer** and open the relevant project.

2.  Navigate to the Data Definition tab.

3.  Locate an artifact that has a **create report definition** link and open that link.

    Only artifacts associated with Report widgets in the Dashboard Visualization tab have links for creating report definitions.

4.  Provide a name and a description for the report.

    By default, the report definition has the same name as the artifact that contains it. This default name is the same as the default for an indicator definition for that artifact, so consider differentiating them.

5.  In the **Development instructions** field, provide the developer with any technical information they need besides the report properties.

    The **Description** field should contain information for the user. The **Development instructions** field should contain internal information for the developer.

6.  Select either a **Facts Table** or a **Report Source**.

7.  In the **Condition** field, describe the filtering conditions for the report.

    You can write the conditions in plain text instead of the condition builder syntax.


**Parent Topic:**[Defining indicators and reports](../concept/designing-indicators.md)

