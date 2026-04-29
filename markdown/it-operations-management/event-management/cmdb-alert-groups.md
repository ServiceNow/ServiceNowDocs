---
title: CMDB based alert grouping
description: CMDB based alert grouping helps organizations manage alerts by organizing them according to their related configuration items \(CIs\) within the Configuration Management Database \(CMDB\). This method group alerts based on CI relations in applications or infrastructure components, allowing teams to better understand the impact of issues, respond more effectively to alerts, and maintain service availability.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mixed alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# CMDB based alert grouping

CMDB based alert grouping helps organizations manage alerts by organizing them according to their related configuration items \(CIs\) within the Configuration Management Database \(CMDB\). This method group alerts based on CI relations in applications or infrastructure components, allowing teams to better understand the impact of issues, respond more effectively to alerts, and maintain service availability.

CMDB alert groups are created based on the current relationships between CIs in an organization. This means that when several alerts are triggered on different CIs—for example, if a server is experiencing issues — alerts are grouped based on CI relationships.

By default, all the existing connections between CIs are used to group alerts. However, given the complexity of IT systems, there are many types of relationships, and organizations can filter which ones to consider when aggregating alerts. For instance, you can filter relationship types by suggested relationships that appears in the CMDB Group CI Relations \[em\_suggested\_relation\_type\] table. You can also filter using the hosting and containment rules \(dependent relationship rules\).

For example, if a server is hosting multiple applications, and there’s a problem with that server, all the alerts related to both the server and the applications it hosts can be grouped together. This helps the IT team quickly identify and address the root cause of the issue rather than dealing with each alert in isolation. Similarly, if different processes are running on a server, grouping alerts based on those processes allows teams to see how problems in one area might affect others, leading to a more comprehensive understanding of the situation.

The CMDB alert groups are effectively displayed in the [Express List](../../service-operations-workspace-itom/concept/el-cmdb-based-link-view.md) within the Service Operations Workspace, which allows teams to easily monitor and manage related alerts. This feature enhances operational efficiency by providing a clear view of alerts that are interconnected based on the current relationships among configuration items \(CIs\).

