---
title: Test generation design considerations
description: Leverage the full potential of Test generation by following these design considerations.
locale: en-US
release: australia
product: Test Generation
classification: test-generation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Test generation references, Test generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Test generation design considerations

Leverage the full potential of Test generation by following these design considerations.

Starting with the Australia release, Test generation is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Test generation records and components

Test generation application has the following records and components.

-   **Test**

    A test is a logical grouping of related automated test steps that verify some functionality or feature. Each test is a record in the Test \[sys\_atf\_test\] table. Test designers typically create a test to verify one feature or a group of related features.

-   **Test step**

    A test step combines a step configuration with the runtime test data necessary to run a step. The test step always specifies the order in which it runs in the test. Test steps have their own related list of step results. Each test step is a record in the Test Step \[sys\_atf\_step\] table that specifies a test action, the step configuration, and an execution order. Test designers add test steps to tests to verify functionality.


## Exceptions

-   Test generation doesn't support the following test step categories:
    -   Custom UI
    -   Lists
    -   Service Catalog in Service Portal
    -   Forms in Service Portal
-   Test generation for Servicenow store provided scoped apps. Tests can be created either in Global scope or custom scope, excluding ServiceNow default scope apps.
-   Test generation doesn't support scripts and custom scripts.

## Minimum requirements

The following are the requirements to start using the Test generation application.

-   Upgrade to Yokohama
-   Purchase Creator Pro plus SKU
-   Download and install the Test generation application from ServiceNow store
-   The now.assist.creator role is required to access Test generation

**Parent Topic:**[Test generation references](tg-reference.md)

**Related topics**  


[Design considerations for prompting](tg-prompt-design-considerations.md)

