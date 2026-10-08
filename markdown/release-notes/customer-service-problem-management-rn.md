---
title: Customer Service Problem Management release notes
description: The ServiceNow Customer Service Problem Management application helps customer to identify and resolve service problems. See the following sections for release notes by version.Map Test Group characteristics to Test Definition characteristics and run test definitions conditionally, so Test Run data flows through automatically to support fault isolation and repair decisions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/customer-service-problem-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [Telecommunications, Media, and Technology release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Customer Service Problem Management release notes

The ServiceNow® Customer Service Problem Management application helps customer to identify and resolve service problems. See the following sections for release notes by version.

## About Customer Service Problem Management

-   Identify and resolve service problems that customers experience, using a structured approach to customer-reported issues.
-   Define tests that diagnose service problems, then apply targeted solutions based on the results.
-   Resolve broadband and internet issues with AI-driven workflows that track network tickets and create actionable tasks for customer agents.

See [Customer Service Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/cspm-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Customer Service Problem Management by requesting it from the ServiceNow Store.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/technology-industry-rn-landing.md)

## Version 8.2.0

Map Test Group characteristics to Test Definition characteristics and run test definitions conditionally, so Test Run data flows through automatically to support fault isolation and repair decisions.

### What's new

-   **Service Lifecycle Request**

    Create cases for customer-initiated changes to the ownership of an existing service. A new case type, Account change request, extends the Customer Service base case and includes child tables to support use cases such as transfer of responsibility.


### What's changed

-   **[Test group characteristics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/test-group-characteristics.md)**

    Add characteristics directly to Test Groups, map product specifications to the Test Group that should run. Propagate those values to Test Definitions through attribute mapping and decomposition rules. The right tests run with the correct inputs for each product, reducing manual configuration and errors.


### Plugin information

-   **New plugins**

    Service Lifecycle Request \(com.sn\_slc\): Provides Service Lifecycle Request management.


