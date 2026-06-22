---
title: Switch back to Zing search in ITSM Mobile Agent
description: If AI search is already enabled in ITSM Mobile Agent, enable Zing search configuration to use your own search profiles and configurations. It will enable Zing search in ITSM Mobile Agent and all workspaces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/itsm-mobile-agent/switch-zing-itsm-mobile-agent.html
release: zurich
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AI Search in ITSM Mobile Agent, Explore, ITSM Mobile Agent, IT Service Management]
---

# Switch back to Zing search in ITSM Mobile Agent

If AI search is already enabled in ITSM Mobile Agent, enable Zing search configuration to use your own search profiles and configurations. It will enable Zing search in ITSM Mobile Agent and all workspaces.

## Before you begin

Role required: admin

For information about Zing search in mobile, see [Global search for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/mobile/mobile-platform/mobile-search-config.md).

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  Click **New**.

3.  On the System property form, add the following information.

    -   Name: glide.ais.global\_search.use\_zing
    -   Value: true
4.  Click **Submit**.


