---
title: Application Insights properties
description: These system properties control the behavior of the Application Insights application.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitor, Platform performance, Maintain and monitor, Administer]
---

# Application Insights properties

These system properties control the behavior of the Application Insights application.

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. It is recommended to evaluate the [Overview of Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=zurich&pubname=zurich-impact&ft:locale=en-US) product available with the ServiceNow Impact packages. Work with your Account team to review Impact packages.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Application Insights properties

To change Application Insights properties, navigate to **System Properties** &gt; **All Properties**.

These properties can be used to control the threshold trigger behavior and the p1 prediction model feature.

<table id="table_yfp_ngd_lqb"><thead><tr><th>

Property

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_app\_insights.minutes\_between\_triggers**

</td><td>

integer

</td><td>

How many minutes to wait before sending out a notification for an identical metric trigger.Default: **30**

</td></tr><tr><td>

**sn\_app\_insights.p1\_predict\_factor.semaphores**

</td><td>

integer

</td><td>

The normalizing factor for data for the semaphores metric in the p1 prediction model. Default: **21**

</td></tr><tr><td>

**sn\_app\_insights.p1\_predict\_factor.sys\_load**

</td><td>

integer

</td><td>

The normalizing factor for data for the sys\_load metric in the p1 prediction model. Default: **923**

</td></tr><tr><td>

**sn\_app\_insights.p1\_predict\_max\_cooldown**

</td><td>

string

</td><td>

The number of consecutive "no p1 predicted” minutes required to exit the p1 alert state. Default: **5**

</td></tr><tr><td>

**sn\_app\_insights.p1\_predict\_threshold**

</td><td>

integer

</td><td>

The minimum confidence required for the p1 predict model to predict a p1 alert state. Default: **90**

</td></tr><tr><td>

**sn\_app\_insights.default\_load\_duration\_in\_days**

</td><td>

integer

</td><td>

The default time duration for metric graphs which include overview graphs, individual metric graphs, and drill-down slow pattern graphs.Default: **1**

</td></tr></tbody>
</table>**Parent Topic:**[Application Insights](../concept/application-insights.md)

