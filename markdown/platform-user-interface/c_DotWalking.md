---
title: Dot-walking to data in related tables
description: Dot-walking provides access to fields on related tables from a form, list, or script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/c\_DotWalking.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Dot-walking to data in related tables

Dot-walking provides access to fields on related tables from a form, list, or script.

If the current table contains a reference to another table, any field on the referenced table can be accessed using dot-walking.

Dot-walking references a field by building a chain of field names separated by dots \(periods\). For instance, **incident.assigned\_to.company** references the company of the user assigned to an incident. The recommended limit for chain length is three levels.

-   **[Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/dot-walking-examples.md)**  
Access fields on a related table from a form, list, or script by dot-walking. This topic includes examples of the different ways that you can dot-walk.

**Parent Topic:**[Common UI elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/p_CommonUIElements.md)

