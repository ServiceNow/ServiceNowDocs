---
title: Test run in Service Test Management
description: A test run is one execution of a published test definition that validates service behavior. Create test runs from a workspace, through the subflow, or from an external system using the TMF 653 API. Check this.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/test-run-stm.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 3
breadcrumb: [Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Test run in Service Test Management

A test run is one execution of a published test definition that validates service behavior. Create test runs from a workspace, through the subflow, or from an external system using the TMF 653 API.

very test run belongs to a test group run, so a test run can't exist on its own.

You can create a test run in three ways:

-   **From a workspace**

    From a task or case in a workspace, by running diagnostics. When you start a test group run, the system creates a test run in the **Draft** state for each test definition, that you select, and its test measures and test characteristics. For more information, see [Test group run in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-run-initiation.md).

-   **From the Automated test run creation tool subflow**

    The subflow creates a test run in the **Draft** state for a test definition within a test group run. The test run takes the name of the test definition and is described it as "Automated test run for" followed by the name of the definition. It also sets the start time to the current time.

-   **From an external system**

    An external system creates and updates the test run through the TMF 653 API that Customer Service Problem Management provides. For more information, see [Related Customer Service Problem Management information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-related-cspm-information.md).


**Note:** A test run can reference only a published test definition.

For more information about how the test runs are executed, see [Test run execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-run-execution.md).

## Automated test run creation tool

The Automated test run creation tool subflow creates a test run for a test definition within a test group run. The subflow can:

-   Run a separate flow that creates test characteristics.
-   Wait for user input.
-   Wait for the test run to complete, with an optional timeout.

The subflow creates the test run in the **Draft** state, and it returns the test run that it creates. For its inputs, see [Flows, subflows, and actions installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-flows-and-actions.md). To use it, set the execution type of a test group to **Automated** and select a flow that calls the subflow. See [Create a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/create-test-group.md).

**Related topics**  


[Test group run and test run states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-run-state-model.md)

[Service Test Management automation framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-automation-framework.md)

[Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md)

