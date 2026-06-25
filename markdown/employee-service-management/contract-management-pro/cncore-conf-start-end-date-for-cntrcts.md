---
title: Auto-populate the start date and end date for contract requests
description: Configure an extension point implementation to automatically add the start date and end date while creating a contract request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-conf-start-end-date-for-cntrcts.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Auto-populate dates in contract]
breadcrumb: [Configure additional features in CM Pro, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Auto-populate the start date and end date for contract requests

Configure an extension point implementation to automatically add the start date and end date while creating a contract request.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** field, enter `sn_cm_core.ContractManagementExt`.

3.  Select the record.

4.  In the Related Links section, select **Create implementation**.

5.  On the Script Include form, fill in the fields.

    \[Omitted image "cmpro-extension-point.png"\] Alt text: Extension point to add scripts.

    For a description of the field values, see [Scripted Extension Point form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/scripted-extension-point-form-fields.md).

6.  In the **Script** field, add a method `populateDataForInitiateContractModal` to define the fields from which the values will be automatically added in the **Start date** and **End date** fields of a contract request.

    You can also define the exact dates for the **Start date** and **End date**.

7.  Select **Update**.


## Result

The **Start date** and **End date** fields in the Initial contract window are automatically updated from the parent record while creating a contract request.

For more information on initiating a contract request, see [Initiating a contract or amendment request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-initiate-contract.md).

**Parent Topic:**[Configure additional features in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace]()

[Configure signature pause duration when modifying signatories]()

[Activate a system property to generate a certificate of completion]()

[Enable users to view email details in activity stream]()

[Enable keyword search for contract templates]()

[Configuring contract summarization for Contract Management Pro]()

[Configure conditions to send reminder notifications for expiring contracts]()

[Copy fields from parent request to amendment request]()

[Manage notifications in Contract Management Pro]()

