---
title: Tag Governance dashboard – Efficacy tab
description: The Efficacy tab displays the results of tag audits as tag health ratings and compliance coverage of CIs. Interactive widgets show tag coverage status and tagging trends over time.
locale: en-US
release: xanadu
product: Tag Governance
classification: tag-governance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Tag Governance dashboard – Efficacy tab

The Efficacy tab displays the results of tag audits as tag health ratings and compliance coverage of CIs. Interactive widgets show tag coverage status and tagging trends over time.

![Efficacy tab](../image/tag-dashboard-efficacy-tab.png "Efficacy tab")

## Ratings

See the Ratings report to check the quality of CI tag health. The score is based on an algorithm that considers the following information and the data gathered from tag audit runs:

-   Tag policy compliance
-   Overall CI tagging compliance

## Coverage for CIs

The Coverage for CIs report displays the count of CIs in the CMDB that tag policies govern and the percentage of all CIs that are governed. You can use this information to improve coverage of tag policies.

## Ratings and CI Coverage Trends

The **Trends** report displays the average trend value over time of tag governance rating and coverage of CIs. The report provides insights as to how tag quality and tag coverage have fared over time.

## Reports

|Title|Type|Description|
|-----|----|-----------|
|Ratings|Gauge report|Score that indicates the tagging quality rating across CIs. This value is based on an algorithm that uses the number of CIs that the tag policy covers and the total number of CIs that the tag policy certifies.|
|Coverage for CIs|Stacked Bar report|Percentage and count of all CIs that are governed by tag policies versus all CIs in the CMDB. The value is based on the total number of CIs that tag policies govern, divided by the total number of CIs in the CMDB. An individual bar represents each domain's CI coverage data.|
|Trends|Line trend report|Performance trends of tag quality and tag coverage over time.|

