---
title: Service Test Management automation framework
description: Service Test Management uses flows and subflows to run tests in the background. Events, a spoke selector, and templates start and extend them. You can add your own flows and extension points to customize the behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/stm-automation-framework.html
release: australia
topic_type: concept
last_updated: "2026-10-13"
reading_time_minutes: 3
keywords: [automation framework, flow designer, subflow, spoke selector, automated test group]
breadcrumb: [Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Service Test Management automation framework

Service Test Management uses flows and subflows to run tests in the background. Events, a spoke selector, and templates start and extend them. You can add your own flows and extension points to customize the behavior.

Service Test Management runs tests in the background with Workflow Studio flows and subflows. Events, a spoke selector, and templates start and extend them.

|Building block|Description|
|--------------|-----------|
|Flows and subflows|The application installs flows and subflows that start test group runs, run test runs, record results, evaluate them, and create tasks. For more information, see [Flows, subflows, and actions installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-flows-and-actions.md).|
|Custom action types|Custom actions that the flows use, for example to prepare the request body, update the test run response, and calculate the result of a test run. For more information, see [Flows, subflows, and actions installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-flows-and-actions.md).|
|Event and script action|The event `sn_st_mgmt.schedule_test_group_run` and its script action start a scheduled test group run at the right time. The application has no scheduled jobs for this. For more information, see [Test group run in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-run-initiation.md).|
|Spoke selector|The Service Test Request in the spoke selector sends a test run to an external system through an adapter flow that you choose. For more information, see [Service Test Request spoke selector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/service-test-request-spoke-selector.md).|
|Extension point|The extension point `sn_st_mgmt.DiagnoseDataBrokerProcessor` lets another application supply the products and test definitions that apply to a task. The built-in implementation reads them from product inventory, configuration items, and the affected configuration items of the task.|

## Flow or subflow initiation

The following conditions initiate a flow or a subflow.

-   **A test group run reaches the New state**

    The Execute Test Group flow starts and processes the draft test runs.

-   **A scheduled time arrives**

    The event fires and the script action sets the test group run to New, which starts the flow above. The script action runs asynchronously.

-   **An automated test group runs**

    The flow that you selected in the **Flow** field of the test group runs. That flow can call the Automated test run creation tool subflow once for each test definition.

-   **A test run is executed**

    The Execute test run flow sends the test run through the spoke selector, and the flows that follow record and evaluate the result.

-   **Repair tasks are needed**

    The application runs the Trigger resolution tasks for test groups subflow in the foreground and waits for it to finish.


## Customization options

-   To run tests against your own external system, copy the subflow **TEMPLATE: Execute test run** and register the copy as the adapter in the spoke selector. The subflow **STM test run demo adapter** shows a working adapter that simulates a result without an external system.
-   To change how a test group is run, copy the subflow **TEMPLATE: Execute test group** and select the copy in the **Flow** field of an automated test group. A demo subflow with demo data is provided as a reference.
-   To create test characteristics for each automated test run, select your own flow in the **Test characteristics creation flow** input of the Automated test run creation tool subflow.
-   To decide which products and test definitions apply to a task, add your own implementation of the extension point.

Test runs that automation creates and evaluates are cleaned up after 30 days. See [Test run execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-run-execution.md).

**Related topics**  


[Test run in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-run-stm.md)

[Create a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/create-test-group.md)

