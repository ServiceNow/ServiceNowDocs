---
title: Create implementation in Scripted Extension Point
description: Create the implementation in the Scripted Extension Point, provided out-of-the-box, by placing it in the script include in the base application code.
locale: en-US
release: zurich
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure legal storage system, Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create implementation in Scripted Extension Point

Create the implementation in the Scripted Extension Point, provided out-of-the-box, by placing it in the script include in the base application code.

## Before you begin

The application scope must be changed to the specific application for which the implementation in the Scripted Extension Point is targeted.

Role required: You must have the specific role for the developer or administrator of the application, or you must have the admin role.

## About this task

If you want to send additional information while uploading the document, you must create the implementation in the Scripted Extension Point and store it in custom fields in the iManage Workspace. The custom fields are preset on the iManage and must be enabled for mapping. For example, &lt;custom field 1&gt; is mapped to Practice Area, &lt;custom field 2&gt; is mapped to Category, &lt;custom field 3&gt; is mapped to Requested by, and so on.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for **sn\_lg\_ops.iManageCustomFieldHelperExtension** in the API Name field, under the Legal Request Management application scope.

3.  Select the record to open.

4.  Select the **Create implementation** in the related link section.

5.  On the form, fill in the fields.

    For more information, see [Scripted Extension Point form fields](../reference/scripted-extension-point-form-fields.md).


## Result

The Implementation is created in Scripted Extension Point. For more information on how to use the script include for Scripted Extension point, see [Use the script include for Scripted Extension Point](../reference/implement-script-include-for-extn-pt.md).

-   **[Use the script include for Scripted Extension Point](../reference/implement-script-include-for-extn-pt.md)**  
Use the script include for Scripted Extension Point to update the custom fields on the iManage storage based on the mapping provided in the functions.
-   **[Scripted Extension Point form fields](../reference/scripted-extension-point-form-fields.md)**  
List of fields in the Scripted Extension Point.

**Parent Topic:**[Configure an external storage system for legal requests and legal matters](integrate-legal-ext-storage.md)

