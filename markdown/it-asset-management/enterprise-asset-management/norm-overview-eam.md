---
title: Normalization overview for Enterprise Asset Management
description: Use the Normalization view in the Enterprise Asset Workspace to view information related to normalization such as normalization status, model content service download, lifecycle overview.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Enterprise Asset Workspace, Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Normalization overview for Enterprise Asset Management

Use the Normalization view in the Enterprise Asset Workspace to view information related to normalization such as normalization status, model content service download, lifecycle overview.

You can also create custom enterprise model types, product models, and model libraries from this view.

You can access the Normalization view by navigating to **Enterprise Asset Workspace** &gt; **Normalization**.

![Enterprise model normalization](../image/eam-normoverview.png "Enterprise model normalization")

<table id="table_nvt_3qb_vtb"><thead><tr><th>

Widget

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise models up for end of life

</td><td>

Enterprise Model Lifecycle \[sn\_eam\_model\_lifecycle\]

</td><td>

The beginning phase of the end of life for enterprise models. Shows the count of enterprise models whose start date of the end of life phase is either the current month, quarter, or year.

**Note:** Only enterprise model life cycle records that are active, model status is in production, and life cycle type is Publisher appear in **This month**, **This quarter**, or **This year**

</td></tr><tr><td>

Normalization status

</td><td>

 

</td><td>

Normalization status of all the enterprise models. View the count of enterprise models that were normalized and those models that didn't get normalized. For details on the normalization status, see [Normalization status for enterprise models](../reference/norm-status-eam.md).

</td></tr><tr><td>

Lifecycle overview

</td><td>

Enterprise Model Lifecycle \[sn\_eam\_model\_lifecycle\]

</td><td>

The count of enterprise models that are present in each life cycle stage: General availability, end of support, end of extended support, and end of sale.**Note:** Only enterprise model life cycle records that are active appear in this widget.

</td></tr><tr><td>

Enterprise model content service download.-   Days until next content download
-   Days since last content download

</td><td>

Data Services Download Schedules \[cds\_client\_schedule\]

</td><td>

The days since the content service library was last downloaded on your instance and the days remaining for the next download to take place.

</td></tr></tbody>
</table>