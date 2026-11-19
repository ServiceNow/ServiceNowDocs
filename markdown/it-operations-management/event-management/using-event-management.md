---
title: Configuring Event Management
description: Event Management administrators administer events, manage and monitor alerts, aggregate alerts, and work review and monitor services' status with the Operator Workspace service monitor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/using-event-management.html
release: brazil
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-11-15"
reading_time_minutes: 3
keywords: [AIOps, NOC, Setup Hub, Otto]
breadcrumb: [Event Management, ITOM AIOps, IT Operations Management]
---

# Configuring Event Management

Event Management administrators administer events, manage and monitor alerts, aggregate alerts, and work review and monitor services' status with the Operator Workspace service monitor.

Event Management operators find alerts, analyze them, and take action to resolve the underlying issue.

## Configuration overview for administrators

After you activate Event Management, set it up to receive and process events, and then to generate and analyze alerts. You can use guided setup \(**Guided Setup** &gt; **ITOM Guided Setup**\) or the ITOM configuration console, or complete the tasks manually in the following order:

1.  Configure a [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/r_MIDServerSystemRequirements.md) to receive and process events.
2.  [Configure the MID Web Server extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/configure-mid-web-server-extension.md) so the MID Server can accept pushed events and metric data. You can secure the extension with API key authentication or mTLS.
3.  Configure [Configure Event Management connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/connectors-and-listeners.md) for your monitoring tools, or create a custom connector definition.
4.  Define [event field mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/c_EMEventFieldMapping.md) and [Binding alerts to CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/ci-binding-alert.md) to control how events become alerts and how each alert is tied to its configuration item \(CI\).
5.  Set up [Alert management rules for resolving alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/alert-management-rule.md) and [CI remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/t_SACreateCIRemediation.md) to act on alerts automatically.
6.  [Request Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping/t_ActivateServiceMappingPlugin.md) and run [top-down discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/t_EMGetBaselineServiceMapping.md) to get CI relationships for software and hardware.
7.  Configure [impact calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/c_EMImpactCalculation.md) for services to establish priority for alert resolution.
8.  Configure [alert groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/t_EMCreateAlertGroup.md) to consolidate related alerts and speed up root cause analysis.
9.  Activate the Predictive Intelligence plugin \(com.glide.platform\_ml\) to enable machine learning and find similar alerts.
10. Complete any other general tasks as appropriate, such as domain separation and performance tuning.

**Note:** Event Management does not support creating incidents on remote instances.

