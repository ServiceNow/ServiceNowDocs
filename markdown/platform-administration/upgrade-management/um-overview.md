---
title: Upgrade Console summary
description: Utilize the Upgrade Console store application to access all pertinent information and tools for your upgrade.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Exploring Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Console summary

Utilize the Upgrade Console store application to access all pertinent information and tools for your upgrade.

![Image showing the upgrade management summary page](../image/um-summary.png)

You can achieve the following using Upgrade Console.

-   Get a comprehensive, single-page view of all relevant information for an upgrade
-   Access to all required tools for an upgrade
-   Option to use the guided setup process for an upgrade on your instance
-   One-stop experience for a seamless upgrade process

**Note:** By default, you are on the Overview tab when you first land in Upgrade Console.

The following are the major sections on the Overview tab.

## Get started on your upgrade

In this section, you can view the latest three releases. You can also select the required patch version and select **Get started** to start the selected upgrade. Select Read release notes link to view the delta changes in the latest version of the release.

**Note:** This section has the above UI only when an upgrade is not scheduled.

## Upgrade scheduled

In this section, you can view the scheduled upgrade name and the start date information. You can select **Go to monitor** to go to the Monitor module to see more details on the scheduled upgrade. Select **Go to guided upgrade** to work on the pre and post upgrade activities.

**Note:** This section is visible only when an upgrade is scheduled.

## Current version

You can view the current version name in this section.

**Note:** You can also select the End of life for current version link to learn when the current version expires. See [KB0610454](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0610454) for more information.

## Tools

This section displays all the required tools needed for a seamless upgrade experience. It has the following tools:

-   Automated Test Framework: The Automated Test Framework \(ATF\) is a robust tool designed to automate the testing of your instance. By automating test creation and execution, the ATF significantly reduces the time and effort required to verify instance functionality after various changes, such as upgrades, application development, or configuration updates implemented through update sets. When a test fails, the ATF provides detailed information about the specific changes that might have caused the issue, enabling you to quickly identify and address the root cause. See [Explore ATF in Upgrade Console](um-atf-explore.md) for more details.
-   Cloning: The System Clone application facilitates the duplication of entire databases. This cloning technique, frequently employed to mirror a production instance for testing purposes, utilizes data extracted from the latest nightly backup. See [Explore Cloning in Upgrade Console](um-clone-explore.md) for more details.
-   Upgrade History: The Upgrade History module maintains a comprehensive record of all upgrades performed on your instance. This module allows you to access detailed reports of both historical and recent upgrades, providing valuable insights into the upgrade process and its outcomes. See [Explore Upgrade History in Upgrade Console](um-upgrade-history-explore.md) for more details.
-   Upgrade Monitor: The Upgrade Monitor module empowers you to efficiently manage the upgrade process. You can schedule upcoming upgrades and monitor the progress of ongoing upgrades in real-time. Once an upgrade is complete, the module provides a detailed summary of the upgrade process and a list of any records that encountered conflicts during the upgrade. See [Explore Upgrade Monitor in Upgrade Console](um-upgrade-monitor-explore.md) for more details.
-   Now Support: See [Now Support in Upgrade Console](um-now-support.md) for more details.
-   Upgrade Preview: The Upgrade Preview module offers a comprehensive solution for gaining a deep understanding of your instance's readiness for an upgrade. By providing a detailed preview of how your instance might be affected by different ServiceNow release versions, this module enables you to make informed decisions about your upgrade strategy. With the ability to explore and assess potential impacts, you can confidently plan, schedule, and prepare for your upgrade, ensuring a successful transition to the latest ServiceNow release. [Explore Upgrade Preview in Upgrade Console](um-upgrade-preview-explore.md) for more details.
-   Upgrade Skipped Record Rules Editor: To effectively manage customization requirements during and after upgrades, leverage skipped record rules. By creating these rules based on your specific conditions, you can either automate the resolution of skipped records during the upgrade process or manually execute them post-upgrade. This flexible approach empowers you to maintain control over your customizations and ensure a seamless upgrade experience. See [Explore Upgrade Skipped Record Rules Editor in Upgrade Console](um-skipped-rules-explore.md) for more details.
-   Upgrade Plans: Experience a more efficient and streamlined upgrade process with the Upgrade Plan. This feature automates the installation of applications, significantly reducing the time and effort required to complete upgrades. Upgrade Plan empowers you to take control of your upgrade process and achieve a seamless transition to the latest ServiceNow release by allowing you to define the applications and target versions to be installed in your instance. See [Explore Upgrade Plan in Upgrade Console](um-upgrade-plan-explore.md) for more details.

## Helpful Resources

This section contains links to the product documentations, knowledge base articles, and community forums.

