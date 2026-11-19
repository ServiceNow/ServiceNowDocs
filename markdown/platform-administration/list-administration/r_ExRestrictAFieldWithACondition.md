---
title: Condition-based field restriction example
description: This access control prevents most users from editing a critical incident in a list. It is defined by a data condition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/list-administration/r\_ExRestrictAFieldWithACondition.html
release: australia
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2026-11-09"
reading_time_minutes: 1
breadcrumb: [Contextual security, List editor, Administer, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Condition-based field restriction example

This access control prevents most users from editing a critical incident in a list. It is defined by a data condition.

\[Omitted image "RestrictCriticalEvents.png"\] Alt text: This ACL rule sets a condition using the Data Condition builder.

-   **Type:** record
-   **Operation:** list\_edit
-   **Name:** Incident \[incident\]
-   **Decision Type:** Allow If
-   **Data Condition:** \[**Priority**\] \[**is not**\] \[**1 - Critical**\]

