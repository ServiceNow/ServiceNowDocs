---
title: Filter REST request and response headers
description: You can add a list of REST request and response headers that are not to be saved in step-result records. You can filter headers that might contain authentication credentials or other sensitive information. The phrase "Header redacted for security" is saved instead.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/automated-test-framework-atf/atf-filter-rest-headers.html
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administering REST test step configurations, Administer, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Filter REST request and response headers

You can add a list of REST request and response headers that are not to be saved in step-result records. You can filter headers that might contain authentication credentials or other sensitive information. The phrase "Header redacted for security" is saved instead.

To specify headers to be filtered, create a system property `glide.atf.rest.log.header_blacklist` with a comma-separated list of header names to be filtered. For information on adding properties, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Parent Topic:**[Administering REST test step configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/automated-test-framework-atf/atf-administer-rest.md)

