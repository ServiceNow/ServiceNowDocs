---
title: Test group characteristics
description: Define characteristics on a test group so that its test definitions can inherit them and the test group run can show them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/test-group-characteristics.html
release: brazil
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [test group characteristics, characteristic mapping, conditional test group]
breadcrumb: [Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Test group characteristics

Define characteristics on a test group so that its test definitions can inherit them and the test group run can show them.

In Service Test Management, you can define characteristics on a test group in addition to a test definition. Characteristics describe the properties that are required to run and evaluate a test. When you define them once on the test group, you don't have to repeat them on every test definition in the group.

Each characteristic belongs to either a test group or a test definition, never both. You choose the owner when you create the characteristic, and you can't change it afterward. A test definition that needs a different or additional characteristic has its own characteristic.

## How test definitions inherit characteristics

To let a test definition inherit a characteristic from its test group, you map the group characteristic to the test definition. The mapping is a configuration record, so you create it yourself. To change what a test definition inherits, you delete the mapping or add a characteristic that belongs to the test definition.

Each test group characteristic can be mapped once for a given test definition. A characteristic that belongs to a test definition can be the target of only one mapping within the same test group.

After the system selects a test definition, it applies the mapping to decide which characteristics show on the test group run. For details, see [Test group run characteristics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/test-group-run-characteristics.md).

## Selecting test groups by condition

You can add conditions to the relationship between a specification and a test group. The test group applies to a product inventory record only when the record meets the conditions. For details, see [Define conditions for a test group relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/define-conditions-for-test-group-relationship.md).

## Related tasks

-   [Define a characteristic for a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/define-characteristic-for-test-group.md)
-   [Map a test group characteristic to a test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/map-test-group-characteristics-to-test-definition.md)
-   [Define a test decomposition rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/define-test-decomposition-rule.md)
-   [Define conditions for a test group relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/define-conditions-for-test-group-relationship.md)
-   To set up the test group itself, see [Setting up a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/setting-test-group.md).

