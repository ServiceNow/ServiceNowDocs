---
title: Setting definitions and value types
description: A setting definition describes a single configurable parameter on a piece of operational equipment, including its data type, value format, and optional properties such as criticality and classification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/icw-setting-definitions-and-value-types.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 3
breadcrumb: [Industrial Centerlines, Explore, Digital Factory Workspace, Industrial Connected Workforce]
---

# Setting definitions and value types

A setting definition describes a single configurable parameter on a piece of operational equipment, including its data type, value format, and optional properties such as criticality and classification.

## About setting definitions

Each setting definition represents one operator-modifiable parameter on a piece of operational equipment. Setting definitions are created directly on operational equipment items rather than inherited from equipment models or classes. Each definition specifies the setting's data type, value format, and optional descriptive properties.

Setting definitions support the following optional properties:

-   Criticality: Indicates whether the setting is critical to quality, critical to safety, or critical to release.
-   Class: Categorizes the setting as primary, changeover, or routine.
-   Unit of measure: Specifies the measurement unit for the setting value.
-   Changeover relevance: Indicates whether the setting is relevant during equipment changeovers.

Setting definitions have a state \(Draft, Pending Review, Active, Retired\), are versioned, and have an effective date range that defines when they are valid for use. Definitions can also be marked as temporary or test, making them available only for a limited time and scope.

**Note:** Updates to setting definitions require approval from a user with the Industrial Centerlines config or admin role before they can be used in a centerline task.

## Data types

Each setting definition specifies one of the following data types:

-   Numeric: Any positive or negative integer or decimal value \(for example, 0, 1.234, -34.5\) with a defined precision. Integers are represented as numeric values with no digits of precision. Decimal precision can be configured up to nine digits, with a default baseline of three digits \(for example, 3.142\).
-   String: A text value that is evaluated in a case-insensitive manner.

## Value formats

The value format defines how a setting’s value is validated and presented. The available formats depend on the data type of the setting definition.

|Value format|Description|
|------------|-----------|
|Numeric range|A numeric value that must fall within a defined range. The range is specified using up to seven limit levels. An optional target value can indicate the optimal value within the range. At least one of the upper or lower specification limits must be provided.|
|Numeric target|A specific numeric value without tolerance. The recorded value must match the target exactly to the designated precision.|
|Choice|A set of predefined string values from which the operator selects one. The allowable choices are stored as setting choice records associated with the setting definition.|
|Text|A free-text entry that is evaluated against a predefined value in a case-insensitive manner.|

## Numeric range limits

When a setting definition uses the numeric range format, the range can be specified using up to seven limit levels. These limits support both input validation and compliance evaluation during centerline task execution.

|Limit|Description|
|-----|-----------|
|Lower Entry|The lowest possible value that the setting can reach. Used as an input validation check to reject impossible or absurd values. For example, the Lower Entry for a pH setting might be 0. If not specified, any low value is accepted on input.|
|Lower Specification|The lowest allowable value for the setting. If the value is less than this limit, the settings are non-compliant.|
|Lower Warning|A value that is not considered within the optimal range but passes input validation.|
|Target|The optimal value for the setting.|
|Upper Warning|A value above the optimal range that passes input validation.|
|Upper Specification|The highest allowable value for the setting. Values above this limit are non-compliant.|
|Upper Entry|The highest possible value that the setting can reach. Used as an input validation check to reject impossible or absurd values. For example, the Upper Entry for a pH setting might be 14. If not specified, any high value is accepted on input.|

**Note:** The Upper and Lower Warning values and the Target are optional. At least one of the Upper Specification or Lower Specification values must be provided in the setting specification.

**Parent Topic:**[Industrial Centerlines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/icw-centerlining-overview.md)

