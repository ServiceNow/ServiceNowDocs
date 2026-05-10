---
title: Overriding default binding
description: Overriding default binding allows flexibility in linking alerts to CIs beyond the default Node-based matching. This helps customize alert binding based on business needs, ensuring accurate associations and preventing mislinked alerts, improving incident management and root cause analysis.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Overriding default binding

Overriding default binding allows flexibility in linking alerts to CIs beyond the default Node-based matching. This helps customize alert binding based on business needs, ensuring accurate associations and preventing mislinked alerts, improving incident management and root cause analysis.

By default, alerts are bound to CIs by matching the node value in the alert with attributes like Name, FQDN, IP, or MAC Address in the CI. However, if you want to change this behavior—either by using additional criteria or ignoring the node altogether—you can use the **Override Default Binding** check box.

This allows for two scenarios:

1.  When Binding Type = CI Field Matching
    -   If the CI is a host, the Node is required for binding. For more information, see [Bind host CIs using CI field matching](../task/ci-matching-ci-is-host.md).
    -   If the CI is not a host, the Node must be empty. For more information, see [Bind non-host CIs using CI field matching](../task/ci-matching-ci-non-host.md).
2.  When Binding Type = CI Identification. For more information, see [Bind alerts to CIs using CI identification](../task/bind-alerts-CI-app-host-monitoring.md).

This flexibility ensures alerts are linked correctly based on specific business needs.

**Note:** You can also use the Service Operations Workspace to define binding rules. For more information, see [Create Enrich automation](../../service-operations-workspace-itom/task/enrich-alert-sow-itom.md).

