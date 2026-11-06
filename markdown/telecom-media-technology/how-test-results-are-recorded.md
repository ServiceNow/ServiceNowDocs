---
title: Recording test results and violations
description: Test measures, threshold rule violations, and applied consequences are sent by external systems and stored against a parent record. When a duplicate is received, the system updates the existing record rather than creating a new one.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/how-test-results-are-recorded.html
release: australia
topic_type: concept
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [test measure, threshold rule violation, applied consequence, external source, external ID]
breadcrumb: [Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Recording test results and violations

Test measures, threshold rule violations, and applied consequences are sent by external systems and stored against a parent record. When a duplicate is received, the system updates the existing record rather than creating a new one.

Test measures, threshold rule violations, and applied consequences are normally sent by an external system rather than entered by users. Each record carries an external source and an external ID.

When the same test measure, violation, or applied consequence is sent again for the same parent record, the system updates the existing record instead of creating a duplicate.

On each test measure, the application keeps a text summary that shows whether the measured value meets the limits stored on the violations of that measure.

The API that receives these records is provided by the Customer Service Problem Management application. See [Related Customer Service Problem Management information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-related-cspm-information.md).

**Related topics**  


[Use Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-use.md)

[Service Test Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/st-mgmt-data-model.md)

