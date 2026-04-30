---
title: Filter REST request and response headers
description: You can add a list of REST request and response headers that are not to be saved in step-result records. You can filter headers that might contain authentication credentials or other sensitive information. The phrase "Header redacted for security" is saved instead.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering REST test step configurations, Administering the Automated Test Framework \(ATF\), Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Filter REST request and response headers

You can add a list of REST request and response headers that are not to be saved in step-result records. You can filter headers that might contain authentication credentials or other sensitive information. The phrase "Header redacted for security" is saved instead.

To specify headers to be filtered, create a system property `glide.atf.rest.log.header_blacklist` with a comma-separated list of header names to be filtered. For information on adding properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Administering REST test step configurations](atf-administer-rest.md)

