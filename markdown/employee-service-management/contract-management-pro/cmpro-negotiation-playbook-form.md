---
title: Contract Analysis Playbook form
description: Fields on the Contract Analysis Playbook form define the negotiation guidance for a contract type and the conditions that determine when an external AI tool retrieves it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-negotiation-playbook-form.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-08-18"
reading_time_minutes: 3
keywords: [Contract analysis playbook, Playbook fields, reference, Contract negotiation]
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract Analysis Playbook form

Fields on the Contract Analysis Playbook form define the negotiation guidance for a contract type and the conditions that determine when an external AI tool retrieves it.

## Contract Analysis Playbook form

The fields on the Contract Analysis Playbook form are described in the following table.

|Field|Description|
|-----|-----------|
|Name|Unique name of the playbook.|
|Description|Summary of the guidance that the playbook provides.|
|Application|This field is automatically set per the application scope setting.|
|Request table|Table that the conditions apply to, such as Contract request table \[sn\_cm\_core\_contract\_request\]. The conditions in the **Conditions** field are built against the fields of this table.|
|Order|Value that sets the priority of the playbook within a contract type. When more than one active playbook matches a contract, the playbook with the lowest order value applies. The value must be unique for the contract type.|
|Contract type|Contract type that the playbook applies to. Only active contract types are available.|
|Active|Option to make the playbook available to the playbook tool. When selected, an external AI tool can retrieve the playbook. When cleared, the playbook tool does not return the playbook.|
|Content source|Method used to provide the playbook content. Select **Upload file** to attach a document, or **Enter manually** to type the content.|
|Document|Attached file that contains the playbook content. Supported formats are PDF, Word, Excel, PowerPoint, and Markdown, with a maximum file size of 800 KB. Use the **Update** or **Delete** option to replace or remove the file. This field appears only when **Upload file** is selected in the **Content source** field.|
|Conditions|Conditions that determine when the playbook applies, built against the fields of the selected request table. When the conditions are empty, the playbook applies to all contracts of the contract type.|
|Playbook content|Contract analysis guidance entered directly on the form. This field appears only when **Enter manually** is selected in the **Content source** field.|

**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro]()

[Components installed with Contract Workspace]()

[Components installed with Analytics Pack for Contract Management Pro]()

[Contract request State and Contract document status in Contract Management Pro]()

[Signatory roles]()

[Clause Variation form]()

[Contract Configuration form]()

[Properties installed to configure expiry notifications]()

[Properties installed to configure contracts integrations]()

[Expiring Contracts Condition form fields]()

[Action assignment form]()

[UFX Add on Event mapping form]()

[Obligation form]()

[Obligation Management notifications]()

[Contract analysis playbook tool messages]()

[Contract Management Pro glossary]()

[Contract Management solutions]()

