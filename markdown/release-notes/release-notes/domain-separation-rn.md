---
title: Domain Separation release notes
description: The ServiceNow Domain Separation application enables you to separate data, processes, and administrative tasks into logically defined domains. Domain Separation was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Domain Separation release notes

The ServiceNow® Domain Separation application enables you to separate data, processes, and administrative tasks into logically defined domains. Domain Separation was enhanced and updated in the Australia release.

## Domain Separation highlights for the Australia release

-   Use the new AI agent to manage domain visibility through natural language. Query, validate, add, and remove visibility settings without navigating complex admin interfaces.

-   System and domain administrators can now review a dedicated dashboard of process overrides that were affected by global process upgrades. Filter and sort overrides by date and process type to prioritize review and take action.
-   Domain visibility queries now complete in under one second for large instances — a 70% improvement for MSPs managing thousands of domains and users.

See for more information.

## New in the Australia release

-   **[AI Agent for Domain Visibility Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-sep-aia.md)**

    Use the new AI agent to manage domain visibility through natural language conversations. Domain administrators can ask the agent to query visibility by user, validate that visibility is not redundant or oversized, and take direct actions to add or remove visibility settings. The agent supports end-to-end workflows so administrators can complete multistage visibility management tasks without leaving the conversational interface. Install the Domain Separation AI Agent plugin to enable this capability.

-   **Global Domain Upgraded Process Overrides Report**

    System and domain administrators can now track and review process overrides that are affected by global process upgrades. A new admin dashboard provides a comprehensive list of impacted overrides with filtering and sorting by date and process type. Use the scriptable API to build custom integrations or automations on top of the override tracking data.

-   **Domain Visibility Performance Improvements for Large MSPs**

    Domain visibility queries now complete in under one second on average — a 70% reduction from the previous 3.2 second average for large instances. A new query optimization replaces multiple OR conditions with a single IN clause on the domain ID for instances that exceed the configured domain collection size threshold. All 785 Domain Separation customers benefit from faster queries, with the greatest impact for the 20 customers operating 10,000 or more domains.


## Changed in this release

-   **Dot-Walk Scoping Bypass Compliance \(DIRS0000335\)**

    Domain Separation has been updated to comply with the platform-wide dot-walk scoping bypass directive \(DIRS0000335\). Customers who have customizations involving dot-walk queries on domain-separated tables should review their configurations after upgrading.

-   **Java 21 Runtime Support**

    Domain Separation has been validated and updated to run on the Java 21 runtime introduced in the Australia release. Deprecated Java APIs have been removed from the Domain Separation codebase. No action is required for customers — this update is included automatically with the Australia upgrade.


## Activation information

Domain Separation is a ServiceNow AI Platform feature available with activation of the `com.glide.domain.activation_utility` plugin. For details, see [Domain separation plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-plugin.md).

**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

