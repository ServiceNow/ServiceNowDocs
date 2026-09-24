---
title: Identity release notes
description: The ServiceNow Identity application supports mechanisms that let you validate the identity of users. See the following sections for release notes by version.The Brazil Early Availability release adds security features for Identity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/identity-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform security release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Identity release notes

The ServiceNow® Identity application supports mechanisms that let you validate the identity of users. See the following sections for release notes by version.

## About Identity

-   Choose any unique field — not just User ID — as the identifier in a federated ID criteria for the User table, as long as the criteria includes at least one unique field for generating federated ID.
-   Use role masking for AI agents and agentic workflows to limit the inherited roles during tool execution, verifying that AI agents run with restricted privileges, minimizing potential security risks and helping prevent unintended actions.
-   Prevent the Conditional Script Writer group from being selected as the assignment group on task-based records, so the permission-only group is no longer used for operational assignment target.

See [Identity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/identity-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Identity is a ServiceNow AI Platform product that is active by default.


## Accessibility and localization

-   **Accessibility information**
    -   **Coral theme**

        Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Brazil Early Availability

The Brazil Early Availability release adds security features for Identity.

### What's changed

-   **[Role masking in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/role-masking.md)**

    Use role masking for AI agents and agentic workflows to limit the inherited roles during tool execution, verifying that AI agents run with restricted privileges, minimizing potential security risks and helping prevent unintended actions.

-   **[Restrict the Conditional Script Writer group from assignment group selection on Scripting Governance Tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/explore-sgt.md)**

    The Conditional Script Writer group can no longer be selected as the assignment group on any task or incident based — through the user interface with the base system configuration.

-   **[Federated ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/federated-id.md)**

    Choose any unique field — not just User ID — as the identifier in a federated ID criteria for the User table, as long as the criteria includes at least one unique field for generating federated ID.


### What's deprecated or removed

-   **[User Registration Request plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_UserRegistration.md)**

    Starting with the Brazil release, User Registration Request plugin \(com.snc.user\_registration\) is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.


### Plugin information

-   **Plugins planned for deprecation**

    User Registration Request \(com.snc.user\_registration\): Planned for deprecation in the D release. Activate External User Self-Registration and review [Activate External User Self-Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/external-user-registration-plugin.md) for configuration guidance.


