---
title: ServiceNow Vault for HR Service Delivery
description: Classify sensitive employee data and enable employees/former employees to request deletion of personal data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/vault-hr-service-delivery.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# ServiceNow Vault for HR Service Delivery

Classify sensitive employee data and enable employees/former employees to request deletion of personal data.

## Classify HR records

ServiceNow Vault for HR introduces the new classification HR PII to enable HR professionals to identify and manage sensitive employee data. The HR PII categorizes data from HR applications, with categories such as contact information, tax-related information, and visa-related information. The categories are organized under two parent data classifications: Master data PII and Transactional Data PII.

The classification HR PII and the data classifications are included out-of-the-box. \[Omitted image "vault-classification.png"\] Alt text: HR PII has two parent data classifications, each with several child classifications To create additional data classifications under HR PII, see [Creating data classifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/data-classification/create-data-classification-codes.md).

Each data classification category contains a “Classified Dictionary Entries” related list, which displays the HR application-specific tables and columns included in the classification. The ServiceNow Vault for HR demo data provides classified dictionary entries. \[Omitted image "vault-dict.png"\] Alt text: The example contact information classification has columns such as address, work phone, and email

To add columns from an HR application to the classified dictionary entries list, see [Classify HR data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/classify-hr-data.md).

## Employees request data deletion

ServiceNow Vault for HR provides the interface elements and backend process to enable employees and former employees to request deletion of their personal data.

Employees can submit a request to erase personal identifiable data or an HR case associated with their employee record through the **Erasure of personal data** catalog item, available in the **Employee Center** &gt; **Human Resources** section.

Former employees can submit the request through **Alumni Service Center** &gt; **Services** &gt; **Erasure of personal data**.

\[Omitted image "vault-delete-data.png"\] Alt text: Erasure of personal data request catalog item has a field to specify the data for deletion and a field to select HR cases for deletionFor instructions on modifying the fields in the Erasure of Personal Data Request including the target user who receives the HR case, see [Edit the HR case template for an HR catalog item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/edit-hr-case-template-for-hr-catalog-item.md).

-   **[Setting up ServiceNow Vault for HR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/install-vault-hr.md)**  
You can install ServiceNow Vault for HR if you have the admin role. The application includes demo data and installs related ServiceNow applications and plugins if they are not already installed.
-   **[Classify HR data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/classify-hr-data.md)**  
Assign data classifications to HR application-specific table columns in the Dictionary \[sys\_dictionary\] table. The assigned columns will appear in the “Classified Dictionary Entries” related list for a data classification.

**Parent Topic:**[Integration of HR Service Delivery with ServiceNow applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/integrate-hr-platform-apps.md)

