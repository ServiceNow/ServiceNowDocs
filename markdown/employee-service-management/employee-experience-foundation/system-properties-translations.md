---
title: Enable translated topic path updates
description: Improve the accuracy and reliability of topic translations with a new system property that helps keep translated topic paths up to date automatically.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
keywords: [translation, localization, topic paths, multilingual]
breadcrumb: [Create and associate topics, Unified Taxonomy for Employee Center, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Enable translated topic path updates

Improve the accuracy and reliability of topic translations with a new system property that helps keep translated topic paths up to date automatically.

## Before you begin

Role required: admin

## About this task

This new system property helps keep translated topic paths up-to-date automatically and enable access to the latest localized content or multilingual topic structures.

-   Ensure that topic paths and topic names changes are reflected in other languages.
-   Capture the last run time of the **Generate topic path translations** job.
-   Track translations for localized Employee Center experiences.
-   Improve reliability of the translated content during updates or content restructuring.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Search for the translated topic path tracking property `taxonomy.topic_path_translations_job_last_run` and open.

3.  Set the property value to **true**.


## Result

The system property tracks translation of topic names and path updates automatically. Employees can access localized or region-specific content with the latest topic labels and navigation paths.

