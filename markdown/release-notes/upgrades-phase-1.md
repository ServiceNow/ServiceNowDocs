---
title: Phase 1 - Read the release notes and plan your upgrade
description: Before you begin the upgrade process, it is essential to read the release notes for your target version so you understand the required upgrade and migration tasks. This information helps you plan a safe and effective upgrade.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Upgrade to the Australia release, Australia release notes]
---

# Phase 1 - Read the release notes and plan your upgrade

Before you begin the upgrade process, it is essential to read the release notes for your target version so you understand the required upgrade and migration tasks. This information helps you plan a safe and effective upgrade.

## Before you begin

**Important:** If multiple software versions are involved in your upgrade, be sure to consult the release notes for each version between your current version and the target version.

Role required: admin.

## About this task

![Upgrade progress bar](../image/progress-bar-phase-1.png)

## Procedure

1.  Read the release notes for your target version.

    Review upgrade and migration tasks that you will need to complete before or after your upgrade.

    -   ServiceNow provides release notes for every release. The release notes offer valuable information about new functionality, notable changes, and fixes available in a particular version. Read the [Australia release notes](../../family-release-notes.md) to determine whether the upgrade contains functionality you need and fixes that resolve any issues affecting your instance. The release notes can also help you determine whether items you previously customized are being upgraded.
    -   For Australia -specific upgrade considerations, see [Pre- and post-upgrade tasks for various products](../reference/upgrade-and-migration-tasks.md).
    -   If you are thinking about upgrading to the Australia family, problem \(PRB\) fixes can be an important factor in your upgrade plans. You can generate a list of . Compare the lists of fixed problems across various Australia upgrade scenarios to help you decide which release version to upgrade to.
2.  Complete the preparation and planning tasks in Phase 2 of the [Upgrade planning checklist](../upgrades-planning-checklist.md).

    The checklist contains a list of planning tasks that guide you through various aspects of upgrade preparation. You are guided through tasks such as scoping, gathering stakeholders, identifying features to disable and enable, and creating test plans to use throughout the upgrade. Follow these steps to ensure that all aspects of your organization are ready for the upgrade.

3.  To better prepare for the upgrade, evaluate the level of customizations on your instances.

    For information on customization best practice guidelines, visit the [Customer Success Center website](https://www.servicenow.com/success/playbook/innovate-at-scale.html).

<table id="table_x55_slh_5fb"><thead><tr><th>

Complexity score

</th><th>

Customization examples

</th></tr></thead><tbody><tr><td>

Low

</td><td>

-   Modification to form layout/design
-   Add fields and/or UI policies to forms
-   Build simple custom integration
-   Extend an existing table \(such as incident\) in scope with new fields only


</td></tr><tr><td>

Low-medium

</td><td>

-   Extend an existing table \(such as incident\) in scope with some scripting
-   Extend an existing table \(such as incident\) as the basis for a different application, such as HR


</td></tr><tr><td>

Medium

</td><td>

Build a new scoped application

</td></tr><tr><td>

Medium-high

</td><td>

Build a new global application

</td></tr><tr><td>

High

</td><td>

-   Change baseline business rules \(such as modifying the SLA process\)
-   Build a complex custom integration


</td></tr></tbody>
</table>4.  Create a comprehensive test plan that includes test cases for all core instance functionality and integrations, including any customizations you may have.

    To efficiently test and evaluate system functionality, create a set of detailed test scripts for your testing team to use. You will use this test plan throughout each instance upgrade.

<table id="table_oqx_nqs_tx"><thead><tr><th>

Instance

</th><th>

Type of testing required

</th></tr></thead><tbody><tr><td>

Development

</td><td>

Conduct smoke tests.

</td></tr><tr><td>

Test

</td><td>

-   Use the ServiceNow Automated Test Framework to assist you in testing your non-production instances.
-   You can use Automated Test Framework quick start tests and product testing suites to help you jump start your testing before and after upgrades. For a list of available tests and activation information, see Quick start tests.
-   For extra testing coverage, you can also conduct user acceptance testing \(UAT\) on your non-production instances.


</td></tr><tr><td>

Production

</td><td>

Conduct UAT.**Note:** The Automated Test Framework is intended for use on non-production instances. On your production instance, conduct UAT only.

</td></tr></tbody>
</table>
