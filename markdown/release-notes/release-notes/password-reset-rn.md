---
title: Password Reset release notes
description: The ServiceNow Password Reset application enables you to set up your end users to reset and change their passwords either using self-service or with the help of a service desk agent. Password Reset was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Password Reset release notes

The ServiceNow® Password Reset application enables you to set up your end users to reset and change their passwords either using self-service or with the help of a service desk agent. Password Reset was enhanced and updated in the Yokohama release.

## Password Reset highlights for the Yokohama release

-   Enhanced security for all client-callable script includes by switching off the sandbox mode.
-   Enhanced security access for Password Reset tables.

See [Password Reset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/password-reset-landing-page.md) for more information.

## New in the Yokohama release

-   **[Deny ACLs for Password Reset Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/r_InstalledWithPasswordReset.md)**

    Enhance the security of Password Reset related tables by restricting access to non-authenticated users through Deny ACLs.


## Removed in this release

Password Reset workflows are deprecated and have been replaced by flows in the base system for most users. zBoot users must still use the Password Reset flows.

## Activation information

Password Reset is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-capabilities-rn-landing.md)

