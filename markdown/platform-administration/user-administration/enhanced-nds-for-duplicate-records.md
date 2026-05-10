---
title: Enabling duplicate company names in extension tables
description: You can create records with duplicate company names in extension tables, such as Customer Account \[customer\_account\] table, without causing normalization conflicts in Normalization Data Services.Configure the Normalization Data Services feature to enable records with duplicate company names across core company's extension tables, such as Customer Account \[customer\_account\] table.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Normalization data services, Creating users, companies, departments, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enabling duplicate company names in extension tables

You can create records with duplicate company names in extension tables, such as Customer Account \[customer\_account\] table, without causing normalization conflicts in Normalization Data Services.

If your ServiceNow instance has company records in the Company \[core\_company\] table from IT Service Management \(ITSM\) or IT Operations Management \(ITOM\), and you are adopting Customer Service Management \(CSM\), you may encounter errors when creating Customer Account records for the same companies.

Normalization Data Services manages company name normalization across the Company \[core\_company\] table and its extension tables, such as Customer Account \[customer\_account\] table. By default, Normalization Data Services enforces unique company name across all company-related tables. This causes conflicts when a vendor in the Company table and a customer account share the same name.

The **glide.cmdb.canonical.use\_base\_core\_company\_only** property introduces support for creating duplicate company names in extension tables. When you enable this property, Normalization Data Services restricts unique company name validation to the base, Company \[core\_company\] table only. Each duplicate record in an extension table still links to the correct normalized record in the base table.

Enable this property if you are upgrading from Zurich or an earlier release. You must use Customer Service Management with one or more of the following applications that extend the Company \[core\_company\] table:

-   ITSM Software Asset Management
-   Hardware Asset Management

**Parent Topic:**[Normalization data services](c_NormalizationOverview.md)

## Configure Normalization Data Services to create duplicate company name in extension table

Configure the Normalization Data Services feature to enable records with duplicate company names across core company's extension tables, such as Customer Account \[customer\_account\] table.

### Before you begin

Role required: nds\_admin

### About this task

**Note:** This procedure applies only if you are upgrading from Zurich or an earlier release. If you are on the Australia release or later, this feature is enabled by default and no action is required.

### Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Script includes**.

2.  Search for and open the **ClearNonCoreCompanyExtensionsFix** script.

3.  Select **Run Script**.

    The script clears the hash values and sets the Normalized flag to false for all duplicate company name records in the Company \[core\_company\] extension tables.

4.  Verify that the script ran successfully.

    1.  Navigate to **All** &gt; **System Log** &gt; **All**.

    2.  Search for the following log entries in the Log \[syslog\_list.do\] table.

        -   \[ClearNonCoreCompanyExtensionsFix\] Cleared hash
        -   \[ClearNonCoreCompanyExtensionsFix\] Set canonical=false
    The log entries confirm that the hash values are cleared and the normalized flag is set to false.

5.  Add the **glide.cmdb.canonical.use\_base\_core\_company\_only** system property and set its value to **True**.

    For more information, see [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#).

6.  Normalize data in the CMDB table.

    1.  Navigate to **All** &gt; **Normalization Data Services** &gt; **Guided Setup**.

    2.  In the Normalize Configuration Items \(CMDB\) Model step, select **Configure**.

    3.  Select **Start Update**.

    4.  Select **Close** after the update completes.

7.  Verify if you can create records with duplicate company names in extension tables.

    1.  Navigate to **All**, and then enter `customer_account.list` in the filter to go to the Customer Account table.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        For a description of the field values, see [Account form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-account-form.md).

    4.  Select **Submit**.

8.  If you’re using Hardware Asset Management \(HAM\), run the following one-time script.

    1.  Navigate to **All** &gt; **System Definitions** &gt; **Script includes**.

    2.  Select **New**.

    3.  Enter a **Name** for the script include.

    4.  Enter the script include code in the **Script** field.

        ```
        var worker = new CanonicalUpdaterWorker(); 
                   var tables = { 
                   'sn_hamp_hw_manufacturer': ['company'],
                   'cmdb_hardware_product_model': ['normalized_company'], 
                   'cmdb_consumable_product_model': ['normalized_company'], 
            }; 
            for (var table in tables) {
                 if (tables.hasOwnProperty(table)) {
                 var fields = tables[table]; 
                 for (var i = 0; i < fields.length; i++) {
                     worker.addNormalization(table, fields[i]); 
                 } 
               } 
            } 
            worker.setProgressName(gs.getMessage("Normalization Data Service")); 
            worker.setBackground(true); 
            worker.start();
        ```

    5.  Select **Submit**.

    6.  Select **Run Script**.


