---
title: Activate the Service Mapping Candidate skill
description: The Service Mapping Candidate skill provides Now Assist the ability to classify app service candidates and generate a description for them. The skill is active by default. If needed, administrators can activate or deactivate the skill.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Generate description, Find processes, Classify application service candidates, Now Assist skill, Now Assist, Gen AI, generative AI, ITOM, IT Operations management]
breadcrumb: [Activate Now Assist skills in Now Assist for IT Operations Management \(ITOM\), Configure, Now Assist for ITOM, IT Operations Management]
---

# Activate the Service Mapping Candidate skill

The Service Mapping Candidate skill provides Now Assist the ability to classify app service candidates and generate a description for them. The skill is active by default. If needed, administrators can activate or deactivate the skill.

## About this task

The Service Mapping agentic workflow, Analyze potential impact, uses two Now Assist skills:

-   Service Mapping Candidate
-   Service Mapping Candidates Impact

The Service Mapping Candidate skill provides names for processes and application service candidates. The skill gets details about the processes within the application service candidate, such as publisher, product, and description. Then, it gets details about the application service candidate, such as name, and description.

## Before you begin

Before activating the Now Assist skills, you must install the Now Assist for IT Operations Management \(ITOM\) plugin. For more information, see [Install Now Assist for IT Operations Management](../../now-assist-setup-itom/task/install-now-assist-itom.md).

You must configure the following settings:

-   ITOM pro plus SKU
-   Now Assist for ITOM 9.10
-   Service Mapping Plus \(minimum version 1.16.3\)
-   Now Assist for IT Service Management \(ITSM\)
-   Now Assist for Platform \(minimum version 9.1.0\)

**Important:** This Now Assist skill is now turned on by default. The skill will be automatically available to appropriate role users for the application. This change simply activates the skill and does not touch the roles that are needed to use the skill. The new default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills will turn on automatically.

-   **Existing customers who are upgrading**

    Any previously unconfigured skill will turn on automatically \(the skill was never turned on, then off again\).

    There is no change to Now Assist skills that are currently enabled and customized.

    Previously configured skills that were turned on, then off, will remain inactive.


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  On the navigation panel, select **ITOM**.

3.  On the Service Mapping Candidate tile, select **Activate**.


**Parent Topic:**[Activate Now Assist skills in Now Assist for IT Operations Management \(ITOM\)](activate-now-assist-skills-itom.md)

