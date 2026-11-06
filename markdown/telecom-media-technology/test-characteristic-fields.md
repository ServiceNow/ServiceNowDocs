---
title: Test Characteristic form fields
description: Review the fields on the Test Characteristic form and the rules that govern which characteristics you can add.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/test-characteristic-fields.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [test characteristic fields, characteristic option, is mandatory]
breadcrumb: [Reference, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Test Characteristic form fields

Review the fields on the Test Characteristic form and the rules that govern which characteristics you can add.

Characteristics are available when the Product Model plugin \(com.sn\_prd\_pm\) is active. See [Plugins installed with Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-requirements.md).

<table id="table_test_char_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Characteristic

</td><td>

Service or product characteristic that the test uses.

 The list excludes characteristics of type attachment and duration.

 For example, if you select a download speed characteristic for a speed test definition, the test measures download speed.

</td></tr><tr><td>

Characteristic option

</td><td>

Option defined for the characteristic.

</td></tr><tr><td>

Is Mandatory

</td><td>

Option that makes the characteristic mandatory for the test.

</td></tr><tr><td>

Test definition

</td><td>

Test definition that the characteristic belongs to. The system fills in this field when you add the characteristic from a test definition.

</td></tr><tr><td>

Test group

</td><td>

Test group that the characteristic belongs to. The system fills in this field when you add the characteristic from a test group.

</td></tr></tbody>
</table>## Rules

-   A characteristic belongs to either a test definition or a test group, never both. You select the owner when you create the characteristic, and you can't change it afterward.
-   Choice, yes/no, and checkbox characteristics can be added again with a different option until all the options are used. Characteristics of other types can be added once.
-   When you publish, a characteristic that has options needs a valid option that isn't repeated. A characteristic that has no options must have no option.

To let a test definition inherit a characteristic from its test group, see [Map a test group characteristic to a test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/map-test-group-characteristics-to-test-definition.md). For which characteristic appears on a test group run, see [Test group run characteristics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-run-characteristics.md).

**Related topics**  


[Define a characteristic for a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-characteristic-for-test-group.md)

