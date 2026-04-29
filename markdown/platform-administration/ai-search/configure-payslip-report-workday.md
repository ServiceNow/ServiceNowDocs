---
title: Configure a payslip report in Workday
description: Configure a custom report for payroll data in Workday. The Workday external content connector uses this report to make content and metadata from your payroll data searchable.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Workday external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a payslip report in Workday

Configure a custom report for payroll data in Workday. The Workday external content connector uses this report to make content and metadata from your payroll data searchable.

## Before you begin

A Workday admin must have already an integration system user and an unconstrained integration system security group in your Workday tenant. For details on this preliminary task, see [Configure Workday security settings](configure-workday-security-settings.md).

You need an account with the following privileges in your organization's Workday tenant:

-   **Custom Report Creation** domain access
-   Access to the **Payroll Results** report data source
-   **Copy Standard Report to Custom Report** task access

Role required: none

## About this task

This task is optional. The Workday external content connector can retrieve payslip data from your Workday source system using a custom report that you configure. If you don't want to retrieve payslip data from Workday, you can skip this task.

## Procedure

1.  Log in to your Workday tenant with your administrator credentials.

2.  Create a new custom report from the Payslip to Print - Report Design standard report.

    1.  In the Workday search bar, search for the **Copy Standard Report to Custom Report** task and select it.

    2.  On the Copy Standard Report to Custom Report page, in the Standard Report field, search for the **Payslip to Print - Report Design** report and select it.

    3.  Enter a name for your custom report.

        As an example, you might enter `Workday connector payslip report`.

    4.  Select **OK**.

    Workday creates your new custom report and displays its configuration screen.

3.  In the Data Source field, search for the **Payroll Results** entry and select it.

    Workday automatically populates the Data Source Filter field.

4.  Configure the columns for your new custom report.

    1.  On the Columns tab for your new custom report, in the table, select **+** to add a row for a new column.

    2.  Select or enter the following field values for the new column.

        |Business Object|Field|Column Heading Override|Column Heading Override XML Alias|
        |---------------|-----|-----------------------|---------------------------------|
        |Payroll Result|Sub Period \(if different from Pay Period\)| |Sub\_Period\_if\_different\_from\_Pay\_Period|

    3.  For each row in the table that has **Absence Plans** specified as its Business Object, select **–** to remove the row.

5.  Configure the group column headings for your new custom report.

    1.  In the Group Column Headings table, select **–** to remove the row that has **Absence Plans** specified as its Business Object.

    2.  For each remaining group column header rows, select and delete all text in the Group Column Heading field.

6.  Configure the prompts for your new custom report.

    1.  On the Prompts tab for your new custom report, in the Prompt Defaults table, select **–** to remove the existing prompt row.

    2.  Select the **Populate Undefined Prompt Defaults** option.

        Workday automatically populates the Prompt Defaults table with built-in prompts.

7.  On the Advanced tab for your new custom report, select the **Enable As Web Service** option if it's not already selected, then select **OK**.

    Workday saves your configuration changes for your new custom report.

8.  Transfer ownership of your new custom report to the integration system user created for the Workday external content connector.

    1.  From the View Custom Report page, navigate to **…** &gt; **Custom Report** &gt; **Transfer Ownership**.

    2.  On the Transfer Ownership of Custom Reports page, in the New Owner field, enter or select the **ISU SNOW ACL** integration system user account.

        **Important:** If you don't see this integration system user account in the system, check that a Workday admin has completed the [Configure Workday security settings](configure-workday-security-settings.md) preliminary task.

    3.  Select **OK**.

9.  Generate a sample report using your new custom report and copy its CSV URL.

    1.  On the View Custom Report page for your new custom report, navigate to **...** &gt; **Web Service** &gt; **View URLs**.

    2.  On the View URLs Web Service page, configure a sample report by filling in the fields.

        |Field|Value|
        |-----|-----|
        |Period Date Indicator|Select **Based on Payment Date**.|
        |End Date|Select an arbitrary end date for the report. The end date must occur after your specified start date.|
        |Start Date|Select an arbitrary start date for the report.|
        |Worker|Select any member of your Workday organization.|

    3.  Select **OK**.

        Workday displays parameters and URLs for your sample report.

    4.  Long-press \(or right-click\) the **CSV** link and copy the CSV URL.

    5.  Paste the copied URL into a web browser or a text editor.

    The CSV URL has the format `https://<hostname>.workday.com/ccx/service/customreport2/<tenant-name>/<report-owner-user-name>/<report-name-alias>`. This URL may optionally be followed by a question mark and one or more URL parameters separated by ampersands. As an example, your CSV URL might be `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_payslip_report?Period_Date_Indicator%21WID=e3e3e13f80904ee185eab1fbf331acef`.

