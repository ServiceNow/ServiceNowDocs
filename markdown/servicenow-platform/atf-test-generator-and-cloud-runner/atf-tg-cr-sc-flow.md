---
title: Tests generation for flow and flow logic
description: Use the ATF Test Generator and Cloud Runner store application to auto-generate tests that drive a ServiceNow flow for Service Catalog.
locale: en-US
release: yokohama
product: ATF Test Generator and Cloud Runner
classification: atf-test-generator-and-cloud-runner
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Operating ATF Test Generator and Cloud Runner, ATF Test Generator and Cloud Runner, Extend ServiceNow AI Platform capabilities]
---

# Tests generation for flow and flow logic

Use the ATF Test Generator and Cloud Runner store application to auto-generate tests that drive a ServiceNow flow for Service Catalog.

## Service Catalog

By default, the ATF Test Generator and Cloud Runner store app supports the auto-generation of the tests and test steps for flows and flow logics for Service Catalog.

There are three sys properties that the process of generating tests for flows for Service Catalog is dependent on:

-   sn\_atf\_tg.enable\_flow\_generation: if set to true, only the flow generation steps are generated. The default value is true
-   sn\_atf\_tg.unsupported\_flow: It doesn’t generate steps for the mentioned flow sys id. You can mention multiple flow names separated by commas
-   sn\_atf\_tg.unsupported\_flow\_logic: It doesn’t generate steps for the mentioned flow logic. You can mention multiple flow logic names separated by commas

**Note:** If a Service Catalog item contains a flow or a flow logic, generate the test steps for flows after the record validation and record query steps are performed. A flow or a flow logic can have multiple tests and test steps.

All steps are server-side steps and the flow starts with a log message and ends with a log message. The logs are added before any actions to inform you of the actions that are followed in the flow.

## Other trigger types

Apart from Service Catalog, the following are the trigger types supported by ATF Test Generator and Cloud Runner store app.

-   Created: The flow steps begin after the initial set of record validation steps when submitting the form. It starts with a log message that contains the flow name and ends with a log message indicating the flow status.
-   Updated: If the type is updated, the flow steps will occur at the end, following the record validation steps.
-   Created or Updated: Depending on the type, the flow steps are generated either in the middle or at the end.

**Note:** For Service Catalog, only one flow is tied to a catalog item. But for the other trigger types, you can have multiple flows tied to a trigger type.

**Parent Topic:**[Operating ATF Test Generator and Cloud Runner](atf-tg-cr-operate.md)

**Related topics**  


[Generating the tests](../task/atf-tg-cr-generate-tests.md)

