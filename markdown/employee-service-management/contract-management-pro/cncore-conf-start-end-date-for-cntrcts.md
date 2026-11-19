---
title: Auto-populate the start date and end date for contract requests
description: Configure an extension point implementation to automatically add the start date and end date while creating a contract request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/cncore-conf-start-end-date-for-cntrcts.html
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure additional features in CM Pro, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
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

    For a description of the field values, see [Scripted Extension Point form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/legal-request-management/scripted-extension-point-form-fields.md).

6.  In the **Script** field, add a method `populateDataForInitiateContractModal` to define the fields from which the values will be automatically added in the **Start date** and **End date** fields of a contract request.

    You can also define the exact dates for the **Start date** and **End date**.

7.  Select **Update**.


**Parent Topic:**[Configure additional features in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace with UI Builder components]()

[Configure signature pause duration when modifying signatories]()

[Activate a system property to generate a certificate of completion]()

[Enable users to view email details in activity stream]()

[Enable keyword search for contract templates]()

[Configuring contract summarization for Contract Management Pro]()

[Configure conditions to send reminder notifications for expiring contracts]()

[Copy fields from parent request to amendment request]()

[Manage notifications in Contract Management Pro]()

