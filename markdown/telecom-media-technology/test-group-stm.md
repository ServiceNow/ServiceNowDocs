---
title: Test groups in Service Test Management
description: A test group organizes related test definitions and measurement consequences to help identify the root cause of a service problem. Use test groups to define manual or automated testing strategies, apply shared characteristics across test definitions, and limit scope using conditions tied to product inventory records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/test-group-stm.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 2
breadcrumb: [Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Test groups in Service Test Management

A test group organizes related test definitions and measurement consequences to help identify the root cause of a service problem. Use test groups to define manual or automated testing strategies, apply shared characteristics across test definitions, and limit scope using conditions tied to product inventory records.

A test group contains multiple test definitions and defines the relationships and measurement consequences used to identify the root cause of a service problem.You can define these entities for each test, based on your requirements. The test group contains multiple test definitions.

A test group can also have characteristics that its test definitions inherit. You can limit a test group to specific product inventory records by adding conditions to its relationship with a specification. To configure characteristics that test definitions inherit, see [Test group characteristics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-characteristics.md).

You can set up Test groups as either manual or automated:

-   **Manual**

    One or more Test definitions must be attached to the Test group.

-   **Automated**

    You must create a subflow with a list of steps and add it to the group. To run test diagnostics automatically and provide results directly to the agent, create a flow with specific trigger conditions. When a task meets these conditions, the flow runs automatically and displays the test results for the task.


**Note:** ServiceNow provides a demo subflow with demo data for the automated test group. Use this demo flow as a reference for creating subflows for new automated test groups. To learn about the automation framework, see [Service Test Management automation framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-automation-framework.md).

To create and configure a test group, see [Setting up a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/setting-test-group.md).

**Related topics**  


[Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md)

[Test group run in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-run-initiation.md)

