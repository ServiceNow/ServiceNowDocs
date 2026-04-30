---
title: Import and map data
description: LDAP import maps match fields in your LDAP database to fields in your instance.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# Import and map data

LDAP import maps match fields in your LDAP database to fields in your instance.

**Note:** LDAP mapping has a performance effect, so the recommended approach is to schedule it during off-peak hours, or process a few records at a time to maintain system availability.

Define a transform map that only imports the needed or required attributes. Depending on the version of the instance you are using, the method for specifying LDAP mapping relationships varies.

The easiest way to know whether or not you are running a version which uses the System LDAP application for LDAP integration is to find the application from the application navigator.

The **Run Business Rules** option is applied only for the target table. Only transform maps associated to the target table run the business rules associated with different tables. If you are updating a user group and have business rules running on a user group table, the group must have roles defined.

|System LDAP application?|Map|
|------------------------|---|
|Yes|Use a transform map to specify your mapping.|
|No|Use a LDAP legacy import map to specify your mapping, or the default LDAP transform that is included in baseline instances. Remember to adjust the **Coalesce** field to match against the correct fields.|

## Scheduled imports

A scheduled import allows administrators to import LDAP data on a regular schedule. By default, the LDAP integration includes two sample scheduled imports:

-   Example LDAP User Import
-   Example LDAP Group Import

Neither example is active by default. Change these scheduled imports to meet your company's business needs.