10. Copy the base URL for your Workday tenant, your Workday tenant name, the custom report owner's user name, the custom report name alias, and the period date indicator Workday ID \(WID\).

    1.  Copy the base URL for your Workday tenant from the pasted CSV URL and store it in a secure location.

        The base URL for your Workday tenant is the `https://<hostname>.workday.com` portion of the CSV URL \(everything before the third slash character\). As an example, if your CSV URL is `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_payslip_report?Period_Date_Indicator%21WID=e3e3e13f80904ee185eab1fbf331acef`, the base URL for your Workday tenant is `https://wd2-impl-services1.workday.com`.

        **Important:** Your external content connector admin needs this base URL when configuring the Workday external content connector.

    2.  Copy the tenant name for your Workday tenant from the pasted CSV URL and store it in a secure location.

        The tenant name for your Workday tenant is the `<tenant-name>` portion of the CSV URL \(everything between the sixth and seventh slash characters\). As an example, if your CSV URL is `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_payslip_report?Period_Date_Indicator%21WID=e3e3e13f80904ee185eab1fbf331acef`, your Workday tenant name is `Example`.

        **Important:** Your external content connector admin needs this tenant name when configuring the Workday external content connector.

    3.  Copy the report owner's user name for your custom payslip report from the pasted CSV URL and store it in a secure location.

        The report owner's user name for your custom payslip report is the `<report-owner-user-name>` portion of the CSV URL \(everything between the seventh and eighth slash characters\). As an example, if your CSV URL is `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_payslip_report?Period_Date_Indicator%21WID=e3e3e13f80904ee185eab1fbf331acef`, your custom payslip report owner's user name is `ISU_SNOW_ACL`.

        **Important:** Your external content connector admin needs this payslip report owner's user name when configuring the Workday external content connector.

    4.  Copy the report name alias for your custom payslip report from the pasted CSV URL and store it in a secure location.

        The report name alias for your custom payslip report is the `<report-name-alias>` portion of the CSV URL \(everything between the eighth slash character and the question mark or the end of the URL\). As an example, if your CSV URL is `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_payslip_report?Period_Date_Indicator%21WID=e3e3e13f80904ee185eab1fbf331acef`, your custom payslip report name alias is `Workday_connector_payslip_report`.

        **Important:** Your external content connector admin needs this payslip report name alias when configuring the Workday external content connector.

    5.  Copy the period date indicator WID \(Workday ID\) for your custom payslip report from the pasted CSV URL and store it in a secure location.

        The period date indicator WID for your custom payslip report is the value of the `Period_Date_Indicator_WID` URL parameter from the CSV URL. As an example, if your CSV URL is `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_payslip_report?Period_Date_Indicator%21WID=e3e3e13f80904ee185eab1fbf331acef`, your period date indicator WID is `e3e3e13f80904ee185eab1fbf331acef`.

        **Important:** Your external content connector admin needs this period date indicator WID when configuring the Workday external content connector.


## What to do next

Provide the following items to the connector admin who creates your Workday external content connectors:

-   The base URL for your Workday tenant that you copied in step [10.a](configure-payslip-report-workday.md#copy-base-url-step).
-   The Workday tenant name that you copied in step [10.b](configure-payslip-report-workday.md#copy-tenant-name-step).
-   The custom payslip report owner's user name that you copied in step [10.c](configure-payslip-report-workday.md#copy-report-owner-user-name-step).
-   The custom payslip report's name alias that you copied in step [10.d](configure-payslip-report-workday.md#copy-report-name-alias-step).
-   The period date indicator WID \(Workday ID\) that you copied in step [10.e](configure-payslip-report-workday.md#copy-period-indicator-wid-step).

Your connector admin needs these items to configure a Workday external content connector to retrieve searchable content and metadata from payroll information in your Workday source system.

**Parent Topic:**[Workday external content connector](../concept/workday-external-content-connector.md)

