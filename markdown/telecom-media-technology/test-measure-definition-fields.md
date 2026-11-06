---
title: Test Measure Definition form fields
description: Review the fields on the Test Measure Definition form in the Service Test Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/test-measure-definition-fields.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [test measure definition fields, metric name, capture frequency]
breadcrumb: [Reference, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Test Measure Definition form fields

Review the fields on the Test Measure Definition form in the Service Test Management application.

Test measure definitions are optional. You can publish a test definition that has none. To define one, see [Define test measure definitions for a service test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-test-measure-spm.md).

|Field|Description|
|-----|-----------|
|Number|Identifier that the system generates for the test measure definition.|
|Name|Name of the test measure definition. Required. Maximum 250 characters.|
|Metric name|Name of the metric that the test captures. Required. Maximum 250 characters.|
|Metric description|Description of the metric. Maximum 4,000 characters.|
|Unit of measure|Unit that the captured value is expressed in, such as seconds or megabits per second. Required.|
|Value type|Type of the captured value: Number, String, or Boolean. The type determines which comparator a threshold rule can use. See [Threshold Rule form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/threshold-rule-fields.md).|
|Capture frequency|How often the value is captured: Once, Daily, Weekly, or Monthly.|
|Capture method|How the value is captured: Automatic or Manual.|
|Capture period|Duration over which the value is captured.|
|Validity start date time|Date and time from which the test measure definition applies.|
|Validity end date time|Date and time at which the test measure definition stops applying. This value can't be earlier than the validity start date and time.|
|Test definition|Test definition that the test measure definition belongs to. The system fills in this field.|

**Related topics**  


[Setting up test definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/settingup-test-specifications.md)

