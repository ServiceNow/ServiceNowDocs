---
title: Notify release notes
description: The ServiceNow Notify application adds support for SMS and voice channels on the ServiceNow AI Platform to communicate with customers. Notify was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Notify release notes

The ServiceNow® Notify application adds support for SMS and voice channels on the ServiceNow AI Platform® to communicate with customers. Notify was enhanced and updated in the Zurich release.

## Notify highlights for the Zurich release

-   Build Notify subflows according to your requirements by using the default subflows provided in new instances.
-   Coral is the new default theme for Next Experience and Core UI, offering a user-friendly experience.

See [Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

## Important information for upgrading Notify to Zurich

Starting with the Zurich release, Notify uses subflows instead of workflows. For existing users in Zurich, your current workflows are still supported. For new users, your Notify plugin installations use subflows.

As part of this transition, the following workflow activities are available as flow actions and can be used when creating subflows:

-   Join conference call
-   Call
-   Send SMS
-   Forward call
-   Input
-   Hangup
-   Play
-   Record
-   Reject
-   Say
-   Forward to notify client
-   Queue

Maintain, build, and modify your own custom subflows in Workflow Studio with subflows for new instances. The following base system workflows have been migrated to subflows:

-   \(Re\)join Conference Call
-   Join Conference Call with muting
-   Join Conference Call with SMS

Your existing workflows continue to function after the upgrade.

**Note:** All workflow-related artifacts have been moved to a new plugin, which is maintained in a support-only mode and isn't available for new installations.

## New in the Zurich release

-   **[Notify workflow activities](https://www.servicenow.com/docs/access?context=c_NotifyActivities&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Manage the subflows for Notify use cases with the following actions.

    -   Input - Advanced: This action is intended for advanced scenarios where the **Say and Play** activity must be repeated multiple times.
    -   Get Notify Number: This action generates a Notify number by accepting the required type as input—**Voice**, **SMS**, or **both**.

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Notify is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

