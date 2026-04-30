---
title: ServiceNow upgrades
description: The upgrade process moves your instance to a new ServiceNow release version. Understand the difference between upgrading and patching, release definitions, rollback and backup options, and how to test your non-production and production instance upgrades.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Prepare your upgrade, Zurich release notes]
---

# ServiceNow upgrades

The upgrade process moves your instance to a new ServiceNow release version. Understand the difference between upgrading and patching, release definitions, rollback and backup options, and how to test your non-production and production instance upgrades.

Before you begin the upgrade process, read the [Zurich release notes](../../family-release-notes.md) and review the [upgrade and migration tasks for your applications and features](upgrade-and-migration-tasks.md).

![Prepare, upgrade and test the test instance, upgrade and test production instance](../image/upgrade-cycle-at-large.png)

System upgrades can be significant projects. Each ServiceNow feature release includes major additions, and you should always consider the impact of new functionality on an instance. Upgrading implements enhancements to all features that are part of the base system or are already active, unless the feature is customized on your instance. For a list of all available plugins and whether they are active by default on the base system, see [List of Zurich plugins](https://www.servicenow.com/docs/access?context=list-of-plugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Careful preparation and knowledge of the available software, tools, and resources can contribute to a successful upgrade. In addition to the materials provided by ServiceNow, it is important to understand how your ServiceNow instance is currently operating and the performance level of key business functionality. Set the expectation with IT and business users that time must be dedicated to preparing for, implementing, and testing ServiceNow upgrades.

If you have any issues during the upgrade process, [contact Customer Service and Support](http://www.servicenow.com/support/contact-support.html). Customer Service and Support is available 24 hours a day, 7 days a week to assist you with any questions or issues.

For additional help with upgrades, ServiceNow also offers various [Production Readiness Services](http://www.servicenow.com/services/production-readiness-services.html). These services specifically address challenges with instance upgradability, manageability, scalability, and performance. The reviews are performed by a ServiceNow certified professional consultant, who provide recommendations to align customer configurations with ServiceNow best practices. Contact your ServiceNow sales representative for more details.

## Upgrade and update durations in Zurich

The upgrade process takes a significantly shorter time for both updates and upgrades. \(An update occurs when an instance moves from one patch or hotfix to another within the same release family. An upgrade occurs when an instance moves from one release family to another\). As always, test your upgrades, but don't assume from the much faster completion time that the update or upgrade wasn't successful.

## Supported upgrades

You can upgrade directly to the latest release family. If multiple software versions are involved in your upgrade, be sure to consult the release notes for each version between your current version and the target version. For more information about release terminology and availability phases, see the [ServiceNow Release Cycle \[KB0547244\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244) article in the Now Support Knowledge Base.

## Upgrades vs. updates

ServiceNow organizes its releases into families. A family is a set of releases that are named after a major city, such as Zurich. Families also contain patches and hotfixes. For example, the following releases are both part of the Orlando family:

-   Orlando Patch 4
-   Orlando Patch 3 Hotfix 2

Upgrading is the act of moving to a release that is in a different family than your current release. For example, a move from London Patch 7 to Orlando Patch 3 is an upgrade because London and Orlando are different families.

Updating is the act of moving from one patch or hotfix to another within the same release family. For example, a move from Orlando Patch 1 to Orlando Patch 3 is a update because both versions are part of the Orlando family.

In both cases, the target release is Orlando Patch 3. It is the difference between your current and target release family that determines whether you are upgrading or updating.

## Features, patches, and hotfixes

Each release family contains features, patches, and hotfixes.

A feature provides a complete solution that customers can implement to add value to their organization. New features are generally only available as part of a feature release. Features are supported with patches and hotfixes.

<table id="table_tdb_lmz_kx"><thead><tr><th>

Type

</th><th>

Scope

</th></tr></thead><tbody><tr><td>

Feature

</td><td>

-   Introduces new features
-   Includes all available fixes to existing functionality
-   Is production-oriented; quality and stability are of the highest priority throughout the lifecycle

</td></tr><tr><td>

Patch

</td><td>

-   Supports existing functionality with a collection of problem fixes
-   Generally does not include new features

</td></tr><tr><td>

Hotfix

</td><td>

-   Supports existing functionality with a specific problem fix for a feature release
-   May or may not include any previous fixes for a given release
-   Does not include new features

</td></tr></tbody>
</table>For more information about release terminology and availability phases, see the [ServiceNow Release Cycle \[KB0547244\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244) article in the Now Support Knowledge Base.

## Rollbacks and backups

When you plan an upgrade, remember that ServiceNow does not provide a universal rollback option. Rollbacks are available for updates \(for example, Zurich patch-to-patch and Zurich patch-to-hotfix\). The rollback window is 10 days by default. You can customize this window by modifying the **glide.rollback.expiration\_days** property. To request a rollback, [contact Customer Service and Support](http://www.servicenow.com/support/contact-support.html).

Avoid restoring a production instance from backup, when possible, due to downtime and data loss. When a problem cannot be solved using other methods, restoring a production instance from backup is a final option. ServiceNow can restore an instance to any point in time, regardless of when a backup is completed. Customer Service and Support provides support 24 hours a day, 7 days a week for assistance with critical post-upgrade issues.

**Note:** ServiceNow does not perform on-demand backups. Instances are automatically backed up daily during non-peak business hours on schedules defined by ServiceNow. The timing of existing backup schedules is not adjusted.

## Testing throughout upgrades

Testing is an integral portion that occurs after each instance is upgraded. After you upgrade an instance, test and validate it.

This instance naming convention assumes that you have three ServiceNow instances. If you have three instances, upgrade your instances in this order:

1.  Development
2.  Test
3.  Production

If you have more or less than three instances, or if you are using Team Development, these instance labels will be different. In general, upgrade your instances furthest from production towards your production instance.

<table id="table_uzh_mqs_tx"><thead><tr><th>

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

-   Use the ServiceNow [Automated Test Framework](https://www.servicenow.com/docs/access?context=automated-test-framework&version=zurich&pubname=zurich-application-development&ft:locale=en-US) to assist you in testing your non-production instances.
-   You can use Automated Test Framework quick start tests and product testing suites to help you jump start your testing before and after upgrades. For a list of available tests and activation information, see [Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US).
-   For extra testing coverage, you can also conduct user acceptance testing \(UAT\) on your non-production instances.

</td></tr><tr><td>

Production

</td><td>

Conduct UAT.**Note:** The [Automated Test Framework](https://www.servicenow.com/docs/access?context=automated-test-framework&version=zurich&pubname=zurich-application-development&ft:locale=en-US) is intended for use on non-production instances. On your production instance, conduct UAT only.

</td></tr></tbody>
</table>If you encounter any post-upgrade issues, document the issue's conditions, steps to reproduce the issue, and your customizations. [Contact Customer Service and Support](http://www.servicenow.com/support/contact-support.html) to open an incident for each issue, and provide this information accordingly. Customer Service and Support is available 24 hours a day, 7 days a week to assist you with any questions or issues.

**Parent Topic:**[Prepare your upgrade](../../concept/rn-prepare-landing-page.md)

