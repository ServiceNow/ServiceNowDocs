---
title: Data for problem resolution
description: The quick resolution of problems requires gathering as much information as possible about the problem.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference section for Problem Management, Problem Management, IT Service Management]
---

# Data for problem resolution

The quick resolution of problems requires gathering as much information as possible about the problem.

In addition to the information within the problem ticket, useful information is often found in other tables.

## Pertinent related records

Common related records include changes \(through the **Change request** related list\) and incidents in the **Incidents** related list. All the directly related records are accessible through related lists. If the appropriate related list does not appear on the form, the administrator can configure the form to add it.

## Known errors and knowledge articles

Information about already-known issues can be found in two places: the **Known Errors** module in the Problem Management application, or in the Knowledge application. The **Known Errors** module filters the problem table to present all the problems whose cause has been identified but cannot be fixed. The knowledge base can have information that was gathered from incidents, and may also have useful workarounds for problems.

## Dependency Views map

The Dependency Views map provides a visual representation of the configuration items and their relationships and displays information about related issues.

For example, the following image is a map for the CI **nyc rac na200**, which is a mass storage device.

![Dependency views map](../image/ProbBSM1.png "Map for nyc rac nas200 storage device")

The icons beside CIs indicate the following information. You can view information for the selected CI by clicking **Details** in the form header, or by pointing to the icon and viewing a pop-up box.

-   The cloud **x** icon indicates that the CI has an associated problem, which is listed in the **Problem** details pane.
-   The **\(!\)** icon indicates that there is a related incident.
-   The link icon indicates that there are associated tasks, which can be incidents, problems, or changes. If you select the CI, the Details pane displays the associated records.

To open the incident or problem record, click the number in the Details pane.

The map shows the upstream and downstream relationships of the CI. The storage device problem might be an improper change to one of the UNIX servers.

## CMDB baseline history

If a baseline is generated, planned or unplanned changes are tracked within the system. A common cause of problems is improperly executed changes, and reviewing the history of changes to a CI helps track problems caused by improper changes.

To check the CMDB Baseline, view the CI record and check **Baseline Differences** and **Scheduled Changes**. The administrator can use the form designer to add these formatters.

![View baseline differences](../image/problem-baseline.png "Problem baseline")

In the example above, the change in RAM is associated with a change request. You can review the change and see what was planned and what was implemented. The removal of QuickTime software was recorded as an unplanned change.

**Parent Topic:**[Reference section for Problem Management](reference-section-for-problem-management.md)

