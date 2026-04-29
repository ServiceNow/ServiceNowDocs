---
title: CI class recommendations
description: CMDB success advisor analyzes your instance's historical data to recommend which CI classes should be in your Data Foundations scope.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI class recommendations

CMDB success advisor analyzes your instance's historical data to recommend which CI classes should be in your Data Foundations scope.

Recommendations help prioritize classes that provide the most operational value. They are based on:

-   Task activity: Frequency of each CI class appearing in incidents, problems, and changes \(IPC\) over a configurable period \(default 180 days, set in the **sn\_cmdb\_advisor.principal\_class\_suggestion\_period** system property\).

    **Note:** If IPC data is unavailable, classes are ranked by how widely they are used across your CMDB. For new instances with no historical data, a set of default classes is suggested.

-   CI population: Number of CI records in each class.
-   Common Service Data Model \(CSDM\) alignment: Support for service mapping and dependency tracking.

**Note:** You aren't required to accept all recommendations. Recommendations are guidance. Your organization's priorities should drive the final advisor scope selection.

