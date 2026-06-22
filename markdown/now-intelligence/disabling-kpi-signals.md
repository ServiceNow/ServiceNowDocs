---
title: Disabling KPI Signals
description: KPI Signals can be disabled on request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/disabling-kpi-signals.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, KPI Signals, Platform Analytics experience, Platform Analytics]
---

# Disabling KPI Signals

KPI Signals can be disabled on request.

KPI Signals is activated by default. If you do not want this feature, request a ServiceNow AI Platform administrator to set the property **com.snc.pa.activate\_kpi\_signals** to **false**. Because this property does not exist by default, the administrator must add it. You can refer them to [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Important:** If you reactivate KPI Signals, signal detection resumes from the time you originally deactivated the feature, not from the time you reactivated it.

**Parent Topic:**[Configuring KPI Signals for an indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configuring-kpi-signals.md)

