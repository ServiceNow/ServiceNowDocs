---
title: Configure form template semantic search
description: Configure AI-powered semantic search for form templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-form-template-search.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure form template semantic search

Configure AI-powered semantic search for form templates.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Add a system property named **com.glide.ais.semantic\_search**.

    For more information on adding a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

3.  In the Value field, enter `true`.

4.  Select **Submit**.

5.  Add a system property named **glide.template.sematic\_search**.

6.  In the Value field, enter `true`.

7.  Select **Submit**.


