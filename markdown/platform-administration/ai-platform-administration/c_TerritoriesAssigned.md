---
title: Territories assigned
description: Territories are assigned to locations, and are not assigned directly to users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/c\_TerritoriesAssigned.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Phone number field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Territories assigned

Territories are assigned to locations, and are not assigned directly to users.

A user's territory, and so the user's E.164-compliant phone functionality, is based on the user's location. For example, if a user has a location of **SHS quadra 5, Bloco E., Brasilia** defined in the User \[sys\_user\] table, the parent record for Brazil in the location table defines the phone territory. The phone territory may be assigned at any level of the [Map pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/c_MapPages.md) hierarchy, which is searched going up to the next parent until the territory is found or no parents remain.

