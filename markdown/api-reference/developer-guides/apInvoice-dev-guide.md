---
title: AP Invoice API Developer Guide
description: This developer guide describes how to define custom invoice fields that aren’t provided by default with the AP Invoice API for Accounts Payable Invoice Processing. Instructions are also provided for setting authentication when using cXML as the payload.Use the following procedure to add custom fields for invoices, invoice lines, and invoice tax lines to be used with the AP Invoice API.Use the following procedure to map custom fields between source and target tables for the AP Invoice API.Use the following procedure to map custom fields to a payload entry in JSON, cXML, or XML for the AP Invoice API.The sn\_spend\_intg/ap\_invoice/cxml endpoint is authenticated in the payload using credentials stored in the Source System Credential \[sn\_spend\_intg\_source\_system\_credential\] table.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Developer guides, API implementation and reference]
---

# AP Invoice API Developer Guide

This developer guide describes how to define custom invoice fields that aren’t provided by default with the AP Invoice API for Accounts Payable Invoice Processing. Instructions are also provided for setting authentication when using cXML as the payload.

You can define custom invoice fields for the request body. Use the following flow to add custom fields, map them to target tables, and format them for availability in the payload:

1.  [Add custom fields for invoice import](apInvoice-dev-guide.md#)
2.  [Map custom fields between source and target tables](apInvoice-dev-guide.md#)
3.  [Map custom fields to a payload source format](apInvoice-dev-guide.md#)

Define credentials for cXML payloads in the Source system credential \[sn\_spend\_intg\_source\_system\_credential\] table. For instructions, see [Setting credentials for authentication in the cXML payload](apInvoice-dev-guide.md#).

You can apply a filter condition for invoice lines containing multiple ERPs. For information, see [Integration errors](https://www.servicenow.com/docs/access?context=integration-errors-during-erp-posting&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).

See also:

-   [Accounts Payable Invoice Processing](https://www.servicenow.com/docs/access?context=acc-pay-invoice-processing&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [AP Invoice API](../../../inbound-rest/concept/ap-invoice-api.md#)

## Add custom fields for invoice import

Use the following procedure to add custom fields for invoices, invoice lines, and invoice tax lines to be used with the AP Invoice API.

### Before you begin

-   Role required: admin
-   Application scope: [Source-to-Pay Integrations](https://www.servicenow.com/docs/access?context=source-to-pay-integrations-landing&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select one of the following invoice import tables:

    -   Invoice Import \[sn\_spend\_intg\_imp\_invoice\]
    -   Invoice Line Import \[sn\_spend\_intg\_imp\_invoice\_line\]
    -   Invoice Tax Line Import \[sn\_spend\_intg\_imp\_invoice\_tax\_line\]
3.  On the **Table Columns** tab, select **New**.

4.  Select a type associated with the field value \(for example, `Integer`\) from the **Type** menu.

    **Note:** For a list of valid types, see [Field types reference](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

5.  Enter a meaningful name in the **Column label** field.

    Text including the label is automatically populated in the **Column name** field.

6.  Select **Save** or **Submit**.

7.  Add a column of the same name and type to the Invoice \[sn\_shop\_invoice\] table.

    **Note:** For more information on columns and fields, see [Exploring field administration](https://www.servicenow.com/docs/access?context=c_IntroductionToFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

8.  [Map the fields between the source and target tables](apInvoice-dev-guide.md#).


## Map custom fields between source and target tables

Use the following procedure to map custom fields between source and target tables for the AP Invoice API.

### Before you begin

-   Role required: admin
-   Application scope: [Source-to-Pay Integrations](https://www.servicenow.com/docs/access?context=source-to-pay-integrations-landing&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)

Create table columns for mapping the new field from the source table to the target table. Use the steps in [Add custom fields for invoice import](apInvoice-dev-guide.md#).

### Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Transform Maps**.

2.  Open the Invoice Import table transform map.

3.  Click **New** on the **Field Maps** tab.

4.  Select the name of the custom field from the **Source field** menu.

5.  Select the name of the custom field from the **Target field** menu.

6.  Select **Save** or **Submit**.

7.  [Map custom fields to a payload source format](apInvoice-dev-guide.md#).


## Map custom fields to a payload source format

Use the following procedure to map custom fields to a payload entry in JSON, cXML, or XML for the AP Invoice API.

### Before you begin

-   Role required: admin
-   Application scope: [Source-to-Pay Integrations](https://www.servicenow.com/docs/access?context=source-to-pay-integrations-landing&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
-   [Add custom fields for invoice import](apInvoice-dev-guide.md#)
-   [Map custom fields between source and target tables](apInvoice-dev-guide.md#)

### Procedure

1.  Navigate to **All** &gt; **Procurement Integrations** &gt; **Suppliers** &gt; **Invoice Integration Field Mappings**.

2.  Select **New**.

3.  Add the name of the source system to the **Source system** field.

    -   If this field mapping applies to all source systems, enter `Default`.
    -   If the mapping is specific to a particular source system, this value must match the value of the Source-System header parameter received in the API.

        **Note:** All remaining field mappings must be configured specifically for this source system.

4.  Select the format of the source system for which the mapping is being created from the **Source format** choice list \(cXML or JSON\).

5.  Provide a name \(JSON property\) or path \(cXML/XML attribute or element\) for the payload entry in the **Source field** field.

    You can view the Invoice integration field mapping \[sn\_spend\_intg\_invoice\_intg\_field\_mapping\] table for examples of cXML and XML path settings.

6.  Add the name of an attribute if the field is to be defined as an element attribute for cXML payloads, otherwise leave the field empty.

7.  Select the name of the target table containing your custom field from the **Related table** list.

8.  Select the name of the custom field from the **Target field** list.

9.  Select **Save** or **Submit**.

    The mapped field is added to the Invoice integration field mapping \[sn\_spend\_intg\_invoice\_intg\_field\_mapping\] table.


## Setting credentials for authentication in the cXML payload

The sn\_spend\_intg/ap\_invoice/cxml endpoint is authenticated in the payload using credentials stored in the Source System Credential \[sn\_spend\_intg\_source\_system\_credential\] table.

### Before you begin

Role required: admin

Identify the payload source system listed in the Invoice integration field mappings \[sn\_spend\_intg\_invoice\_intg\_field\_mapping\] table.

See also [AP Invoice – POST sn\_spend\_intg/ap\_invoice/cxml](../../../inbound-rest/concept/ap-invoice-api.md#).

### Procedure

1.  Navigate to **All** &gt; **Procurement Integrations** &gt; **Source System Credentials**.

2.  Select **New**.

3.  Add the name of the source system listed in the Invoice integration field mappings \[sn\_spend\_intg\_invoice\_intg\_field\_mapping\] table in the **Source System** field.

    The source system name must match the Source-System header parameter.

4.  Add the user name to be fetched in the **User name** field.

    Use this value in the /cXML/Header/To/Credential \[@domain='NetworkID'\]/Identity element.

5.  Add a strong combination of letters, numbers, and special characters to the **Password** field.

    Use this value in the /cXML/Header/Sender/Credential \[@domain='NetworkID'\]/SharedSecret element.

6.  Select **Submit**.


