---
title: Ranking records with Spotlight
description: Use Spotlight to identify and rank records of interest based on multiple weighted criteria.
locale: en-US
release: australia
product: Spotlight
classification: spotlight
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Ranking records with Spotlight

Use Spotlight to identify and rank records of interest based on multiple weighted criteria.

Spotlight illuminates records that otherwise you might overlook. You can define weighted criteria to identify and rank records that require attention, such as when triaging incidents or performing lead scoring. You can rank records based on multiple dimensions, instead of by a single field value such as priority. While most organizations address high-priority items in a timely manner, lower priority items sometimes are not addressed for an extended period of time. Spotlight helps you focus on items based on business need.

For example, you might want to have incidents brought to your attention if they have been open for a long time, or been reassigned multiple times, even if these incidents are low priority. Among those incidents, you might want one that has been open a long time and been assigned multiple times to be ranked above one that has only been open a long time.

Spotlight uses scheduled jobs that run to evaluate the records. The results of these jobs can be viewed in Spotlight interactive analyses. To share Spotlight results, share the URL of the analysis with any user who has the pa\_spotlight\_viewer role.

The following diagram demonstrates scoring in Spotlight. The large circle represents the set of all open incidents. Each of the smaller circles represents a weighted Spotlight criteria that applies to a subset of the open incidents.

![Colored circles representing Spotlight criteria](../image/Spotlight-diagram.png "Spotlight diagram")

**Note:** To use Spotlight, an administrator must activate the Spotlight plugin.

-   **[Setting up Spotlight](setting-up-spotlight.md)**  
Set up Spotlight for each set of table records that you want to evaluate and rank by importance. The records must be associated with an indicator.
-   **[See Spotlight score details](../task/view-details-of-a-spotlight.md)**  
To see the criteria whose weights contributed to a Spotlight score, view the details of the Spotlight record.
-   **[Spotlight interactive analysis](spotlight-interactive-analysis.md)**  
Spotlight interactive analysis shows the key results of a Spotlight job. Access the analysis from a Spotlight Group record.
-   **[Spotlights on Platform Analytics dashboards](spotlights-configurable-workspaces.md)**  
You can list Spotlights and show them in a dashboard on a configurable workspace.
-   **[Spotlight job logs](spotlight-logs.md)**  
The steps of Spotlight jobs are recorded in logs. Use these logs to debug any issues.
-   **[Domain separation with Spotlight](domain-separation-spotlight.md)**  
If you have domain separation enabled, Spotlight applies it during Spotlight jobs.
-   **[Copy a Spotlight group to domains](../task/copy-spotlight-group-domain.md)**  
You can copy a Spotlight group to other domains, saving the effort of reproducing the group manually for each domain.
-   **[Copy a Spotlight group to breakdown elements](../task/copy-spotlight-group-element.md)**  
You can copy a Spotlight group across multiple elements of a single breakdown.
-   **[Spotlight group copy logs](spotlight-copy-logs.md#)**  
When a Spotlight group is copied, the steps of the copying process are recorded in logs. Use these logs to debug any issues.
-   **[Administering Spotlight](administering-spotlight.md)**  
Users with the admin role can access lower-level components of Spotlight.

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

