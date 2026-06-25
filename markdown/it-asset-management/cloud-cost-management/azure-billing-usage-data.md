---
title: Set up access to Microsoft Azure billing and usage data
description: Set up access to Microsoft Azure billing and usage data depending on your agreement type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/azure-billing-usage-data.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Cloud Cost Management for Microsoft Azure, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Set up access to Microsoft Azure billing and usage data

Set up access to Microsoft Azure billing and usage data depending on your agreement type.

You can access the billing and usage data, by assigning an appropriate role to the Microsoft Azure service principal, depending on your agreement type: Enterprise Agreement \(EA\), Microsoft Customer Agreement \(MCA\), or Microsoft Partner Agreement \(MPA\). Accordingly, some of the following steps might be optional for you.

1.  [Create a Microsoft Azure service principal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/create-ms-azure-service-principal.md)
2.  For EA accounts - [Add the Enrollment Reader role to the Microsoft Azure service principal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/add-enrollment-reader-ms-azure.md)
3.  For MCA accounts - [Add the Billing Profile Reader role to the Microsoft Azure service principal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/add-billing-profile-reader-azure.md)
4.  [Create a record of Microsoft Azure credentials in Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/create-azure-credential-record-ccm.md)
5.  [Schedule and manage the jobs that download Azure billing data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/schedule-azure-billing-job.md)

**Related topics**  


[Create exports on the Azure portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/create-azure-exports.md)

[Cancel an Azure Billing download job in Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/azure-bill-dwnld-cancl-cloudin.md)

