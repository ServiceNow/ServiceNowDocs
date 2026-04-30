---
title: Configure Azure Credentials for Cloud License Estimator
description: To use this tool, configure the Azure Service Principal Account credentials. If you already have credentials configured in the ServiceNow instance, those credentials can be used.The tool supports management accounts and single subscriptions. Management accounts include all subscriptions under that account.
locale: en-US
release: zurich
product: Cloud License Estimator
classification: cloud-license-estimator
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Cloud License Estimator, Cloud License Estimator, ITOM Visibility, IT Operations Management]
---

# Configure Azure Credentials for Cloud License Estimator

To use this tool, configure the Azure Service Principal Account credentials. If you already have credentials configured in the ServiceNow instance, those credentials can be used.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Filter Navigation** &gt; **All** &gt; **ITOM Cloud License Estimator** &gt; **Home**.

2.  On the Home Page, select **Go to Credentials** to open the **Credentials \(discovery\_credentials\)** page.

3.  Select **New** &gt; **Azure Service Principal** and enter the Azure Service Principal Account details.


## Result

A **Credential ID** is generated, which is required when creating configurations.

**Parent Topic:**[Configure Cloud License Estimator](../Concept/configure-cloud-license-estimator.md)

**Related topics**  


[Configure Amazon Web Service Credentials for Cloud License Estimator](cle-aws-credential-setup.md#)

## Create Azure Account Configuration and generate CLE reports

The tool supports management accounts and single subscriptions. Management accounts include all subscriptions under that account.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Filter Navigation** &gt; **All** &gt; **ITOM Cloud License Estimator** &gt; **Home**.

2.  On the Home page, select **Create Configuration** to open the Create Configuration pop-up.

3.  Enter the following details:

    -   **Name**: Enter a name for the configuration.
    -   **Cloud Provider**: Choose **Azure** from the list. Fill in the additional fields appear.
    -   **Account ID**: Enter the management account ID or subscription ID.
    -   **Management group**: Select this checkbox if the Account ID is a management account.
    -   **Credentials**: Select the Azure Service principle credentials configured in [Configure Azure Credentials for Cloud License Estimator](cle-azure-credential-setup.md#).
    -   **Activate**: Enable this option.
4.  Select **Save and run license estimator**.

    The configuration is saved and the tool generates the report. You are redirected to the **Report** page where the status of the report generation can be tracked.

5.  From the **Report** page, select **Download resource report** to download a PDF of the report.


**Related topics**  


[Generate Cloud License Estimator Reports](../Concept/cle-generate-reports.md)

