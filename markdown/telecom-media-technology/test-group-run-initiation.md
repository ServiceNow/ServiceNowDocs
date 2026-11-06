---
title: Test group run in Service Test Management
description: A test group run captures one execution of a published test group and provides a structured record of test runs, measures, and characteristics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/test-group-run-initiation.html
release: australia
topic_type: concept
last_updated: "2026-10-13"
reading_time_minutes: 3
keywords: [test group run, run diagnostics, scheduled test group run, diagnostic task]
breadcrumb: [Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Test group run in Service Test Management

A test group run captures one execution of a published test group and provides a structured record of test runs, measures, and characteristics.

Every test group run belongs to a diagnostic task, which links the run to the task or case that it was started for. You can start a test group run from a task or case in a workspace by running diagnostics.

When you start a test group run, the system creates these records:

-   A diagnostic task for the task or case. If the record already has a diagnostic task, the system reuses it. If not, the system creates one and copies the short description of the record to it. If the system can't create a diagnostic task, it shows the error "Error in creating diagnostic task" and doesn't create the test group run.
-   The test group run. It is linked to the published test group, to the diagnostic task, to the product table and product instance, and to the scheduled time if you set one.
-   One test run in the **Draft** state for each test definition that you selected. Each test run is linked to the test group run and is named after its test definition.
-   One test measure for each test measure definition of the test definition. Each test measure has the metric name, the unit of measure, and a link to its test measure definition.
-   The test characteristics that you chose for each test run, each with a characteristic, an option, and a value.

Execution begins when the test group run is in the **New** state. You can run it immediately or at a scheduled time that you choose.

-   **No scheduled time**

    The system sets the test group run state to New.

-   **Scheduled time**

    The system sets the state to **Scheduled** and queues a timed event for the scheduled time. When the time arrives, the system sets the state to **New**. If the state is no longer **Scheduled** at that time, for example because the run was cancelled, the system leaves the state unchanged and the run doesn't start.


For the states and what moves a record between them, see [Test group run and test run states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-run-state-model.md).

## New state processing

A test group run in the **New** state starts the Execute Test Group flow, which processes the draft test runs of the test group run.

The flow processes the test runs in the order that you set on the test group to definition mappings:

-   Only active mappings count. A test definition with an inactive mapping isn't processed.
-   Test runs whose mappings have the same **Order** value are handled together. The groups of test runs are handled in ascending order.

For an automated test group, the flow that you select in the **Flow** field of the test group controls execution. For information about how automated test group flows work, see [Service Test Management automation framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-automation-framework.md).

**Related topics**  


[Test group run and test run states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-run-state-model.md)

[Test run execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-run-execution.md)

[Setting up a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/setting-test-group.md)

