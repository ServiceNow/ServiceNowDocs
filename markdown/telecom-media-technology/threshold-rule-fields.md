---
title: Threshold Rule form fields
description: Review the fields on the Threshold Rule form and the rules that govern which comparators and targets you can combine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/threshold-rule-fields.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [threshold rule fields, conformance comparator, conformance target, allowed crossing]
breadcrumb: [Reference, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Threshold Rule form fields

Review the fields on the Threshold Rule form and the rules that govern which comparators and targets you can combine.

To create a threshold rule, see [Define threshold rules for a test measure definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-threshold-rules.md).

|Field|Description|
|-----|-----------|
|Number|Identifier that the system generates for the threshold rule. Read-only.|
|Name|Name of the threshold rule. Required. Maximum 250 characters.|
|Description|Description of the threshold rule. Maximum 4,000 characters.|
|Test measure definition|Test measure definition that the rule applies to. Required. The system fills in this field when you create the rule from the Threshold Rules related list of a test measure definition. Read-only.|
|Conformance comparator exact|Option to compare the captured value against a single exact value instead of a range.|
|Conformance target exact|Value that the captured value is compared against. Required when you select **Conformance comparator exact**.|
|Conformance comparator lower|Comparator for the lower limit: greater than, or greater than or is.|
|Conformance target lower|Lower limit that the captured value is compared against. Use a numeric value.|
|Conformance comparator upper|Comparator for the upper limit: less than, or less than or is.|
|Conformance target upper|Upper limit that the captured value is compared against. Use a numeric value.|
|Number of allowed crossing|Number of threshold crossings that are allowed before a consequence is applied. Enter an integer.|
|Severity|Severity of a violation that this rule raises: 1 - High, 2 - Medium, or 3 - Low.|
|Tolerance period|Duration during which crossings are allowed without a consequence being applied.|

## Comparison rules

-   If the value type of the test measure definition is String or Boolean, select **Conformance comparator exact**.
-   If you select **Conformance comparator exact**, enter **Conformance target exact** and leave the lower and upper fields empty.
-   If you don't select **Conformance comparator exact**, leave **Conformance target exact** empty. Set a lower limit, an upper limit, or both, and give each comparator its target.
-   Use numeric values for the lower and upper targets.

