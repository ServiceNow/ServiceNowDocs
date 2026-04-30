---
title: Additional search resources
description: The similar case recommendation feature uses additional search resources, which are configured using the Contextual Search application.The Major Case agent assist recommendations is used for recommending major cases.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Similar case recommendations, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Additional search resources

The similar case recommendation feature uses additional search resources, which are configured using the Contextual Search application.

Navigate to **Contextual Search** &gt; **Additional Resources** to view the Search Resources \(Additional Resources view\) list. Two types of additional search resources are available: Table and Predictive Intelligence Similarity.

## Table resources

Additional search resources of the type **Table** are based on a selected table and have specific conditions that must be met for a record to be included in the search results.

The following **Table** additional search resources are included with the Customer Service plugin:

-   Resolved Cases
-   Open Major Issues

The following **Table** additional search resources are included with the Problem Management Best Practice - Madrid - State Model plugin:

-   Open Problems
-   Resolved Problems

<table id="table_additional_resource_table"><thead><tr><th>

Additional Resource

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resolved Cases

</td><td>

Case

</td><td>

Returns a list of cases created in the last six months that have a state of resolved or closed and the resolution code is one of the following: -   Solved - Fixed by support/Guidance provided
-   Fixed by closing related PRB
-   Workaround provided based on open PRB

 Actions available:

-   **Link to Case**: the current case becomes a child of the case selected from the search results.
-   **Copy Resolution Information**: copies the resolution notes and resolution code from the selected case to the current case.

</td></tr><tr><td>

Open Major Issues

</td><td>

Case

</td><td>

Returns a list of open major cases.Actions available:

 **Link to Case**: the current case becomes a child of the case selected from the search results.

</td></tr><tr><td>

Open Problems

</td><td>

Problem

</td><td>

Returns a list of open problems. Actions available:

 **Link to Case**: adds the selected record as the Problem reference on the current case.

</td></tr><tr><td>

Resolved Problems

</td><td>

Problem

</td><td>

Returns a list of problems that have a state of Resolved or Closed. Actions available:

 **Link to Case**: adds the selected record as the Problem reference on the current case.

</td></tr></tbody>
</table>## Predictive Intelligence Similarity resources

Additional search resources of the type Predictive Intelligence Similarity are associated with a Machine Learning \(ML\) similarity solution definition. Search resources of this type require the Predictive Intelligence plugin \(com.glide.platform\_ml\). The resources listed in the following table are included with the Predictive Intelligence plugin.

In addition to the associated similarity solution definition, Predictive Intelligence Similarity resources can have configured properties. These properties identify conditions that must be met for cases to be included in the search results.

<table id="table_usd_p4d_cgb"><thead><tr><th>

Additional Resource

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommended Resolved Cases

</td><td>

Case

</td><td>

Returns a list of resolved similar cases created in the last six months.Associated with the Recommended Resolved Cases similarity solution definition.

</td></tr><tr><td>

Recommended Open Cases

</td><td>

Case

</td><td>

Returns a list of open similar cases created in the last six months.Associated with the Recommended Open Cases similarity solution definition.

</td></tr><tr><td>

All Similar Cases

</td><td>

Case

</td><td>

Returns a list of all similar cases created in the last six months.Associated with the All Similar Cases similarity solution definition.

</td></tr></tbody>
</table>## Major case agent assist recommendations

The Major Case agent assist recommendations is used for recommending major cases.

The agent assist provides a recommendation for each of the two major case scenarios:

-   Major case found: returns a list with one or more major cases created in the time-frame indicated in the solution definition that are similar to the current case. Cases are listed by similarity score. The default time-frame is set to the start of yesterday.
-   No major case found: returns a recommendation based on the number of cases created in the time-frame indicated in the solution definition that are similar to the current case \(does not include any major cases\). The default time-frame is set to the start of yesterday.

To configure the time-frame for the solution definition threshold, see [Update your similarity score threshold](https://www.servicenow.com/docs/access?context=update-similarity-threshold&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

If the Major Case agent assist recommendations find one or more major cases similar to the current case, the Predictive Intelligence tab displays these cases ranked by similarity score. The case with the highest score is highlighted with a white box and the title **Major Case** and includes a user action to link the current case to the major case.

![Agent Assist window in the Predictive Intelligence tab displaying a recommendation to link the current case to a major case.](../image/csm-agent-intelligence-tab-major-case.png "Predictive Intelligence major case recommendation")

If the Major Case agent assist recommendations find cases similar to the current case, but no major cases, the Predictive Intelligence tab displays a recommendation highlighted with a blue box. It includes the option to propose the current case as a major case candidate.

![Agent Assist window in the Predictive Intelligence tab displaying a recommendation to propose the current case as a major case.](../image/csm-agent-intelligence-tab-recommendation.png "Predictive Intelligence tab similar case recommendation")

The Major Case agent assist recommendations:

-   Uses the Major Case agent assist recommendations ML solution definition.
-   Includes some properties that provide customers with customization options, such as the recommendation title and message that appears in the Predictive Intelligence tab.
-   Includes the **Potential Major Case** trend definition.

    This definition sets the threshold for:

    -   Finding the number of distinct accounts that cases need to belong to for a major issue recommendation. The default value is 3.
    -   The number of similar cases that need to be returned by the solution definition for a major issue recommendation using a script. The default value is 10.

