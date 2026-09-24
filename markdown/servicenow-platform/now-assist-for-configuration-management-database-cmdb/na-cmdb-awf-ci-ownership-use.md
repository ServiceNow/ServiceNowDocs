---
title: Determine the owner of a CI
description: Matches unowned CIs against group profiles and proposes ownership. Runs hourly, supports on-demand invocation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.html
release: brazil
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Using agentic workflows, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Determine the owner of a CI

Matches unowned CIs against group profiles and proposes ownership. Runs hourly, supports on-demand invocation.

## Before you begin

Role required: admin

## About this task

Enables you to review ownership assignments by user groups and to request ownership inference for a group of CIs.

-   The feature runs autonomous background jobs that consume assists without direct user action. One hourly inference make up to 1000 LLM call. How we meter this affects packaging and pricing — we need a direction before GA.
-   The prototype scopes to one field and semi-automated review. Everything beyond — the remaining 6 ownership fields, fully- automated mode, change detection, natural-language profiles, and platform-data inference \(ITSM / ITAM\) — sits in the backlog awaiting priority.

## Procedure

1.  Navigate to **All** &gt; **** &gt; ****.

2.  Review recommendations and provide feedback.

    Your feedback in the review step improves accuracy.


**Parent Topic:**[Using agentic workflows in ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md)

