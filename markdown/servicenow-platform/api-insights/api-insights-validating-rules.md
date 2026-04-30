---
title: Validating API specifications in API Insights
description: You can access API specification validation rules to verify that your API specifications are complete, consistent, and adhere to best practices.
locale: en-US
release: zurich
product: API Insights
classification: api-insights
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [CMDB administrator tasks, Configure, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Validating API specifications in API Insights

You can access API specification validation rules to verify that your API specifications are complete, consistent, and adhere to best practices.

Validation rules identify structural issues early during import or analysis, improving overall API quality. You can manage these rules to enforce standardization across API specifications and reduce errors by checking for missing or incorrect fields before APIs are published or used in production.

## Storing API specifications

The API Specification \[sn\_api\_insights\_ws\_api\_specification\] table stores the specification documents that describe individual APIs. Each record includes the following details to identify the API to which the specification belongs and to manage multiple versions.

<table id="table_mjj_v3q_tfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the API.

</td></tr><tr><td>

Version

</td><td>

Version of the API.

</td></tr><tr><td>

Type

</td><td>

Format and version of the API specification standard being used. For example, `openapi3.0.0` for an OpenAPI specification.

</td></tr><tr><td>

State

</td><td>

Current status indicating whether the API specification has been validated against the applicable rules and the validation outcome. Valid values are:-   **Unprocessed**: Indicates that the API specification hasn’t been validated.
-   **Valid**: Indicates that the API specification was validated and processed successfully or with warnings. If warnings are present, details are displayed in the **Message** field.
-   **Invalid**: Indicates that the API specification was validated but contains errors. Error details are displayed in the **Message** field.

</td></tr><tr><td>

Specification

</td><td>

Full content of the API specification file. **Note:** For OpenAPI, includes the complete OpenAPI document describing endpoints, methods, and schema.

</td></tr><tr><td>

Message

</td><td>

Messages are generated after processing all validation rules for the specification type. They include errors or warnings with explanations.

</td></tr></tbody>
</table>## Validation rule structure

The Specification Validation Rule \[sn\_api\_insights\_ws\_spec\_validation\_rule\] table stores validation rules for the API specifications defined in the API Specification \[sn\_api\_insights\_ws\_api\_specification\] table.

**Note:** The sn\_cmdb\_editor role is required to edit or delete validation rules, and the cmdb\_read role to view them.

Each validation rule contains the following key components:

<table id="table_l3b_bcq_tfc"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Specification

</td><td>

API specification for which the rule is designed.

</td></tr><tr><td>

Version

</td><td>

Version of the API specification the rule validates. If specified, the rule applies only to those versions. To restrict validation to specific versions, specify them in the **Version** field. Separate multiple values with commas. For example, `1.0,1.1,2.0`.**Note:** If the **Version** field is left empty, the rule runs for all installed versions of the specified API specification type.

</td></tr><tr><td>

Type

</td><td>

Type of validation to perform. The valid values are:-   **Path**: Verifies that the specific keys are present within arrays of objects, individual objects, or both, in the designated sections of the API specification document.
-   **Expected value**: Validates whether the specified key matches the expected values specified in the **Value** field. This validation applies only to a single key specified in the **Key** field.

</td></tr><tr><td>

Key

</td><td>

Part of the specification to verify. If no expected value is provided, you can enter multiple keys in the **Key** field, separated by commas.

</td></tr><tr><td>

Value

</td><td>

Expected values for the key specified in the **Key** field. Separate multiple values with commas.

</td></tr><tr><td>

Severity

</td><td>

Severity level of the validation rule outcome, either a warning or an error.**Note:** When set to warning, the API specification remains valid if the rule isn’t met, indicating it is not a failure, and only a message is displayed.

</td></tr><tr><td>

Message

</td><td>

Explanation of the issue when the rule is triggered.

</td></tr><tr><td>

Active

</td><td>

Option to activate the rule. Only active rules are triggered by the **API Specification Validation** scheduled job.

</td></tr></tbody>
</table>## API specification validation process

The **API Specification Validation** scheduled job automatically validates unprocessed API specifications against active rules based on their specification type to ensure compliance with required standards.

The validation process includes:

1.  Retrieving all active validation rules from the Specification Validation Rule \[sn\_api\_insights\_ws\_spec\_validation\_rule\] table.
2.  Selecting APIs marked as unprocessed in the API Specification \[sn\_api\_insights\_ws\_api\_specification\] table.
3.  Applying relevant validation rules to each selected API based on its specification type, such as OpenAPI.
4.  Verifying the presence or correctness of specific fields or their values within the API specification.
5.  Updating the processing status and capturing any errors or warnings.

## Predefined rules for OpenAPI specifications

By default, the application includes the following validation rules for OpenAPI specifications:

-   **Validate tags**

    Verifies that each tag in the API specification includes a `name` field. If the `name` field is missing, the system returns a warning message but marks the specification as valid.

-   **Validate required sections**

    Verifies that the API specification includes the required top-level sections: `info`, `paths`, and `components`. If any of these sections are missing, the system returns an error message and marks the specification as invalid.

-   **Validate servers section**

    Verifies whether the API specification includes a `servers` section that defines the server endpoints. If the `servers` section is missing, the system returns an error message and marks the specification as invalid.


These predefined rules verify critical sections such as tagging, metadata, and server definitions in OpenAPI specifications.

