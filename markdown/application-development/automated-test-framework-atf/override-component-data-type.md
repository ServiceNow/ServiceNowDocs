---
title: Override component data type
description: Use the sn-atf-data-type and sn-atf-data-type-params attributes to override the type of field displayed in a Set Component Value test step.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Custom UI test steps, UI test steps, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Override component data type

Use the `sn-atf-data-type` and `sn-atf-data-type-params` attributes to override the type of field displayed in a Set Component Value test step.

## Before you begin

Role required: admin

## About this task

Settable components have a data type that determines what values a Custom UI test step can set. For example, a page component intended to display a reference to a particular record can have a reference data type to only display Sys ID values.

## Procedure

1.  Open the custom UI page you would like to test.

2.  Add the `sn-atf-data-type` attribute to the settable component and set the value to the field type you would like displayed in the Set Component Value test step.

    This attribute contains a string of the testable data type. The available values include those listed in the following table.

    |Attribute value|Description|
    |---------------|-----------|
    |glide\_date|Contains a string specifying a particular day.|
    |glide\_date\_time|Contains a string specifying a particular day and time of day.|
    |reference|Contains a Sys ID to a related record. This data type requires specifying additional information in the `sn-atf-data-type-params` attribute.|

3.  Add the `sn-atf-data-type-params` attribute to provide additional information when the value of `sn-atf-data-type` is `reference`.

    This attribute contains a string of JSON formatted key-value pairs. Available key-value pairs include those listed in the following table.

    |Key|Value|
    |---|-----|
    |reference|Name of the table that contains the records you want the reference field to display. For example, add `"reference":"incident"` to display records from the Incident table.|
    |reference\_qual|Filter to apply to the query. For example, add `"reference_qual":"active=true"` to display only active Incident records. See [Reference qualifiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ReferenceQualifiers.md)|


## Example

```
<input id="someTextField" value="someSysId" sn-atf-data-type="reference" sn-atf-data-type-params='{"reference":"incident","reference_qual":"active=true"}'/>
```

**Parent Topic:**[Custom UI test steps](../concept/custom-ui-test-steps.md)

