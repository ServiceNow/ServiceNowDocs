---
title: Migrate from CAPI to Patterns
description: Migrate from Cloud API \(CAPI\)-based Cloud Discovery to Patterns-based Cloud Discovery. The task requires supported instance and few plugins. Migration works for Amazon Web Services \(AWS\) and Microsoft Azure. Administrator can perform this task after the initial instance is set up.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Discovery setup, Discovery, ITOM Visibility, IT Operations Management]
---

# Migrate from CAPI to Patterns

Migrate from Cloud API \(CAPI\)-based Cloud Discovery to Patterns-based Cloud Discovery. The task requires supported instance and few plugins. Migration works for Amazon Web Services \(AWS\) and Microsoft Azure. Administrator can perform this task after the initial instance is set up.

## Before you begin

Ensure that your ServiceNow AI Platform has the following:

-   The release version is Paris or later.
-   The Discovery and Service Mapping Patterns \(sn\_itom\_pattern\) plugin.

Role required: discovery\_admin

## About this task

When the migration is triggered, the script disables the appropriate CAPI discovery steps for the cloud environment to prevent them being triggered during cloud discovery. Also, the script enables the appropriate cloud patterns for the environment that is used to run future cloud discovery. After the migration, discovery uses the latest patterns instead of the legacy discovery method, CAPI.

**Note:**

The CAPI-based discovery method is going to be deprecated in the future.

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Migrate CPG to Pattern**.

2.  On the CAPI to Pattern Migration page, read the instructions and select **Run Prerequisites Check**.

3.  After the Prerequisite scan is passed, you can either choose as follows:

    -   Migrate All—Migrate both AWS and Azure together.
    -   Migrate AWS or Migrate Azure—Migrate each instance one at a time.
4.  Select Migrate and confirm to proceed migration.

    **Note:**

    For any issues while migrating, see the troubleshooting steps documented in the [CAPI to Pattern Migration: Procedure for switching from CAPI-based Cloud Discovery to pattern-based Cloud Discovery \[KB0827153\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0827153) article in the Now Support Knowledge Base.


