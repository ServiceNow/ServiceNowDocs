---
title: Idea module form
description: Learn about the fields of the Idea module form. Use this form to create or edit the details of an idea in Innovation Management.
locale: en-US
release: xanadu
product: Innovation Management
classification: innovation-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Form field information for Innovation Management, Reference, Innovation Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Idea module form

Learn about the fields of the Idea module form. Use this form to create or edit the details of an idea in Innovation Management.

<table id="table_jzp_4ry_phb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Module name

</td><td>

Name for the module. Use a name that clearly identifies the entity for which you are creating the module. For example if you are creating a module for your departments, use the department name such as HR, Support, and IT.

</td></tr><tr><td>

Module Id

</td><td>

Unique identifier for the module used as a parameter in the Idea Portal URL to direct users. For example, if you use **hr** as the **Module Id**, the URL to access the Idea Portal would look like the following example: `/idea/?id=ideas_list&sysparm_module_id=hr`

</td></tr><tr><td>

Idea table

</td><td>

The table to be used to store ideas. This table must extend the Idea \[im\_idea\_core\] table.

</td></tr><tr><td>

Enable downvote

</td><td>

Option for activating the ability to down-vote an idea.Default: Selected

</td></tr><tr><td>

Active

</td><td>

Option for activating the idea module.Default: Selected

</td></tr><tr><td>

Category Limit

</td><td>

The maximum number of categories a user can select while submitting an idea. Default: 5This field does not appear by default on the Idea module form so you must add it by personalizing the form.

</td></tr></tbody>
</table>**Parent Topic:**[Form field information for Innovation Management](form-field-information-for-innovation-management.md)

**Related topics**  


[Create an Idea module](../task/create-idea-module.md)

