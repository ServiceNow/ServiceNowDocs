---
title: Namespace identifier
description: The system adds a namespace identifier to the front of application artifacts such as tables, scripts, and configuration records.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Application scope, Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Namespace identifier

The system adds a namespace identifier to the front of application artifacts such as tables, scripts, and configuration records.

The identifier cannot be changed or removed from application artifacts to ensure that they are always associated to the proper application and that they have a unique name.

The system generates a namespace identifier from the following information:

|Element|Requirements|Sample Value|
|-------|------------|------------|
|The prefix characters for a scoped application.|Scoped applications always start with an x\_ prefix.|x\_|
|The instance customer prefix \(glide.appcreator.company.code\)|This string is two to five characters long. ServiceNow generates this prefix for each customer. The instance stores the prefix in the **glide.appcreator.company.code** system property.|acme|
|The application ID|This string can be up to 40 characters long. If the string is longer than 18 characters, the system truncates the application name and appends it to prefix `x_<glide.appcreator.company.code>_`. Application developers set this ID when they create the application. The system uses the application name by default.|book\_rooms|

The example values generate a namespace identifier of x\_acme\_book\_rooms.

