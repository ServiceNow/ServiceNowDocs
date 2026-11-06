---
title: Test definitions in Service Test Management
description: A test definition specifies the parameters, metrics, and threshold rules for a service test. Use test definitions to identify the root cause of service problems across service types, product models, and inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/test-definition-stm.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 3
breadcrumb: [Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Test definitions in Service Test Management

A test definition specifies the parameters, metrics, and threshold rules for a service test. Use test definitions to identify the root cause of service problems across service types, product models, and inventory.

Test definition includes characteristics, relationships, test meaures definitions, measure consequences, and threshold rules. These entities enable the system to trigger relevant tests for the service problem that help to identify the root cause of the problem. You can define these entities for each test based on your requirements.

To learn more about creating a test definition, see [Setting up test definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/settingup-test-specifications.md).

## Test definition lifecycle

A test definition moves forward through four states. When a test definition is moved to a state, it can't return to an earlier state.

-   **Draft**

    You can edit the test definition and its related records: relationships, test measure definitions, threshold rules, and measure consequences. A new definition starts in this state. For more information, see [Create a test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/create-test-specification.md)

-   **Published**

    The test definition is locked, and test runs can reference it. For more information, see [Publish a test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/publish-test-specification-spm.md).

-   **Retired**

    A published test definition that is no longer used. A retired definition can't be changed. For more information, see [Retire test definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/retire-test-definition.md).

-   **Archived**

    Only a retired test definition can be archived. Fore more information, see [Archive test definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/archive-test-definitions.md).


**Note:**

-   Relationships, test measure definitions, threshold rules, and measure consequences can be changed only while the test definition is in the Draft state.
-   A test definition that is the related definition of a published test definition can't be retired or archived. On the form, the system shows an error. From a list, the system skips those definitions and names them in a message.
-   A test run can reference only a published test definition.

For the messages that the system shows, see [Service Test Management error messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-error-messages.md). To reuse a locked definition as a starting point, see [Copy a test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/copy-test-definition.md).

**Related topics**  


[Test groups in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-stm.md)

[Test run in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-run-stm.md)

[Test group run in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-run-initiation.md)

