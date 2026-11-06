---
title: Service Test Management data model
description: The Service Test Management data model uses separate tables to define tests and to store test results. Understand this separation before you configure test groups, test definitions, or threshold rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/st-mgmt-data-model.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 6
keywords: [service test management, data model]
breadcrumb: [Explore, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Service Test Management data model

The Service Test Management data model uses separate tables to define tests and to store test results. Understand this separation before you configure test groups, test definitions, or threshold rules.

Service Test Management is a common application. It provides a standard test data model that other applications consume. The tables are designed to be referenced from outside the application as well as from within it.

The tables are categorized into two groups:

-   **Definition tables**

    Definition tables hold the reusable configuration that an administrator creates once. For example, a test group, the tests it contains, the measures each test captures, and the thresholds those measures are judged against.

-   **Run tables**

    Run tables hold the records the platform creates each time a test runs. For example, the captured measure values, any threshold violations, and the consequences applied as a result.


Every run record points back to the definition record it was created from. This lets you change a definition without altering the history of tests that already ran against the previous version.

\[Omitted image "st-mgmt-data-model.png"\] Alt text: Diagram of the Service Test Management tables, showing the definition tables, the reference between each run table.

## Definition tables

Use the definition tables to model the tests you run and the conditions under which a result is acceptable.

<table id="definition-tables-table"><thead><tr><th>

Table

</th><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Test Group

</td><td>

`sn_st_mgmt_test_group`

</td><td>

A named collection of test definitions that run together. Specifies whether the group runs manually or automatically, and the subflow that runs it. A group moves through the **Draft**, **Published**, and **Retired** states.

</td></tr><tr><td>

Test Group To Definition Mapping

</td><td>

`sn_st_mgmt_test_suite_to_def_mapping`

</td><td>

Links a service test group to the test definitions it contains and sets the order in which they run. Clearing the **Active** check box leaves a test definition in the group but exclude it from runs.

</td></tr><tr><td>

Service Test Definition

</td><td>

`sn_st_mgmt_test_definition`

</td><td>

A single test, including the subflow that performs it and the role required to run it. Records the dates the test was published and retired, and whether the test is a bundle of other tests.

</td></tr><tr><td>

Test Definition Relationship

</td><td>

`sn_st_mgmt_test_definition_rel`

</td><td>

Relates one test definition to another and sets the order of the relationship, so a bundled test can declare the tests it is made up of.

</td></tr><tr><td>

Test Group to Product Relationship

</td><td>

`sn_st_mgmt_test_definition_m2m`

</td><td>

Determines which products a test group applies to. Points to a product specification, a product model, or a product inventory table, and holds the conditions that must match before the group is selected for a product.

</td></tr><tr><td>

Test Measure Definition

</td><td>

`sn_st_mgmt_test_measure_definition`

</td><td>

A metric that a test captures, including how often it is captured, whether it is captured automatically or manually. Also captures the unit of measure, the value type, and the dates between which the measure is valid.

</td></tr><tr><td>

Threshold Rule

</td><td>

`sn_st_mgmt_threshold_rule`

</td><td>

The acceptable range for a test measure. Defines the comparators and target values for an exact match, a lower bound, and an upper bound. It also defines the severity, the number of crossings allowed, and the tolerance period before the rule is considered breached.

</td></tr><tr><td>

Measure Consequence

</td><td>

`sn_st_mgmt_measure_consequence`

</td><td>

The action prescribed when a threshold rule is breached, and whether that action repeats on each subsequent breach.

</td></tr></tbody>
</table>## Characteristic tables

The characteristic tables connect test groups and test definitions to characteristics and the options available for them.

<table id="characteristic-tables-table"><thead><tr><th>

Table

</th><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test Characteristic

</td><td>

`sn_st_mgmt_test_definition_characteristic`

</td><td>

A characteristic available on a test group or a test definition, with the option that applies.

</td></tr><tr><td>

Test Decomposition Rule

</td><td>

`sn_st_mgmt_test_decomposition_rule`

</td><td>

The characteristic values that decide which test definitions in a group apply to a given run, so a group decomposes into only the relevant tests.

</td></tr><tr><td>

Test Characteristic Attribute Mapping

</td><td>

`sn_st_mgmt_test_group_char_to_def_mapping`

</td><td>

Maps a characteristic on a source test to the matching characteristic on a target test, so that a value entered once passes to the tests that need it.

</td></tr></tbody>
</table>## Run tables

The platform creates run records when a test group or a test is run. You don't create these records directly.

<table id="run-tables-table"><thead><tr><th>

Table

</th><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test Group Run

</td><td>

`sn_st_mgmt_test_group_run`

</td><td>

One run of a service test group against a product instance. Holds the schedule, the state of the run, and the diagnostic task the run belongs to.

</td></tr><tr><td>

Test Run

</td><td>

`sn_st_mgmt_test`

</td><td>

One run of a single test definition. Records the result, the start and end times, the product instance and sold product tested, and whether the test ran proactively or on demand. A test run can reference a parent test run and the test group run that created it.

</td></tr><tr><td>

Test Group Characteristic Run

</td><td>

`sn_st_mgmt_test_group_char_run`

</td><td>

The characteristic values used for a test group run.

</td></tr><tr><td>

Test Definition Characteristic Run

</td><td>

`sn_st_mgmt_test_characteristic`

</td><td>

The characteristic values used for an individual test run.

</td></tr><tr><td>

Test Measure

</td><td>

`sn_st_mgmt_test_measure`

</td><td>

A metric value captured during a test run, with the capture time and method, the accuracy, the unit of measure, and the result the value produced.

</td></tr><tr><td>

Threshold Rule Violation

</td><td>

`sn_st_mgmt_measure_threshold_rule_violation`

</td><td>

A record created when a captured test measure falls outside its threshold rule. Copies the comparators, target values, and severity that were in effect, so the violation stays accurate after the rule changes.

</td></tr><tr><td>

Applied Consequence

</td><td>

`sn_st_mgmt_applied_consequence`

</td><td>

The action actually applied for a threshold rule violation, and the measure consequence it came from.

</td></tr></tbody>
</table>## Task tables

Two task tables connect test runs to the work carried out around them.

|Table|Table name|Description|
|-----|----------|-----------|
|Diagnostic Task|`sn_st_mgmt_diagnostic_task`|Groups the test group runs and test runs performed to diagnose a problem, and records whether the diagnosis is automated.|
|Resolution Task|`sn_st_mgmt_resolution_task`|Holds the list of test runs used to confirm that a problem is resolved.|

**Note:**

## Relationship between definition and run records

Each run table points to the definition table it was created from:

-   A test group run references the service test group it ran.
-   A test run references its service test definition, and the test group run that created it when the test ran as part of a group.
-   A test measure references its test measure definition.
-   A threshold rule violation references both the test measure that breached the threshold and the threshold rule it breached.
-   An applied consequence references both the threshold rule violation and the measure consequence that prescribed the action.

## Domain separation

The tables in Service Test Management carry a domain field, and the Service Test Definition and Test Run tables also carry a domain path. In a domain-separated instance, this restricts test definitions and test results to the domain that owns them.

**Note:** Plan your domain structure before you create test groups and test definitions. Records created in the wrong domain are not visible to the users who need to run or review them.

## Related applications

Other applications build on this data model rather than duplicating it. Customer Service Problem Management application creates a service problem case and uses test runs to diagnose and confirm the resolution of the customer issues. For more information, see [Related Customer Service Problem Management information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-related-cspm-information.md).

**Related topics**  


[Service Test Management components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-components.md)

[Customer Service Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/cspm-landing-page.md)

