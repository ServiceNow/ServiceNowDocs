---
title: Import custom SAP named user types
description: Import custom SAP named user types into your ServiceNow instance so that you can track and manage SAP licenses based on the named user types that are specific to your SAP system.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Import custom SAP named user types

Import custom SAP named user types into your ServiceNow® instance so that you can track and manage SAP licenses based on the named user types that are specific to your SAP system.

## Before you begin

Role required: admin

## Procedure

1.  Go to [KB1299127](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1299127) to download the Microsoft Excel spreadsheet template \(imp\_samp\_sap\_custom\_nut.xlsx\) that you can use to import custom SAP named user types into your ServiceNow instance.

2.  Fill in the spreadsheet with all the custom SAP named user types that you want to import.

    The **Client**, **System**, **Named user type value**, and **Named user type name** fields are required for every entry on the spreadsheet.

3.  From your ServiceNow instance, open the SAP Custom Named User Types \[imp\_samp\_sap\_custom\_nut\] table.

    **Note:** The Application Scope of your ServiceNow instance must be set to **Software Asset Management Professional for SAP**.

    1.  On the page header of your ServiceNow® instance, select **All**.

    2.  In the menu navigation filter, enter `imp_samp_sap_custom_nut_list.do`.

        The SAP Custom Named User Types \[imp\_samp\_sap\_custom\_nut\] table opens.

4.  Right-click the table header and then select **Import**.

5.  On the form, fill in the fields.

<table id="table_k3z_qln_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Do you want to insert or update data?

</td><td>

Option that indicates whether you’re inserting new data or updating existing data in the SAP Custom Named User Types \[imp\_samp\_sap\_custom\_nut\] table.

</td></tr><tr><td>

Do you want to create an Excel template to enter data?

</td><td>

Option to generate the Microsoft Excel spreadsheet template that you can use to insert or update data in the SAP Custom Named User Types \[imp\_samp\_sap\_custom\_nut\] table. Enable this option only if didn’t already download the spreadsheet template in [step 1](import-custom-sap-named-user-type.md#dl-template).

</td></tr><tr><td class="sub-head" colspan="2">

Step 1: Create an Excel template file to enter data**Note:** This form section appears only when you enable the **Do you want to create an Excel template to enter data?** option.

</td></tr><tr><td>

Include all fields in the template

</td><td>

Option to include all available fields in the Microsoft Excel spreadsheet template.

</td></tr><tr><td>

Create Excel Template

</td><td>

Option to generate the Microsoft Excel spreadsheet template.

</td></tr><tr><td class="sub-head" colspan="2">

Step 2: Upload the template file

</td></tr><tr><td>

Excel template file

</td><td>

Microsoft Excel spreadsheet that contains the named user types that you want to insert or update in the SAP Custom Named User Types \[imp\_samp\_sap\_custom\_nut\] table.

</td></tr></tbody>
</table>6.  Select **Upload**.

7.  On successful upload, select **Preview Imported Data**.

    The Imp Tmpl Samp Sap Custom Nuts page opens.

8.  Verify that the correct number of custom SAP named user types were uploaded and then select **Complete Import**.

    The custom SAP named user types are imported into your ServiceNow® instance. The named user types are then added to the Named User Types \[samp\_named\_user\_type\] table.


**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](import-abap-program-sap.md)

[Establish an SAP connection](add-sap-connection.md)

[Create entitlements for SAP](create-entitlement-sap.md)

[Create software models for SAP](add-software-model-sap.md)

[Create a custom SAP named user type](create-named-user.md)

[Map a role to a named user type](create-named-user-type-role-mapping.md)

[Create custom SAP price lists](create-sap-pricelist.md)

[Import custom SAP price lists](import-custom-sap-price-list.md)

[SAP USMM-based optimization](../concept/usmm-optimization.md)

[User transaction activity for named user types](../concept/sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)

[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)

