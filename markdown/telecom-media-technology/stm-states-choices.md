---
title: States and choice values
description: Review the states and the choice list values that the Service Test Management records use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/stm-states-choices.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [test definition state, test run state, test run result, severity, choice values]
breadcrumb: [Reference, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# States and choice values

Review the states and the choice list values that the Service Test Management records use.

## States

For what moves a test group run or a test run from one state to the next, see [Test group run and test run states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-run-state-model.md).

|Record|Values|
|------|------|
|Test definition state|Draft, Published, Retired, Archived. A definition can't move back to an earlier state. See [Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md).|
|Test group state|Draft, Published, Retired|
|Test run state|Draft, Pending for Input, New, Acknowledged, Rejected, Pending, In progress, Cancelled, Completed, Failed|
|Test run result|Pass, Fail, Inconclusive, Timed out|
|Test group run state|Draft, New, Pending for input, Scheduled, In progress, Cancelled, Completed|

## Choice values

|Field|Values|
|-----|------|
|Test group execution type|Manual, Automated|
|Threshold rule severity|1 - High, 2 - Medium, 3 - Low|
|Violation severity|High, Medium, Low|
|Value type|Number, String, Boolean|
|Capture frequency|Once, Daily, Weekly, Monthly|
|Capture method|Automatic, Manual|
|Conformance comparator lower|greater than, greater than or is|
|Conformance comparator upper|less than, less than or is|
|Test definition relationship type|Dependency, Substitution, Exclusivity|

