---
title: Phase 4 - Upgrade and validate the development instance
description: Track the progress of your upgrades with the Upgrade Monitor. For your first non-production instance upgrade \(your development instance\), use the Upgrade Monitor to process the skipped list of records that were not addressed in the upgrade. Then identify your update sets and perform functional testing.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Upgrade to the Australia release, Australia release notes]
---

# Phase 4 - Upgrade and validate the development instance

Track the progress of your upgrades with the Upgrade Monitor. For your first non-production instance upgrade \(your development instance\), use the Upgrade Monitor to process the skipped list of records that were not addressed in the upgrade. Then identify your update sets and perform functional testing.

## Before you begin

Role required: admin.

## About this task

![Upgrade progress bar](../image/progress-bar-phase-4.png)

The Upgrade Monitor helps you upgrade an individual instance. You can monitor the progress of an upgrade and resolve conflicts between the upgrade and customizations.

## Procedure

1.  Using the Upgrade Monitor, monitor the upgrade to your instance and validate that the upgrade to your development instance is complete.

2.  After the upgrade for your development instance is complete, [process the skipped records list](https://www.servicenow.com/docs/access?context=uc-process-skipped-records&version=australia&pubname=australia-platform-administration&ft:locale=en-US) in the Upgrade Monitor.

    As you are processing the skipped list, you may merge and revert records, resolve conflicts for an individual record, and make additional customizations. These changes go into the latest version, which goes into your current update set.

3.  Identify your update sets.

    You need these update sets for your subsequent non-production instances. If there are issues that must be addressed after the upgrade, make the appropriate changes and they will go into your current update set. Collect the update sets that:

    -   Were created while reviewing the skipped updates list.
    -   Were created while changing customizations to work with the latest release.
    -   Must go live immediately after your next upgrade.
    Gathering these update sets before your upgrade expedites the process of exporting, importing, and committing them onto your other instances. After the correct update sets are identified, follow the standard process for moving and applying those update sets. Refer to [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=australia&pubname=australia-application-development&ft:locale=en-US) for details.

4.  Before and after upgrading, conduct smoke tests on your development instance. Use your comprehensive test plan to perform functional testing.

    After upgrading, track any defects or deviations from the pre-upgrade testing results. Defect tracking can help identify root causes and create fixes. When a fix is identified, capture the fix in a single update set. The resulting update sets hold the cumulative fixes that should be applied to the production instance.

    To help automate your testing and validation on non-production instances, use the [Automated Test Framework](https://www.servicenow.com/docs/access?context=automated-test-framework&version=australia&pubname=australia-application-development&ft:locale=en-US). You can use Automated Test Framework quick start tests and product testing suites to help you jump start your testing before and after upgrades. For a list of available tests and activation information, see [Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US).


