---
title: Create or modify a record producer for legal services through Classic environment
description: Create or modify a record producer to define an intake form for a legal request. Employees can use these intake forms on the Legal Service Portal to submit legal requests.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Managing record producers for legal services, Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create or modify a record producer for legal services through Classic environment

Create or modify a record producer to define an intake form for a legal request. Employees can use these intake forms on the Legal Service Portal to submit legal requests.

## Before you begin

Ensure that you have the Legal Request Management application scope selected.

Role required: sn\_lg\_ops.legal\_catalog\_admin

## About this task

To manage record producers using Catalog Builder, see [create or modify a record producer for legal services through Catalog Builder](create-record-producer-catalog-builder-legal.md).

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Legal Catalog** &gt; **Record Producers**.

2.  Create or modify a record producer.

    -   To create a record producer, click **New**.
    -   To modify an existing record producer, open the record producer from the list.
3.  On the form, fill in the fields.

<table id="table_jn3_jrx_djb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the record producer.

</td></tr><tr><td>

Table name

</td><td>

Name of the table that stores the data collected through the record producer.-   Select **Legal Request \[sn\_lg\_ops\_request\]** if you are creating the record producer for legal requests.
-   Select **Legal Matter \[sn\_lg\_matter\_matter\]** if you are creating the record producer for legal matters.

**Note:** You must have installed the Legal Matter Management app to use this option.

-   Select a table specific to a practice area if you want to use the data collected from the record producer for reporting. For more information, see [Configure a practice area table](configure-pa-tables-for-reporting.md).


</td></tr><tr><td>

Application

</td><td>

Application to which the record producer belongs. This field is automatically set to the application scope in which you are creating the record producer.

</td></tr><tr><td>

Active

</td><td>

Option for marking the record producer active.Only active record producers are available as legal intake forms in the Legal Service Portal.

</td></tr><tr><td class="sub-head" colspan="2">

What it will contain tab

</td></tr><tr><td>

Short description

</td><td>

Brief description of the record producer.

</td></tr><tr><td>

Description

</td><td>

Full description of the record producer.

</td></tr><tr><td>

Script

</td><td>

Script that dynamically assigns values to specific fields on the created record.

</td></tr><tr><td class="sub-head" colspan="2">

Accessibility tab

</td></tr><tr><td>

Catalogs

</td><td>

Name of the service catalog to which the record producer belongs. Select **Legal Operations Catalog**.

</td></tr><tr><td>

Category

</td><td>

Name of the [service catalog category](add-catalog-categories.md) in which the intake form should appear in the Legal Service Portal.

</td></tr></tbody>
</table>4.  Save the record producer.

    -   Save a new record producer by clicking **Submit**.
    -   Save the changes to an existing record producer by clicking **Update**.
5.  In the Variables related list, add or modify variables.

    Variables in a record producer appear as fields on the legal intake form to collect information from employees when they're submitting a legal request.

    **Important:** If you are configuring the record producer for a practice area table, you must map the variable with a column name of the selected table. On the Variable form, select the **Map to field** check box and the column name of the selected practice area table in the **Field**. Only the mapped variables are copied to the columns of the selected table.

    For more information on creating variables, see [Create a service catalog variable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/t_CreateAVariableForACatalogItem.md).

6.  In the Assigned topics related list, assign the catalog item to a topic in a taxonomy so that the catalog item is added to the Employee Center portal.

    For more information on assigned topics and taxonomy, see [Unified Taxonomy for Employee Center](../../employee-center/concept/config-taxonomy.md).

7.  In the Applicable For and Not Applicable For related lists, apply the user criteria to control access of the record producer.

    User criteria define conditions for user records that enable you to grant or deny access to the record producer for users matching those conditions. For more information on creating a user criteria, see [Set up the user criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/t_CreateAUserCriteriaRecord.md).

8.  If you have enabled the option to [save attached documents for a legal request in an external storage](associate-categories-practice-area.md), you can add the script to validate the documents attached to a legal request while submitting.

    1.  In the Catalog Client Scripts related list, click **New**.

    2.  On the Catalog Client Scripts form, fill in the fields.

        For more information, see [Create a Service Catalog client script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/t_CreateACatalogClientScript.md).

    3.  In the **Script** field, copy the following client script which runs on the catalog item to determine if:

        -   The file size of the document being uploaded is within the permitted limits.

            This check applies to Microsoft OneDrive external storage.

        -   A file with the same name already exists in the folder.
        ```js
        var status = true;
                var uniqueNames = [];
                var duplicateNames = [];
                var largeFileNames = [];
                var attachments = this.angular.element("#sc_cat_item").scope().attachments;
                attachments.forEach(function(attachment) {
                    var name = attachment['file_name'];
                    var size = getSizeInBytes(attachment['size']);
                    if (uniqueNames.indexOf(name) != -1) {
                        duplicateNames.push(name);
                    } else if (size > 4000000) {
                        largeFileNames.push(name);
                    }
                    uniqueNames.push(name);
                });
                if (largeFileNames.length > 0) {
                    g_form.addErrorMessage("Size of file should be less than or equal to 4Mb");
                    largeFileNames.forEach(function(name) {
                        g_form.addErrorMessage(name + " is more than 4Mb");
                    });
                    status = false;
                }
                if (duplicateNames.length > 0) {
                    g_form.addErrorMessage("File names should be unique");
                    duplicateNames.forEach(function(name) {
                        g_form.addErrorMessage(name + " found with a duplicate name");
                    });
                    status = false;
                }
                return status;
            }
        }
        function getSizeInBytes(size) {
            var unit = size.split(" ")[1];
            var value = parseFloat(size.split(" ")[0]);
            switch (unit) {
                case "MB":
                    value = value * 1000000;
                    break;
                case "KB":
                    value = value * 1000;
                    break;
            }
            return value;
        }
        ```


**Parent Topic:**[Managing record producers for legal services](../concept/record-producers-legal-services.md)

