---
title: Create exports on the Azure portal
description: Create exports for your Azure service account to download Azure billing data.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up access to Microsoft Azure billing and usage data, Configure Cloud Cost Management for Microsoft Azure, Configure, Cloud Cost Management, IT Asset Management]
---

# Create exports on the Azure portal

Create exports for your Azure service account to download Azure billing data.

## Before you begin

Roles required:

-   For Enterprise Agreement \(EA\): Enterprise administrator, Storage Account Contributor
-   For Microsoft Customer Agreement \(MCA\): Billing account owner or contributor, Storage Account Contributor
-   For Subscriptions \(EA/MCA/MPA\): contributor, Storage Account Contributor

## About this task

When you're using the Azure Export method to download billing data, you must create an export for your service account on the Azure portal to export billing data to your ServiceNow storage account.

Cloud Cost Management 10.0 and later versions support the FOCUS billing format in addition to the Cloud Native billing format. You must create exports for your Azure service account with the appropriate cost template.

## Procedure

1.  Log in to the [Azure portal](https://portal.azure.com) and search for **Cost Management**.

2.  Select a billing account scope.

3.  Select **Exports**.

4.  Select **+ Create**.

5.  On the Basics tab, select one of the following templates.

    -   For the Cloud Native billing format, create exports with the **Cost and usage \(actual\)** and **Cost and usage \(amortized\)** templates to ensure accuracy of billing data.
    -   For the FOCUS billing format, create exports with the **Cost and usage \(FOCUS\)** to ensure efficient billing data management.
    ![Cost Management page on Microsoft Azure portal showing templates for various billing formats](../image/focus-billing-azure.png)

6.  Select **Next**.

7.  On the Datasets tab, enter **Export prefix** to customize your export name.

8.  Select the edit icon ![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png) next to the export name that you want to edit.

9.  In the Edit export window, fill in the fields.

<table id="table_lzj_sgs_nfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type of data

</td><td>

The type of billing data for the export.

</td></tr><tr><td>

Export name

</td><td>

A unique name for the export.

</td></tr><tr><td>

Dataset version

</td><td>

The version of the dataset.**Note:** Because other dataset versions might have different requirements, you should select **2024-08-01** as the dataset version.

</td></tr><tr><td>

Frequency

</td><td>

The option to export data at an interval that meets your requirement. Select **Daily export of month-to-date costs** for the daily export of your data.

**Important:** The Billing Download job must run at least 30–60 minutes after the export of billing data to ensure that the latest data is included in the download.

</td></tr><tr><td>

Compression

</td><td>

Mode of compressing the export data.You can select **None** or **Zip** depending on your preference.

</td></tr><tr><td>

Export description

</td><td>

A brief description of the export.

</td></tr></tbody>
</table>10. Select **Next**.

11. On the Destination tab, select the field values that meet your requirement.

    **Note:** Select **CSV** in the **Format** field because Cloud Cost Management 9.0 and later versions currently supports the CSV format only. The **Overwrite data** check box should be cleared so that the previously downloaded data doesn't get overwritten with the latest downloads.

12. Select **Next**.

13. On the Review + create tab, review your export configuration and change if necessary.


## Result

The export that you have created appears in the list of exports.

**Related topics**  


[Schedule and manage the jobs that download Azure billing data](schedule-azure-billing-job.md)

