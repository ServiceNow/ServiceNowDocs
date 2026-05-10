---
title: Fulfilling service requests in Care Team Operations for Biomed
description: Healthcare Biomed cases can be fulfilled one of two ways, depending on what plugin you have installed.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Fulfilling service requests in Care Team Operations for Biomed

Healthcare Biomed cases can be fulfilled one of two ways, depending on what plugin you have installed.

For Care Team Operations for Biomed to create work orders from Healthcare Biomed cases, the Field Service Management \[com.snc.work\_management\] plugin must be installed.

This plugin provides all roles and features needed for the healthcare biomed case to synchronize to work orders.

It also provides the following roles for Care Team Operations for Biomed:

-   biomed.dispatcher
-   biomed.agent
-   biomed.qualifier

For information on fulfilling work orders, see [Manage work orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/c_ManageWorkOrders.md).

**If the Field Service Management \[com.snc.work\_management\] plugin isn’t installed:**

Work orders aren’t created from healthcare biomed cases. Instead, agents work on fulfilling those cases directly from Workspace.

Cases created are assigned to assignment groups based on the requesting location associations and are configured normally.

For information on fulfilling cases, see [Manage cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/manage-cases.md) in Customer Service Management.

