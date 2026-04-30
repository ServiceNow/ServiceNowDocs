---
title: Select option for Recommended Actions application
description: There are two options for the Recommended Actions application: String-based and ML-based. These options decide the kind of data that you get for your search. It displays data about automations in all states except the Published state.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Recommended Actions with Automation Center, Configure, Automation Center, Workflow Data Fabric]
---

# Select option for Recommended Actions application

There are two options for the Recommended Actions application: String-based and ML-based. These options decide the kind of data that you get for your search. It displays data about automations in all states except the **Published** state.

## Before you begin

Install the Recommended Actions application. For more information, see [Install Recommended Actions application](install-ra.md).

Recommended Actions searches for matching string in **Process name**, **Description**, and **Applications used** fields of the Automation requests form, and **Automation name**, **Description**, and **Source** in the Automation Attribute table.

-   String-based: Searches for the exact string in the same order as in the search criteria.

    This is a good option if you want to use short phrases or single words as your search criteria. By default, this option is enabled.

-   ML-based: This is helpful if you have too much data and your search criteria is long. To use the ML-based recommendations, you need at least 10 records in Automation Center.

Role required: sn\_ac.automation\_technical\_user and sn\_nb\_action.next\_best\_action\_author

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Recommendations**.

2.  Mark the **Active** flag to **true** for the required options.

    **Note:** To identify the options, check the names. The names that have **ML** appended at the end are for ML-based recommendations.

3.  If you have chosen ML-based option, then perform the following steps:

    1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution** &gt; **Definition**.

    2.  Open **Automation request process name similarity** and **Automation attribute automation name** separately.

    3.  Select **Update &amp; Retrain** for each one of them.

    After selecting **Update &amp; Retrain**, the training will start in the scheduler. After it’s complete, it displays **Solution complete**.


**Parent Topic:**[Configuring the Recommended Actions application with Automation Center](../concept/config-ra.md)

