---
title: Relationships between configuration records
description: The Application File Types table defines parent-child relationships between configuration records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application files, Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Relationships between configuration records

The Application File Types table defines parent-child relationships between configuration records.

The system uses this structure to keep configuration records that normally belong together in the same application.

**Note:** Do not modify the Application File Types table as it provides system functionality.

For example, consider the parent-child relationships for a UI policy.

-   The UI policy is a child of the application table.
-   UI policy actions are children of the UI policy.
-   UI policy actions have a parent UI policy and a grandparent application table.
-   The UI policy actions and the UI policy are all descendants of the application table.

![Relationships in a sample configuration record](../image/SampleConfigurationRecordRelationships.png "Sample configuration record relationships")

