---
title: Loom v3.9 release notes
description: This release version includes minor bug fixes and improvements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-loom-3-9.html
release: other
topic_type: reference
last_updated: "2021-02-03"
reading_time_minutes: 1
breadcrumb: [OOB Other release notes]
---

# Loom v3.9 release notes

This release version includes minor bug fixes and improvements.

## Fixed problems

|Problem category|Problem|Short description|Description|
|----------------|-------|-----------------|-----------|
|Loom Predictive Intelligence|PRB1458817|ES DataInput does not support timestamp formats \(with different millisecond counts\)|When an ES DataInput has timestamp format configured with 9'S' \(9 miliseconds values in the format\), documents with 5 milliseconds fail to be processed.|
|Loom Predictive Intelligence|PRB1412137|Custom alerts do not work| |
|Loom Predictive Intelligence|PRB1417857|Data discrepancy - the email title is containing the service names same as application name| |
|Loom Predictive Intelligence|PRB1457736|AlertsCreator: failed patternized|Post 3.8 upgrade, the following error appeared in the BE "AlertsCreator: failed patternized"|
|Loom Predictive Intelligence|PRB1457209|Dashboards are not populating data| |

**Parent Topic:**[OOB Other release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/sn-oob-rn.md)

