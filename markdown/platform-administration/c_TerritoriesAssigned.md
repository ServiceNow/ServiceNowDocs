---
title: Territories assigned
description: Territories are assigned to locations, and are not assigned directly to users.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Phone number field type, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Territories assigned

Territories are assigned to locations, and are not assigned directly to users.

A user's territory, and so the user's E.164-compliant phone functionality, is based on the user's location. For example, if a user has a location of **SHS quadra 5, Bloco E., Brasilia** defined in the User \[sys\_user\] table, the parent record for Brazil in the location table defines the phone territory. The phone territory may be assigned at any level of the [Map pages](https://www.servicenow.com/docs/access?context=c_MapPages&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) hierarchy, which is searched going up to the next parent until the territory is found or no parents remain.

**Parent Topic:**[Phone number field type](c_UsePhoneNumberFields.md)

