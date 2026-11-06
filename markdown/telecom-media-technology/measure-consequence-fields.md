---
title: Measure Consequence form fields
description: Review the fields on the Measure Consequence form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/measure-consequence-fields.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [measure consequence fields, prescribed action, repeat action]
breadcrumb: [Reference, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Measure Consequence form fields

Review the fields on the Measure Consequence form.

A measure consequence belongs to one threshold rule. To create one, see [Define measure consequences for the threshold rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-threshold-consequences-spm.md).

|Field|Description|
|-----|-----------|
|Number|Identifier that the system generates for the measure consequence.|
|Name|Name of the measure consequence. Required. Maximum 250 characters.|
|Description|Description of the measure consequence. Maximum 4,000 characters.|
|Prescribed action|Action to take when the threshold rule is broken. Required. Maximum 250 characters.|
|Repeat action|Repeat flag for the prescribed action. Cleared by default.|
|Threshold rule|Threshold rule that the measure consequence belongs to. Required. The system fills in this field when you create the consequence from a threshold rule.|
|Validity start date time|Date and time from which the measure consequence applies.|
|Validity end date time|Date and time at which the measure consequence stops applying. This value can't be earlier than the validity start date and time.|

**Related topics**  


[Setting up test definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/settingup-test-specifications.md)

