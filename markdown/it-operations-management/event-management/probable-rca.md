---
title: Probable Root Cause Analysis \(RCA\)
description: Shorten the mean time to repair \(MTTR\) by discovering the root cause of an alert.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Probable Root Cause Analysis \(RCA\)

Shorten the mean time to repair \(MTTR\) by discovering the root cause of an alert.

Probable root cause analysis \(RCA\) provides a list of probable root causes for alerts. This capability uses existing data in IT Service Management to help you determine the root cause of an issue.

RCA takes three factors into consideration: Alerts, configuration item \(CI\) topology, and change requests on the CIs. It extracts CIs from alerts or alert groups and analyzes the CI relationships in the CMDB. It then uses a set of configurable filters to consider relevant change requests on the CIs as possible root causes.

Change requests can be related to a time frame or to a CI, the application service it belongs to, or the software installed on it. For example, a CI must be upgraded or a security patch installed on it. A change request on one CI can affect other CIs.

RCA maps the alerts and change requests to the CIs. It proceeds to calculate the root cause score, a logical score used for sorting probable root causes. The calculation of this score is based on change requests on CIs, and on alerts on a crucial CI called the Topology Origin CI. The root cause score determines how RCA populates the probable root causes list.

![Probable Root Cause list](../image/probable-rca3.png "Probable root cause analysis list")

By default, the list shows the five probable root causes with the highest score. It lists the CIs related to each alert, and the reason RCA identified them as probable root causes.

Scoring for probable root causes is determined by the following criteria, in the indicated order \(lower number = higher priority\):

1.  Change on a CI that originates from topology.
2.  Change on a related CI originates from topology.
3.  Change on a CI.
4.  Change on a related CI/change on an application service/change on software.
5.  Alert on the CI that originates from topology.

To disable the Probable Root Cause Analysis feature, you must create the property **sa\_analytics.disable\_prc** and set the value to `true`. For more information on how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

-   **[Customize RCA settings](../task/set-rca-change-query-filters.md)**  
Modify default settings that determine RCA behavior.

**Parent Topic:**[Manage and monitor alerts](c_EMAlert.md)

