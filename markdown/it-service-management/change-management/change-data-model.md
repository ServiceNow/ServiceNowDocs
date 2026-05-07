---
title: Enhanced change data model
description: The enhanced Change data model supports better categorization, change model linkage, and role-based access to change templates. This new data model does not impact the existing standard change catalog and no migration of existing standard changes is required.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Enhanced change data model

The enhanced Change data model supports better categorization, change model linkage, and role-based access to change templates. This new data model does not impact the existing standard change catalog and no migration of existing standard changes is required.

Standard changes are preapproved changes available through the standard change catalog. The catalog properties define the change category and default and required change request values. The existing data model controls the properties of the standard change catalog and the standard change template.

The enhanced data model adds more customization and precision to the change creation process. It supports a separate template taxonomy, which enables Change managers to organize templates for different types of change models other than standard change catalog categories.

**Note:** The new data model is optional for newly created standard changes, so you can adopt it at your own pace without disrupting existing processes.

## Benefits of the enhanced data model

The enhanced data model provides the following advantages:

-   Enables change managers to create a taxonomy for templates that is independent of standard change catalog categories. Change managers can classify and organize templates based on the needs of the organization.
-   Introduces more precision and flexibility in the change creation process with an improved version of the standard change data model.
-   Provides the ability to create Change templates.
-   Aligns template management with the broader change model structure by inheriting properties from change models.

## Change templates

Change templates enable change managers to streamline the creation of commonly raised change requests for any change model. Templates can be created using change models, linking template management directly to the change model framework.

All template-related records, child templates, and any associated template information such as fields and field policies are managed through the change model. Change managers can define who can read, modify, or propose new templates.

Besides the Change manager, any user who is granted access to create and modify the change model through the model's Roles and User Criteria can propose and modify templates.

To use features included in the new change templates, create a template using the change template feature and select the standard change model. Alternatively, you can continue to create standard change templates using the older data model by using the Propose standard change functionality.

**Parent Topic:**[Configuring Change Management](configure-change-management.md)

**Related topics**  


[Create a Change model](../task/create-a-change-model.md)

[Create and propose a change template](../task/create-change-template.md)

