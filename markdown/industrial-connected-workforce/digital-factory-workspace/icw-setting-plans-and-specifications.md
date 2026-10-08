---
title: Setting plans and specifications
description: Setting plans group one or more setting specifications for a given equipment and material context. Setting specifications define the standard values and limits for each setting definition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/icw-setting-plans-and-specifications.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 2
breadcrumb: [Industrial Centerlines, Explore, Digital Factory Workspace, Industrial Connected Workforce]
---

# Setting plans and specifications

Setting plans group one or more setting specifications for a given equipment and material context. Setting specifications define the standard values and limits for each setting definition.

## Setting plans

A setting plan is a container that groups setting specifications for a piece of operational equipment. Plans provide versioning, effective date management, and approval workflows for the standard values applied to equipment settings.

Setting plans support the following capabilities:

-   Versioning: Each plan has a version number that increments from previous versions. A reference to the previous version is stored for traceability.
-   Effective dating: Plans have effective start and end dates that define when the plan is valid for use.
-   Temporary plans: Plans can be marked as temporary with a temporary start and expiration date, making them available for a limited time.
-   State management: Plans follow a state workflow of Draft, Pending Review, Active, and Retired.
-   Approval: Plans have an approval field with values of Not yet Requested, Requested, Approved, and Declined.
-   Duplication: You can duplicate an existing plan to create a new version, copying the setting specifications without re-entering all values.
-   Retirement: You can retire a published setting plan to indicate that it is no longer valid for use in centerline tasks. Retiring a plan moves its state from Published to Retired.

**Note:** Updates to setting plans require approval from a user with an authorized role before they can be used in a centerline task.

## Setting specifications

A setting specification defines the actual standard values for a specific setting definition within a setting plan. The values in a specification depend on the value format of the associated setting definition:

-   Numeric range: The specification provides the limit values \(Lower Entry, Lower Specification, Lower Warning, Target, Upper Warning, Upper Specification, Upper Entry\) that define the acceptable range. At least one of the Upper Specification or Lower Specification values must be provided.
-   Numeric target: The specification provides a single target value that the confirmed value must match exactly.
-   Choice: The specification provides a single value selected from the predefined choices in the setting definition.
-   Text: The specification provides the expected text value for comparison.

Setting specifications share the same versioning, effective dating, temporary marking, and approval workflow as setting plans.

## Validation rules for numeric range specifications

When defining specifications for setting definitions with a numeric range format, the following validation rules apply:

-   At least one of the Upper Specification or Lower Specification values must be provided.
-   If only the Lower Specification is provided, any value greater than or equal to the Lower Specification is valid, subject to the Upper Entry value if provided.
-   If only the Upper Specification is provided, any value less than or equal to the Upper Specification is valid, subject to the Lower Entry value if provided.
-   The Upper and Lower Warning values and the Target are optional.

## Material-based specifications

In the data model, specification values can vary based on material classification, material model, or material characteristic. Different standard values are supported for the same equipment setting, depending on the material being processed.

**Parent Topic:**[Industrial Centerlines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/icw-centerlining-overview.md)

