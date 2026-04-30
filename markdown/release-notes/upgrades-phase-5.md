---
title: Phase 5 - If applicable: Upgrade and validate your other non-production instances, such as your test instance
description: After you've configured and refined your development instance, request to upgrade any other non-production instances you have, such as a test instance. Immediately after the upgrade is complete, apply the post-upgrade changes made to your development instance, including activating optional plugins, installing and upgrading applications, and applying update sets.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Upgrade to the Zurich release, Zurich release notes]
---

# Phase 5 - If applicable: Upgrade and validate your other non-production instances, such as your test instance

After you've configured and refined your development instance, request to upgrade any other non-production instances you have, such as a test instance. Immediately after the upgrade is complete, apply the post-upgrade changes made to your development instance, including activating optional plugins, installing and upgrading applications, and applying update sets.

## Before you begin

Role required: admin.

## About this task

![Upgrade progress bar](../image/progress-bar-phase-5.png)

This instance naming convention assumes that you have three ServiceNow instances. If you have three instances, upgrade your instances in this order:

1.  Development
2.  Test
3.  Production

If you have more or less than three instances, or if you are using Team Development, these instance labels will be different. In general, upgrade your instances furthest from production towards your production instance.

After you have applied your development update sets to your test instance, perform the following tasks on your test instance \(and other non-production instances, if applicable\).

## Procedure

1.  Create a system clone down from your production instance.

2.  Schedule the non-production upgrade in Now Support and verify your upgrade configurations.

3.  Validate that the upgrade to your non-production instance is complete.

4.  Install any optional plugins that were installed on your development instance.

5.  Install any custom applications and post-upgrade fix scripts that you need.

6.  Install update sets.

    Use these update sets to move your initial changes into your subsequent non-production instances.

7.  Perform functional testing and monitor the performance of your instance.

    Reproduce the typical user activities that occur on your production instance. The [Automated Test Framework](https://www.servicenow.com/docs/access?context=automated-test-framework&version=zurich&pubname=zurich-application-development&ft:locale=en-US) can greatly assist you in testing your non-production instances. You can use Automated Test Framework quick start tests and product testing suites to help you jump start your testing before and after upgrades. For a list of available tests and activation information, see [Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US). For extra testing coverage, you can also conduct user acceptance testing \(UAT\).


