---
title: Health windows
description: A health window is a trailing time frame in which the ServiceNow system evaluates audit results from CIs that have desired state fields defined.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certification audits, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Health windows

A health window is a trailing time frame in which the ServiceNow system evaluates audit results from CIs that have desired state fields defined.

The **Health window** and **Health unit** fields define each window, and ends when an audit runs. For example, an audit runs on the fifteenth of the month with a seven-day window. It evaluates the threshold values of a desired state field from the eighth to the fifteenth. When the same audit runs the next day, the system evaluates the threshold from the ninth to the 16th, and so on. The audit counts backward seven days from the current day. ServiceNow evaluates a CI threshold value for each health window, without considering the results from the previous window. As a result, the health of a CI can fail for one audit and then pass in a subsequent audit that runs in a new window.

ServiceNow evaluates stability by recording the number of times a desired state threshold value for a CI switch between **Failed** and **Certified** within the health window. In the example shown here, a 5-minute health window was set for the desired state field on a UPS unit that measures the remaining battery time. The threshold was set at 2, which allows the field to fail two audits in the same health window.

In the initial audit, the system evaluated the threshold value for the **Seconds on battery** field within a 5-minute window. This window ran from 13:52:51 to the time of the audit at 13:57:51. The desired state field showed In Limit for that audit and the second audit conducted less than a minute later. The next two audits were conducted within five minutes of the first audit and both showed that the threshold \(set at 2\) was Exceeded. A subsequent audit was conducted five minutes after the audit in which the desired state field threshold was first exceeded. Since the health window had moved forward enough units, the **Seconds on battery** field was within limits again with only one failure in the 5-minute window being evaluated.

