---
title: Add personas to a project
description: Each project has several personas with different roles in the Performance Analytics solution that you are designing. A persona is a role within your company, such as service desk manager or service owner.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [KPI Composer projects, Design your Performance Analytics solution with KPI Composer, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Add personas to a project

Each project has several personas with different roles in the Performance Analytics solution that you are designing. A persona is a role within your company, such as service desk manager or service owner.

Prerequisites
:   [Create a KPI Composer project](create-kpi-composer-project.md)

## Before you begin

Role required: sn\_kpi\_composer.user \(own project\), sn\_kpi\_composer.admin \(any project\), admin. No role required for responsible user or user with edit access from project sharing.

## Procedure

1.  Navigate to **All** &gt; **KPI Composer** and create or open a project.

2.  In the Analysis tab, click the persona icon \(![](../image/kpi-comp-persona-icon.png)\) at the top right of the screen.

3.  In the Persona dialog, click **Add item**.

4.  Type the name of the new persona and click outside the text box.

    The persona appears in the header of the KPI tree canvas. Each persona automatically gets a 2-letter identifier, which is based on the first two words \(or first two letters if only one word\) that are in the name.

5.  Repeat these steps to add more personas.


## Adding personas to a KPI Composer project

In the following short animation, you see how to add the personas Agent and CIO to a project. Then you see how to add the CIO persona to a Business Goal. ![Creating personas and adding one to an artifact](../image/kpi-comp-add-persona.gif)

## What to do next

Drag personas onto existing artifacts on the canvas to add them to those artifacts. You can add an unlimited number of personas to any artifact. If an artifact has more than three personas, the full names of the personas are hidden. To see the full names, point to the personas.

By holding down the Ctrl/Command or Alt/Option key while dropping a persona onto an artifact, you activate the following advanced functions:

-   **Hold Ctrl while dropping**

    Add the persona to the artifact on which it is dropped and to all child artifacts of that artifact.

-   **Hold Alt while dropping**

    Remove the persona from the artifact on which it is dropped.

-   **Hold Ctrl and Alt while dropping**

    Remove the persona from the artifact on which is dropped and from all child artifacts of that artifact.


**Parent Topic:**[KPI Composer projects](../concept/kpi-composer-projects.md)

**Previous topic:**[Define properties for a project](define-properties-project.md)

**Next topic:**[Group data by breakdown definitions](add-breakdowns-project.md#)

