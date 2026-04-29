---
title: Disable specific URLs for Connect
description: Prevent users from accessing certain websites by disabling linking to specific Top-Level Domains \(TLDs\).
locale: en-US
release: australia
product: Connect
classification: connect
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect administration, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Disable specific URLs for Connect

Prevent users from accessing certain websites by disabling linking to specific Top-Level Domains \(TLDs\).

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, type `sys_properties.list`.

2.  Search for the **glide.ui.url.external.top\_level\_domains** system property.

3.  In the value field, remove any TLDs that you do not want your users to have access to.

    For example, remove any TLDs that are commonly used for restricted websites, such as `xxx` or `adult`.

    The list of TLDs is based on the [top 200 most common domains](http://research.domaintools.com/statistics/tld-counts/).


## Result

Any TLD not included in the value field becomes unclickable in Connect.

