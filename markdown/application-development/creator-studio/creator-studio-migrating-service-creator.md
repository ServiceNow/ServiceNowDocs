---
title: Migrating to Creator Studio from Service Creator
description: Creator Studio is replacing the older Service Creator tool, which will be retired in the Australia release.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Migrating to Creator Studio from Service Creator

Creator Studio is replacing the older Service Creator tool, which will be retired in the Australia release.

**Note:** For information on older versions of Service Creator, refer to the previous release documentation.

## Why you should use Creator Studio instead of Service Creator

Creator Studio has a more modern interface than Service Creator. Creator Studio uses Record Producers directly, implements workflows with Playbooks, and allows fulfillment via Workspaces. It also integrates with deployment pipelines to promote applications created with Creator Studio to production environments.

## How to try Creator Studio

If you're currently using Service Creator and want to try Creator Studio, follow these steps:

-   Confirm that your instance is running at least Xanadu patch 3.
-   Purchase an App Engine Enterprise license.
-   Download Creator Studio from the ServiceNow Store. For more information, see [Installing Creator Studio from the ServiceNow Store](installing-creator-studio-from-the-store.md).
-   Activate Creator Studio.

## Playbooks vs. workflows

Creator Studio uses playbooks instead of workflows to automate processes in the apps you build.

[Playbooks](creator-studio-glossary.md#) are a series of steps triggered by an event. You can add multiple playbooks to an app if needed

The steps in a Creator Studio playbook, which include activities and decisions replace the way Service Creator used to define service configurations.

In Service Creator, you had to first create a service category, then define the service and its table. In Creator Studio, the table is automatically created when you make an app, simplifying the category selection process.

For more details, check out [Working with automation in Creator Studio](creator-studio-working-with-automations.md).

