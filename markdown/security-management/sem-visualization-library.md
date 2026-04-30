---
title: Visualization library
description: The Visualization library lists all the widgets that you can use to visualize and categorize findings. It includes a set of default widgets and any custom widgets that you create for organization-specific reporting. You can browse the available widgets, understand the data they use, and add them to dashboards to build tailored security exposure views.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 3
breadcrumb: [Administration, Security Exposure Management Workspace, Explore, Unified Security Exposure Management, Security Operations]
---

# Visualization library

The Visualization library lists all the widgets that you can use to visualize and categorize findings. It includes a set of default widgets and any custom widgets that you create for organization-specific reporting. You can browse the available widgets, understand the data they use, and add them to dashboards to build tailored security exposure views.

You can use the Visualization library to:

-   **Explore available widgets**

    Review the complete set of default and custom widgets available for building dashboards.

-   **Understand widget behavior**

    Review key details such as data sources, grouping, visualization type, and activation status to choose the appropriate widget for your analysis.

-   **Create a custom widget**

    Build and configure your own widgets to visualize specific metrics or data insights that matter most to your organization.


The following table lists the available widgets, associated tables, and what they display.

<table id="table_zpg_5n4_d1c"><thead><tr><th>

Widget name

</th><th>

Findings tables

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deferred findings by reason

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Misconfigurations
-   Container vulnerability

</td><td>

Active deferred records grouped by reason.

</td></tr><tr><td>

Findings by assignment group

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Misconfigurations
-   Container vulnerability

</td><td>

Active records assigned to various assignment groups.

</td></tr><tr><td>

Findings by base image

</td><td>

Container vulnerability

</td><td>

Active records categorized by the type of the image.

</td></tr><tr><td>

Findings by CI class

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Misconfigurations

</td><td>

Active records categorized by CI classes.

</td></tr><tr><td>

Findings by cloud resource

</td><td>

-   Infrastructure vulnerability
-   Misconfigurations

</td><td>

Active records categorized by various cloud resources.

</td></tr><tr><td>

Findings by remediation status

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Misconfigurations
-   Container vulnerability

</td><td>

Active records grouped by remediation status.

</td></tr><tr><td>

Findings by risk rating

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Misconfigurations
-   Container vulnerability

</td><td>

Active records categorized by the risk ratings.-   1: Critical
-   2: High
-   3: Medium
-   4: Low
-   5: None

</td></tr><tr><td>

Findings by scan type

</td><td>

Infrastructure vulnerability

</td><td>

Active records grouped by the scan type.

</td></tr><tr><td>

Findings by source

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Misconfigurations
-   Container vulnerability

</td><td>

Active records grouped by the source.

</td></tr><tr><td>

Findings by state

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Misconfigurations
-   Container vulnerability

</td><td>

Active records categorized by various states \(Open, Under Investigation, Awaiting Implementation, In Review, Resolved, and Deferred\).

</td></tr><tr><td>

Findings by technology

</td><td>

Misconfigurations

</td><td>

Active records categorized by technology.

</td></tr><tr><td>

Findings by test group

</td><td>

Misconfigurations

</td><td>

Active records categorized by the test groups.

</td></tr><tr><td>

Findings by Vulnerability

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Container vulnerability

</td><td>

Active records categorized by vulnerability.

</td></tr><tr><td>

Findings by Vulnerability Classification

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Container vulnerability

</td><td>

Active records categorized by vulnerability classification.

</td></tr><tr><td>

Findings not in remediation task

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Misconfigurations
-   Container vulnerability

</td><td>

Active records that are and aren't part of the remediation task.

</td></tr><tr><td>

Findings on external-facing assets

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Misconfigurations
-   Container vulnerability

</td><td>

Active records categorized by the asset exposure to internet.

</td></tr><tr><td>

Findings with exploits

</td><td>

-   Infrastructure vulnerability
-   Application vulnerability
-   Container vulnerability

</td><td>

Active records with and without known exploits.

</td></tr></tbody>
</table>If your instance uses localization, make sure that the widget titles show up correctly in all supported languages. Default widgets already include translated titles.But if you update a default widget, create a custom widget, or rename a widget, remember to add or update the translation entry. This keeps titles consistent across languages. For steps, see [Localize widget titles](../../security-exposure-management-findings/task/sem-localize-widget-titles.md).

**Related topics**  


[Configure Visualization library](../../security-exposure-management-findings/task/sem-configure-visualization-library.md)

[Create a custom widget](../../security-exposure-management-findings/task/sem-create-widget.md)

[Visualization widget fields](../reference/sem-vis-widget-fields.md)

