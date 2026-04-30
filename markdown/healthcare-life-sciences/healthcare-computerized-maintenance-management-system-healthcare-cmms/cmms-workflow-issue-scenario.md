---
title: Healthcare Computerized Maintenance Management System - Reporting medical device issue scenario
description: Use the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application for reporting medical device issues and performing corrective maintenance.
locale: en-US
release: zurich
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Healthcare Computerized Maintenance Management System, Clinical Device Management, Healthcare and Life Sciences]
---

# Healthcare Computerized Maintenance Management System - Reporting medical device issue scenario

Use the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application for reporting medical device issues and performing corrective maintenance.

**Important:** Healthcare Computerized Maintenance Management System is now deprecated and no longer supported or available for new activation. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

Scenario: An issue is identified with a medical device in a hospital and a corrective maintenance needs to be performed. A organization contributor for medical devices submits the medical device issue form from the customer service portal of the hospital. In the issue form, the contributor enters the requester organization, medical device, its model, and other issue details. When a medical device issue case is created in the ServiceNow instance, a clinical engineer who acts as a fulfiller with the sn\_hcls\_cmms.clinical\_engineer role can work on the case.

1.  Uses the Workspace to view the medical device issue case.
2.  In Workspace, views the complete information about the medical device, its model, and issue details from the **Details** tab.
3.  Creates a work order to resolve the issue.
4.  When the work order is set to complete, closes the medical device issue case.

