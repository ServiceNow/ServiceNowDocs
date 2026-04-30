---
title: Form configuration with blueprints
description: Blueprints control what the user sees on the catalog order form. You can configure the form to show or hide fields, populate fields with default values, and otherwise create a unique form for the user based on criteria.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Form configuration with blueprints

Blueprints control what the user sees on the catalog order form. You can configure the form to show or hide fields, populate fields with default values, and otherwise create a unique form for the user based on criteria.

**Note:**

-   Starting with Orlando, Cloud Provisioning blueprints are available on instances upgraded from a previous release but you cannot create new blueprints. Resource profiles and custom-created blueprints will no longer be supported starting with the Australia release.
-   Use Cloud Provisioning cloud templates to create catalog items in place of blueprints. Cloud Provisioning [cloud templates](../task/create-cloud-template.md) allow you to ingest Azure ARM, AWS CFT, Google Deployment Manager \(GDM\) and Terraform specification syntax in cloud catalog items to run your cloud deployment orchestration.

You can also change the values in form fields using policies. See [Create a cloud policy](../task/create-cloud-policy.md) and [Create a policy action script](../task/create-policy-script.md) for examples.

## Components of blueprint form configuration

Blueprints use these components to control how the system uses catalog form fields:

-   Catalog variables define the basic structure of each field on catalog order forms.
-   Rules specify an action that the system takes on a field when a condition is met.
-   Scripts query the system for information that you need to show the catalog requester, populate form fields, and process the data that users submit.
-   UI groups to put related fields together in a tab. Users can progress through tabs to fill out all the form fields.

## Start here

These tasks show you the basics of form configuration with blueprints:

-   [Add fields to a cloud catalog item order form](../task/add-fields-control-order-blueprint.md)
-   [Control visibility default values for Cloud catalog items](../task/control-form-field-visibility.md)
-   [Create a variable set for Cloud Provisioning and Governance](../task/configure-ui-group.md)

## Examples

These examples guide you through form configuration based on a specific goal: [Cloud catalog form configuration examples](example-blueprint-rules.md).

-   **[Add fields to a cloud catalog item order form](../task/add-fields-control-order-blueprint.md)**  
You can add fields to a cloud catalog form if you want the user to enter additional information beyond what a default blueprint provides.
-   **[Control visibility default values for Cloud catalog items](../task/control-form-field-visibility.md)**  
Through blueprints, you can control how form fields appear to users in the cloud catalog. For example, you can control where the fields appear to users on the catalog item form, and whether they are read only or mandatory.
-   **[Cloud catalog form configuration examples](example-blueprint-rules.md)**  
Several examples are provided to help you understand how to manipulate Cloud catalog order forms. These example cover blueprint rules, blueprint variables, and blueprint form UI groups.

**Parent Topic:**[Cloud Provisioning Blueprints](blueprints.md)

**Related topics**  


[Build a Cloud Provisioning blueprint](../task/create-blueprint-cmp.md)

