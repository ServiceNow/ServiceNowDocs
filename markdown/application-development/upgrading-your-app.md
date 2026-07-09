---
title: Updating your app for a ServiceNow platform version
description: When ServiceNow releases a new platform version, your app may need updates to keep working correctly. Learn how platform upgrades affect your app helps you plan and complete the upgrade with confidence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/upgrading-your-app.html
release: australia
topic_type: concept
last_updated: "2024-01-01"
reading_time_minutes: 4
keywords: [app upgrade, platform version, compatibility]
breadcrumb: [Version control, Getting Started guide for developers, Building applications]
---

# Updating your app for a ServiceNow platform version

When ServiceNow releases a new platform version, your app may need updates to keep working correctly. Learn how platform upgrades affect your app helps you plan and complete the upgrade with confidence.

ServiceNow releases platform versions on a regular schedule. Each version can include changes to APIs, system tables, UI frameworks, and scripting behavior. If your app uses any of these, parts of it might stop working after the upgrade.

Reviewing your app before the upgrade reaches production gives you time to find and fix compatibility issues in a safe, controlled environment. This reduces the risk of unexpected failures on your production instance.

## How does Git makes upgrades?

When your app is linked to a Git repository, you can isolate all upgrade-related work on a dedicated branch. This approach provides several benefits:

-   Your team can continue feature development on other branches without interruption.
-   All compatibility fixes are reviewed through a pull request before they reach your main branch.
-   You have a clear record of every change made during the upgrade, who reviewed it, and why it was needed.
-   You can roll back to a tagged release if issues appear after the upgrade goes to production.

## What to check before and after an upgrade

Not every platform change affects your app. Focus your review on the areas most likely to cause compatibility issues:

-   **Scripting APIs and GlideRecord methods**

    ServiceNow may deprecate or remove scripting APIs in a version. Check the release notes for your target version. Look for any APIs your app uses that are listed as deprecated or removed. Replace them with the current alternatives before testing.

-   **System tables and column names**

    Platform versions sometimes rename or restructure system tables and columns. If your app queries or references these directly, the queries may return unexpected results or fail after the upgrade.

-   **UI components and front-end frameworks**

    If your app includes UI Builder pages, Service Portal widgets, or Now Experience components, check whether the underlying framework has changed in the version. Visual behavior and component APIs can shift between releases.

-   **Security policies and ACL rules**

    Changes to ACL evaluation order or scope boundary behavior can affect what your app can access and how it responds to user permissions. Review any security-sensitive parts of your app carefully after the upgrade.

-   **Flow Designer actions and IntegrationHub spokes**

    If your app uses Flow Designer flows or IntegrationHub spokes, check whether those components have been updated or changed in the platform version. An updated spoke may behave differently or require updated input configurations.


## The role of automated testing in an upgrade

Running your Automated Test Framework tests on the upgraded test instance is one of the most reliable ways to find compatibility issues quickly. ATF tests give you a structured signal about what is broken and where to focus your fix effort.

Automated tests alone aren't enough. After your tests pass, manually walk through your App's key user flows to catch behavioral or visual changes that tests might not detect. Check form behavior, UI rendering, workflow triggers, and any integration responses.

If your app doesn't have ATF tests yet, an upgrade cycle is a good time to add basic smoke tests for your core workflows. This gives you a reliable baseline for every future upgrade.

## Using a branch strategy for upgrade work

Create a dedicated branch for each platform upgrade. Name it clearly to identify the target version, for example `upgrade/yokohama`. Branch from your current stable release line so you're working from a known good state.

Commit each compatibility fix separately with a short message that explains the change and references the relevant release note. This keeps the branch history readable and makes the pull request review straightforward.

After the pull request is approved and merged, tag the release to mark the point at which your app became compatible with the platform version. A tag like `v2.4.0-yokohama` gives you a clear reference for future comparisons and rollbacks.

## What to do after the upgrade is complete

After your app is running on the platform version in production, take a few steps to close out the upgrade properly:

-   Keep your upgrade branch in the repository as a reference. Don't delete it right away. Issues sometimes appear on production in the weeks following an upgrade, and the branch gives you useful context.
-   Update your app's release notes and internal documentation to reflect any API or behavior changes made during the upgrade.
-   Add ATF tests for any coverage gaps the upgrade revealed so you're better prepared for the next cycle.
-   Monitor the release notes for the next ServiceNow platform version early. Starting your review sooner gives you more time to plan and reduces the pressure of the next upgrade cycle.

**Parent Topic:**[Version control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/version-control.md)

