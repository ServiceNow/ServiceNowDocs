---
title: Configure list AI indicators
description: Use a system property to disable AI indicators for lists.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-list-ai-indicators.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Lists, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure list AI indicators

Use a system property to disable AI indicators for lists.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Add a system property named **glide.ai.list\_indicators.enabled**.

    For more information on adding a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

3.  In the Value field, enter `false`.

4.  Select **Update**.


