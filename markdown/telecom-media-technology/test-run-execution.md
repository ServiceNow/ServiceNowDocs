---
title: Test run execution
description: When a test run is triggered, the system sends a request to the external system through a spoke, records the response, and calculates the result. An external system can also run the test and report back through the Service Test Management Open API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/test-run-execution.html
release: australia
topic_type: concept
last_updated: "2026-10-13"
reading_time_minutes: 2
keywords: [test run, test run result, test measure, automated test]
breadcrumb: [Test run, Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Test run execution

When a test run is triggered, the system sends a request to the external system through a spoke, records the response, and calculates the result. An external system can also run the test and report back through the Service Test Management Open API.

## Test execution against external systems

For a test that runs against an external system, the system works through these steps:

1.  The Execute test run flow takes one test run.
2.  The flow builds a request body from the test run and its test measure definitions, and sends a Service Test Request through the spoke selector. See [Service Test Request spoke selector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/service-test-request-spoke-selector.md).
3.  The adapter flow that the spoke selector selects sends the request to the external system and receives the response.
4.  The system writes the response to the test run, and writes the returned values to the test measures.
5.  The system calculates the result of the test run and compares each value with the threshold rules.
6.  If a value breaks a threshold rule, the system creates a threshold rule violation and applies the measure consequences. For a failed test run that is linked to a service problem case, the system can also create resolution tasks.

The result is one of **Pass**, **Fail**, **Inconclusive**, or **Timed out**. The result is separate from the state of the test run. See [States and choice values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-states-choices.md).

## Reporting test results from an external system

An external system can run the test itself and report back instead of using the spoke selector. It updates the test run through the Service Test Management Open API \(TMF 653\). The update can set the state, the start and end times, the validity period, the characteristics, and the test measures, including their violations and applied consequences. See [Recording test results and violations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/how-test-results-are-recorded.md).

## Test run retention period

A scheduled clean-up deletes test runs in the **Cancelled**, **Completed**, or **Failed** state 30 days after they were created, together with the records that depend on them.

**Related topics**  


[Test group run and test run states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-run-state-model.md)

[Review a test run](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/review-test-run.md)

