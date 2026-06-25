---
title: Import custom SAP price lists
description: Import custom SAP price lists into your ServiceNow instance so that you can track and manage SAP licenses based on the contracts that are specific to your SAP system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/import-custom-sap-price-list.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Import custom SAP price lists

Import custom SAP price lists into your ServiceNow® instance so that you can track and manage SAP licenses based on the contracts that are specific to your SAP system.

## Before you begin

Role required: admin

## Procedure

1.  Go to [KB1299127](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1299127) to download the Microsoft Excel spreadsheet template \(imp\_samp\_sap\_custom\_price\_list.xlsx\) that you can use to import custom SAP price list data into your ServiceNow instance.

2.  Fill in the spreadsheet with all the custom SAP price list data that you want to import.

    The **Client**, **System**, and **Price list value** fields are required for every entry on the spreadsheet.

    **Note:** You must fill in a separate spreadsheet for each custom SAP price list that you want to import data for.

3.  From your ServiceNow instance, open the SAP Custom Price List Data \[imp\_samp\_sap\_custom\_price\_list\] table.

    **Note:** The Application Scope of your ServiceNow instance must be set to **Software Asset Management Professional for SAP**.

    1.  On the page header of your ServiceNow instance, select **All**.

    2.  In the menu navigation filter, enter `imp_samp_sap_custom_price_list_list.do`.

        The SAP Custom Price List Data \[imp\_samp\_sap\_custom\_price\_list\] table opens.

4.  Right-click the table header and then select **Import**.

5.  On the form, fill in the fields.

<table id="table_k3z_qln_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Do you want to insert or update data?

</td><td>

Option that indicates whether you’re inserting new data or updating existing data in the SAP Custom Price List Data \[imp\_samp\_sap\_custom\_price\_list\] table.

</td></tr><tr><td>

Do you want to create an Excel template to enter data?

</td><td>

Option to generate the Microsoft Excel spreadsheet template that you can use to insert or update data in the SAP Custom Price List Data \[imp\_samp\_sap\_custom\_price\_list\] table. Enable this option only if you didn’t already download the spreadsheet template in [step 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/import-custom-sap-price-list.md).

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

Microsoft Excel spreadsheet that contains the data that you want to insert or update in the SAP Custom Price List Data \[imp\_samp\_sap\_custom\_price\_list\] table.

</td></tr></tbody>
</table>6.  Select **Upload**.

7.  On successful upload, select **Preview Imported Data**.

    The Imp Tmpl Imp Samp Sap Custom Price Lists page opens.

8.  Verify that the correct number of entries were uploaded for your custom SAP price list and then select **Complete Import**.

    The data for your custom SAP price list is imported into your ServiceNow instance. The price list is then added to the Price Lists \[samp\_price\_list\] table.

9.  Associate your custom SAP price list with additional SAP named user types.

    By default, the Software Asset Management application automatically associates your custom SAP price list with the SAP named user types that you specified in the imported Microsoft Excel spreadsheet. However, you can associate your price list with additional SAP named user types by adding custom named user types to it.

    1.  On the page header of your ServiceNow instance, select **All**.

    2.  In the menu navigation filter, enter `samp_price_list_list.do`.

        The Price Lists \[samp\_price\_list\] table opens.

    3.  Select your custom SAP price list.

        The Price List record opens.

    4.  In the **Named User Types** related list, select **New**.

    5.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the named user type.|
        |Price List|Price list that you want to associate the named user type with. This field populates automatically.|
        |Is developer|Option that indicates if users with this named user type have a developer role.|
        |Grants access to|Applications that the named user type has access to.|
        |Value|Alphanumerical value that identifies the named user type.|
        |Rank|Priority of the named user type during reconciliation. Lower rank values correlate with a higher priority during reconciliation.|
        |Is licensable|Option that indicates if the named user type can be licensed.|
        |Active|Option that indicates if the named user type is active.|

    6.  Select **Submit**.

    7.  Repeat steps d to f for each custom named user type that you want to add.


**Parent Topic:**[Software Asset Management publisher pack for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack]()

[Set up SAP integration to establish a connection with SAP]()

[Establish an SAP connection using basic authentication]()

[Establish an SAP connection using OAuth 2.0]()

[Create entitlements for SAP]()

[Create software models for SAP]()

[Create a custom SAP named user type]()

[Map a role to a named user type]()

[Create custom SAP price lists]()

[Import custom SAP named user types]()

[SAP USMM-based optimization]()

[User transaction activity for named user types]()

[Self-declaring SAP engine license usage]()

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic]()

[Publisher overview for SAP in the Software Asset Workspace]()

