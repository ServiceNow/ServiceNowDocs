---
title: Setting up a test group
description: Define tests for a particular service type, product model, or inventory to troubleshoot the service-related problems.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Customer Service Problem Management]
---

# Setting up a test group

Define tests for a particular service type, product model, or inventory to troubleshoot the service-related problems.

Test group includes relationships and measure consequences. These entities enable the system to trigger relevant tests for the service problem that help to identify the root-cause of the problem. You can define these entities for each test based on your requirements. The test group contains multiple test definitions.

Customers can set up Test groups as either manual or automated:

-   For manual types, one or more Test definitions must be attached to the Test group.
-   For automated types, you must create a Sub flow with a list of steps and add it to the group.
-   If customers want test diagnostics to run automatically and provide results directly to the agent, they can create a flow with specific trigger conditions. When a task meets these conditions, the flow runs automatically and displays the test results for the task. This may affect system performance.
-   The demo subflow with the demo data for the automated test group is provided. This demo flow can be used as a reference for creating subflow for new automated test groups.

