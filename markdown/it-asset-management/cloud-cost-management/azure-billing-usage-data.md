---
title: Set up access to Microsoft Azure billing and usage data
description: Set up access to Microsoft Azure billing and usage data depending on your agreement type.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Cloud Cost Management for Microsoft Azure, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Set up access to Microsoft Azure billing and usage data

Set up access to Microsoft Azure billing and usage data depending on your agreement type.

You can access the billing and usage data, by assigning an appropriate role to the Microsoft Azure service principal, depending on whether you have an Enterprise Agreement \(EA\) or Microsoft Customer Agreement \(MCA\). Accordingly, some of the following steps might be optional for you.

**Important:** The support for MCA accounts is available from Cloud Cost Management version 9.0 and later.

1.  [Create a Microsoft Azure service principal](../task/create-ms-azure-service-principal.md)
2.  For EA accounts - [Add the Enrollment Reader role to the Microsoft Azure service principal](../task/add-enrollment-reader-ms-azure.md)
3.  For MCA accounts - [Add the Billing Profile Reader role to the Microsoft Azure service principal](../task/add-billing-profile-reader-azure.md)
4.  [Create a record of Microsoft Azure credentials in Cloud Cost Management](../task/create-azure-credential-record-ccm.md)
5.  [Schedule and manage the jobs that download Azure billing data](../task/schedule-azure-billing-job.md)

**Related topics**  


[Create exports on the Azure portal](../task/create-azure-exports.md)

[Cancel an Azure Billing download job in Cloud Cost Management](../task/azure-bill-dwnld-cancl-cloudin.md)

