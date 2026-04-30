---
title: Extend the License and Permit Base Case
description: As an admin, you can further extend the License and Permit install base case to define specific license/permit items received classes.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [License and Permit Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Extend the License and Permit Base Case

As an admin, you can further extend the License and Permit install base case to define specific license/permit items received classes.

## About this task

Licenses and permits are modeled as products, and for approved applications, the license or permit instances are generated and recorded in specific install base item extensions, referred to as Items Received. An admin may need to extend the base case in License and Permit Playbook to implement specific license and permit case application types with varying eligibility and application questions and combinations that may cause the License and Permit Case \(sn\_gsm\_license\_permit\_case\) table to extend beyond the 1000 column limit.

## Before you begin

Select License and Permit Playbook as the application scope when prompted.

Role required: admin

## Procedure

1.  Review the legacy permit application’s attributes and pre-determine the attributes to be created on the extended case type.

2.  Navigate to **All** &gt; **System Definition** &gt; **Tables** and select **New**.

3.  Enter the name of the license or permit for which new cases will be created.

    **Note:** The value in the Name field will be auto-populated based on the value entered in the Label field.

4.  Select the License and Permit Case value in the Extends table field.

5.  Select **Application Access** and ensure the **Can read**, **Can create**, **Can update** and **Can delete** checkboxes are selected.

6.  Select **Save** in the record header context menu.

7.  Select **New** under the Columns tab to add additional fields relevant to the license/permit application.

8.  Enter a value in the Column label field, and select options for the other column-level attributes.

9.  On the form, fill in the fields, adding new columns for each question you wish to list on the license/permit application.

    For example, application questions on a commercial fishing permit would include a vessel name, the vessel's length, the boat registration number, the vessel's home port, etc.

    **Note:** Complex inputs such as lists of information can be captured in a JSON field in the case type extension, or in custom defined tables that reference to the case type extension.

10. Select **Update**.


