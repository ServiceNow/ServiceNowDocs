---
title: Migrating to Creator Studio from Service Creator
description: Creator Studio is intended to replace the legacy Service Creator offering, which will be retired in the Australia release.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2024-10-03"
reading_time_minutes: 1
breadcrumb: [Exploring Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Migrating to Creator Studio from Service Creator

Creator Studio is intended to replace the legacy Service Creator offering, which will be retired in the Australia release.

**Note:** You can find content for old versions of Service Creator in previous release documentation.

## Why you should use Creator Studio instead of Service Creator

Creator Studio has a more modern interface than Service Creator. Creator Studio uses Record Producers directly, implements workflows with Playbooks, and allows fulfillment via Workspaces. It also integrates with deployment pipelines to promote applications created with Creator Studio to production environments.

## Process for trying out Creator Studio

If you're a Service Creator user ready to check out Creator Studio, you must do the following:

-   Confirm that your instance is on a minimum version of Xanadu patch 3.
-   Purchase an App Engine Enterprise license.
-   Download Creator Studio from the ServiceNow Store. For more information, see [Installing Creator Studio from the ServiceNow Store](installing-creator-studio-from-the-store.md).
-   Activate Creator Studio.

## Playbooks vs. workflows

Unlike the workflows that Service Creator used, Creator Studio uses playbooks to automate processes in the apps you build.

[Playbooks](creator-studio-glossary.md#) are a set of activities that occur in order based on a trigger. Each activity is more like a step in a chain of steps. You can add multiple playbooks to an app if you need to.

Playbook activities in Creator Studio replace the process of defining service configurations in Service Creator.

In Service Creator, you had to first create a category for services, and then create the service and its table. Creator Studio automatically creates the table for you when you create an app, and streamlines the category selection process.

For more information, see [Working with automation in Creator Studio](creator-studio-working-with-automations.md).

