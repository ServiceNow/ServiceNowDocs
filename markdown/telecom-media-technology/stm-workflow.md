---
title: Service test management workflow
description: Understand the end-to-end workflow for service test management, from creating test definitions and setting threshold rules to publishing tests, grouping them with inventory, and recording test run results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/stm-workflow.html
release: australia
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 3
breadcrumb: [Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Service test management workflow

Understand the end-to-end workflow for service test management, from creating test definitions and setting threshold rules to publishing tests, grouping them with inventory, and recording test run results.

The following diagram shows the main tasks involved in the Service Test Management life-cycle that can be managed by this application.

\[Omitted image "MMASSET0022576-stm-workflow.svg"\] Alt text: Flowchart showing the service test management life-cycle, from creating test definitions to recording results. For the text description, refer to the steps following this diagram.

The main steps for modeling the Service Test Management are as follows:

1.  Create a test definition and define the values that it captures. For more information about test definitions, see [Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md).
2.  Set threshold rules on those values, and measure consequences on the rules. For more information, see [Define threshold rules for a test measure definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-threshold-rules.md)
3.  Publish the test definition so that test runs can reference it. For more information, see [Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md).
4.  Group test definitions and relate the group to a specification or a product model, so that the right tests apply to the right inventory. For more information, see [Test groups in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-stm.md).
5.  Define test group characteristics and map it to the test definition. For more information, see [Test group characteristics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-characteristics.md).
6.  You receive test group runs and their results. For more information, see [Test group run in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-run-initiation.md) and [Recording test results and violations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/how-test-results-are-recorded.md).

To learn about the detailed steps for modeling the STM workflow, see [Setting up test configuration records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-set-up-test-configurartion-records.md).

To learn the details of the records that Service Test Management uses, see [Service Test Management components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-components.md).

**Related topics**  


[Service Test Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/st-mgmt-data-model.md)

[Exploring Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-explore.md)

