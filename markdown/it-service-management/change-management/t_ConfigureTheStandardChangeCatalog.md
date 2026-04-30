---
title: Configure standard change catalog properties
description: Configure the standard change catalog through the standard change properties.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Standard change catalog, Configure, Change Management, IT Service Management]
---

# Configure standard change catalog properties

Configure the standard change catalog through the standard change properties.

## Before you begin

The Change Management - Standard Change Catalog \[com.snc.change\_management.standard\_change\_catalog\] plugin must be activated.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Standard Change Properties**.

2.  On the form, fill in the fields.

<table id="table_cqb_hjc_zs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog

</td><td>

Select the service catalog to add the generated standard change template to.

</td></tr><tr><td>

Category

</td><td>

Select the service catalog category to add the generated standard change template to. You can also choose the category or any child categories of the selected catalog.**Note:** This value is not set automatically on the Proposal form, but must be specified before it is approved.

</td></tr><tr><td>

Two step

</td><td>

Check box to make the request of a standard change a two-step process. The process redirects the requester from a standard change template to a change request that can be reviewed before submitting.This option is enabled by default on instances provisioned on Jakarta. Customers upgrading from prior releases must enable the **Two step** property.

</td></tr><tr><td>

Mandatory Change Request values

</td><td>

Specify a list of mandatory fields that require values when you propose a new standard change template or a modification to a standard change template.This configuration ensures that when a standard change request is created from a standard change template, one or more fields on the Change Request form contain preset values.

</td></tr><tr><td>

Default Change Request values

</td><td>

Specify default values for common fields on the Change Request form.

</td></tr><tr><td>

Restricted Change Request values

</td><td>

Specify the list of fields that end users are not allowed to provide any value for when making a proposal.**Note:** Ensure that internal columns, such as **Updates**, **Updated**, **Updated by**, **Domain**, **Created**, **Created by** are restricted.

</td></tr><tr><td>

Read-only fields

</td><td>

Specify the fields that end users are not allowed to provide any value for in the created standard change request.**Note:** This configuration ensures that for the specified fields, the values approved in the standard change template do not change when the standard change request is submitted.

</td></tr><tr><td>

Fields to copy

</td><td>

Specify the fields whose values are copied to the **Propose a New Standard Change Template** record producer from a non-standard change request. **Note:** If any fields not specified in this list have default values specified, the default values are copied to the record producer.

</td></tr><tr><td class="sub-head" colspan="2">

**Change Task properties**

</td></tr><tr><td>

Mandatory Change Task fields

</td><td>

Specify a list of mandatory fields. Enter values for these fields when proposing a new change task template or modifying a change task template.

</td></tr><tr><td>

Default Change Task values

</td><td>

Specify default values for fields on the Change Task form when creating a change task template.

</td></tr><tr><td>

Restricted Change Task fields

</td><td>

Specify the list of change request fields that end users are not allowed to provide any value for when creating a change task template.

</td></tr><tr><td>

Read-only Change Task fields

</td><td>

Specify the fields that end users are not allowed to alter any value for in the change task.**Note:** This configuration ensures that for the specified fields, the values approved in the change task template do not change when the change task is created.

</td></tr><tr><td>

Change Task Fields to copy

</td><td>

Specify the fields whose values are copied to one or more change task templates when proposing a new standard change template from an existing change request.

</td></tr></tbody>
</table>3.  Select **Update**.


## What to do next

You can create a standard change catalog. By default, the basic Standard Change Proposal workflow sends approval records to members of the Change Management group and the members should verify and modify the records, as appropriate.

**Parent Topic:**[Standard change catalog](../concept/c_StandardChangeCatalogPlugin.md)

**Related topics**  


[Create a standard change task template](create-a-standard-change-task-template.md)

[Attach files to a standard change template](attach-files-change-templates.md)

[Modify or retire a standard change template](manage-standard-change-template.md)

