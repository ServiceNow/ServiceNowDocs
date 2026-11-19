---
title: Condition-based field restriction example
description: This access control prevents everyone from editing a critical incident in a list. It is defined by a condition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/list-administration/r\_ExRestrictAFieldWithACondition.html
release: brazil
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Contextual security, List editor, Administer, List administration, Forms, fields, and lists, Configure core features, ServiceNow AI Platform]
---

# Condition-based field restriction example

This access control prevents everyone from editing a critical incident in a list. It is defined by a condition.

\[Omitted image "RestrictCriticalEvents.png"\] Alt text:

-   **Type:** record
-   **Operation:** list\_edit
-   **Name:** Incident \[incident\]
-   **Admin overrides:** Clear the check box.
-   **Condition:** \[**Priority**\] \[**is not**\] \[**1 - Critical**\]

