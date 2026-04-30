---
title: Components installed with Application Insights
description: Several types of components are installed with the installation of the Application Insights application, including tables and user roles.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install Application Insights, Application Insights, Monitor, Platform performance, Maintain and monitor, Administer]
---

# Components installed with Application Insights

Several types of components are installed with the installation of the Application Insights application, including tables and user roles.

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. It is recommended to evaluate the [Overview of Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=zurich&pubname=zurich-impact&ft:locale=en-US) product available with the ServiceNow Impact packages. Work with your Account team to review Impact packages.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](../../plugins/task/find-components.md).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Application Insights administrator \[sn\_app\_insights.admin\]

</td><td>

Users of the Application Insights application cannot:

-   Apply filters on graphs for events or transactions.
-   View syslog\_transaction and sysauto records.
-   Create alerts.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application Insights Aggregates \[sn\_app\_insights\_aggregates\]

</td><td>

Temporarily stores aggregates for average, median, and 95th percentile of various statistics such as events processed and transactions.

</td></tr><tr><td>

Application Insights ECC Queue Aggregates\[sn\_app\_insights\_ecc\_queue\]

</td><td>

Temporarily stores ECC queue aggregates for average, median, and 95th percentile of various ECC-related statistics such as inbound and outbound processing.

</td></tr><tr><td>

Metric Trigger \[sn\_app\_insights\_metric\_trigger\]

</td><td>

Log of triggered metric threshold events.

</td></tr><tr><td>

Metric trigger log\[sn\_app\_insights\_metric\_trigger\_log\]

</td><td>

Log of metric trigger events.

</td></tr><tr><td>

P1 Predict\[sn\_app\_insights\_p1\_predict\]

</td><td>

Stores the prediction model values to determine if a system is about to experience a P1 event.

</td></tr><tr><td>

Slow Patterns To Scripts Mapping\[sn\_app\_insights\_slow\_patterns\_to\_scripts\_mapping\]

</td><td>

Stores mapping of slow patterns to scripts.

</td></tr><tr><td>

Script Referenced Slow Pattern \[sn\_app\_insights\_st\_slow\_pattern\_referenced\_script\]

</td><td>

Temporarily holds the count of scripts referenced from the source of a slow pattern.

</td></tr><tr><td>

Slow patterns metrics\[sn\_app\_insights\_st\_slow\_patterns\]

</td><td>

Temporarily stores metrics of slow patterns such as execution counts and times.

</td></tr><tr><td>

Slow Patterns To Scripts Mapping ST \[sn\_app\_insights\_st\_slow\_patterns\_to\_scripts\_mapping\]

</td><td>

Temporarily stores additional calculated relationship mapping of slow patterns to scripts with execution count and time.

</td></tr><tr><td>

Scheduled Jobs \[sn\_app\_insights\_st\_sysauto\]

</td><td>

Temporarily stores metrics of scheduled jobs including processing duration, error, and run counts.

</td></tr><tr><td>

Conditional threshold \[sn\_app\_insights\_trigger\_condition\]

</td><td>

Stores the configuration of metric thresholds, which are a logical combination of the individual triggers in the sn\_app\_insights\_metric\_trigger table.

</td></tr></tbody>
</table>**Parent Topic:**[Install Application Insights](../task/install-application-insights.md)

