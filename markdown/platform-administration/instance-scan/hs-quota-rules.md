---
title: Timeout threshold
description: A timeout determines the execution threshold of a scan from running long scans. For example, any scan running longer than the set time period results in a failure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/instance-scan/hs-quota-rules.html
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Instance Scan, Maintain and monitor, Administer]
---

# Timeout threshold

A timeout determines the execution threshold of a scan from running long scans. For example, any scan running longer than the set time period results in a failure.

If the scan or the check takes longer than the set time period set by the quota rule, an error message appears.

**Note:** By default the scans are limited to three hours and individual checks are limited to 10 minutes.

\[Omitted image "hs-quota-rule-error.png"\] Alt text: Error message: The scan exceeded the time allowed.

To learn how to configure these thresholds, see [Implement a scan timeout threshold](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/instance-scan/hs-full-scan-quota-rule.md) and [Implement a check timeout threshold](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/instance-scan/hs-health-check-quota-rule.md).

