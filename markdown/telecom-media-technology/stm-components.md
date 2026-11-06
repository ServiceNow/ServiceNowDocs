---
title: Service Test Management components
description: Service Test Management uses several record types that work together to define, execute, and evaluate tests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/stm-components.html
release: australia
topic_type: concept
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [test definition, test measure definition, threshold rule, measure consequence, test group, test run]
breadcrumb: [Data model, Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Service Test Management components

Service Test Management uses several record types that work together to define, execute, and evaluate tests.

## Configuration records

Use these records to set up the tests you run and the conditions under which a result is acceptable.

|Record|Description|
|------|-----------|
|Test definition|A reusable test. Its state is Draft, Published, Retired, or Archived.|
|Test measure definition|One value that a test captures, such as a metric name, a unit, and a value type. Optional.|
|Threshold rule|The limit that a captured value is checked against. Each rule belongs to one test measure definition.|
|Measure consequence|An action defined for a threshold rule, with a prescribed action and a repeat option.|
|Characteristic|A service or product characteristic that a test uses. A characteristic belongs to either a test definition or a test group. Requires the Product Model plugin.|
|Test group|A set of test definitions that run together. Its execution type is Manual or Automated, and its state is Draft, Published, or Retired.|
|Specification to test group relationship|A relationship between a published test group and a specification or a product model.|

## Records that tests produce

The platform creates run records when a test group or a test is run. You don't create these records directly.

|Record|Description|
|------|-----------|
|Test group run|One execution of a test group.|
|Test run|One execution of a published test definition.|
|Test measure|One value captured during a test run.|
|Threshold rule violation|The record that the system creates when a test measure breaks a threshold rule. Its severity is High, Medium, or Low.|
|Applied consequence|An action applied because of a violation.|
|Diagnostic task and resolution task|Tasks used to investigate and fix the problems that tests find. Both extend the Task table. See [Related Customer Service Problem Management information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-related-cspm-information.md).|

For more details about the tables behind these records, see [Service Test Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/st-mgmt-data-model.md).

