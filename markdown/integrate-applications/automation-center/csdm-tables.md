---
title: Automation Center and CSDM tables
description: Automation Center uses CSDM tables. Several ServiceNow products benefit from and add value to Automation Center.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CSDM guidelines, Configure, Automation Center, Workflow Data Fabric]
---

# Automation Center and CSDM tables

Automation Center uses CSDM tables. Several ServiceNow products benefit from and add value to Automation Center.

## CSDM tables used by Automation Center

-   cmdb\_ci: Stores all automations before they are displayed in the Automation Center dashboard.
-   cmdb\_ci\_automation: Stores automations from cmdb\_ci\_flow\_automation, cmdb\_ci\_base\_rpa\_process, and cmdb\_ci\_rpa\_process.
-   cmdb\_ci\_flow\_automation: Stores flows that are tracked as automations.
-   cmdb\_ci\_base\_rpa\_process: Stores third-party Robotic Process Automation data.
-   cmdb\_ci\_rpa\_process: Stores ServiceNow Robotic Process Automation data.
-   cmdb\_ci\_base\_rpa\_robot: Stores third-party robot data.
-   cmdb\_ci\_rpa\_robot: Stores ServiceNow robot data.

## Products that add value to Automation Center

When you use Automation Center with any of the following ServiceNow products, you increase the value you get from Automation Center:

-   Robotic Process Automation
-   Integration Hub
-   Document Intelligence

**Parent Topic:**[Applying Common Service Data Model guidelines to Automation Center](applying-csdm.md)

