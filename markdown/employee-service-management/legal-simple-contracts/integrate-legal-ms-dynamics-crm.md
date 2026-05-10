---
title: Configure Microsoft Dynamics CRM for sales contracts
description: Configure Microsoft Dynamics CRM to import the sales representatives, sales accounts, and active opportunities data into the tables in the ServiceNow instance for the sales contracts support.
locale: en-US
release: australia
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure Microsoft Dynamics CRM for sales contracts

Configure Microsoft Dynamics CRM to import the sales representatives, sales accounts, and active opportunities data into the tables in the ServiceNow instance for the sales contracts support.

## Before you begin

Ensure that the administrator has installed and set up spokes for the CRM app you want to configure.

-   **[Microsoft Dynamics CRM spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/microsoft-dynamics-crm-spoke.md) v1.3.0 or later version**

    For more information on the setup and creating the Microsoft Dynamics CRM account, see [Set up Microsoft Dynamics CRM spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-ms-dynamics-crm.md).


Role required: sn\_lg\_ops.request\_config, sn\_lg\_contracts.contracts\_config, or sn\_lg\_matter.matter\_config

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Legal Integrations** &gt; **Integrations**.

2.  Create or modify an external app configuration.

    -   To create an external app configuration, click **New**.
    -   To modify an existing external app configuration, open the external app configuration from the list.
3.  On the Integration Type page, click the **CRM** link.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the CRM app configuration.|
    |Description|Description of the CRM app configuration.|
    |Active|Option for marking the configuration for CRM app configuration as active.|
    |Table|Table in which the information about sales contracts is stored.|
    |Condition|Filter conditions to determine which CRM app configuration to use.|
    |Execution order|Order in which a CRM app is used for creating contract documents. The system with the lower-order value is chosen first.|
    |App|CRM app such as Microsoft Dynamics CRM.|

5.  Save the external app configuration.

    -   Save a new external app configuration by clicking **Submit**.
    -   Save the changes to an existing external app configuration by clicking **Update**.
6.  Click **Publish**.


## Result

The configuration for the Microsoft Dynamics CRM app is published and is ready to be used in sales contract review requests.

## What to do next

-   [Schedule import set jobs to pull data from the CRM system](schedule-import-sales-contract-crm.md)
-   [Create a deflection rule for sales contracts](create-contract-deflection-rule.md)

