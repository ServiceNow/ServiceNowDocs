---
title: Set up work order synchronization in Care Team Operations for Facilities
description: The Field Service Management \[com.snc.work\_management\] plugin is required for work order synchronization to function with Care Team Operations for Facilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/healthcare-life-sciences/cto-facilities-fsm-plugin.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Operations for Facilities, Healthcare Operations, Healthcare and Life Sciences]
---

# Set up work order synchronization in Care Team Operations for Facilities

The Field Service Management \[com.snc.work\_management\] plugin is required for work order synchronization to function with Care Team Operations for Facilities.

For Care Team Operations for Facilities to create work orders from Healthcare Facilities cases, the Field Service Management \[com.snc.work\_management\] plugin must be installed.

This plugin provides all roles and features needed for the healthcare facilities case to synchronize with work orders.

For information on fulfilling work orders, see [Manage work orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/c_ManageWorkOrders.md).

Case and work order states are synchronized according to a predefined state mapping. To change which case state maps to which work order state, see [Modify state decision tables in Care Team Operations for Facilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/healthcare-life-sciences/cto-facilities-modify-state-tables.md).

**If the Field Service Management \[com.snc.work\_management\] plugin isn’t installed:**

Work orders aren't created from healthcare facilities cases. Instead, agents work on fulfilling those cases directly from their portals.

Cases created are assigned to assignment groups based on the requesting location associations and are configured normally with CSM case management functionality.

