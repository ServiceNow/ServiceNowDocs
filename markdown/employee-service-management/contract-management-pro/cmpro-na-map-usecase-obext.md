---
title: Map a use case for contract obligation extraction
description: Map a use case to specific tables, and define conditions to apply the use case for obligation extraction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-na-map-usecase-obext.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 2
keywords: [Obligation extraction use case mapping]
breadcrumb: [Configure obligation extraction, Configure, ServiceNow Otto for Contract Management Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Map a use case for contract obligation extraction

Map a use case to specific tables, and define conditions to apply the use case for obligation extraction.

## Before you begin

Ensure that the application scope is in the Global or ServiceNow Otto for Contract Management Pro scope. If you’re configuring the use case mapping in a different application scope, add the scoped ACL to the Use Case Mapping table \(sn\_cm\_gen\_ai\_usecase\_configuration\).

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **AI Admin Hub** to access the **AI Skills** tab of the AI Admin Hub console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  Select **Activate skill** on the skill you want to activate.

    \[Omitted image "cmpro-NA-skills.png"\] Alt text: AI skills available for Contract Management Pro.

4.  In the General details page, view the skill details and select **Save and continue**.

5.  In the Use case page, select **Save and continue**.

    For more information on creating a use case, see [Create use cases for contract obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-use-case-obext.md).

6.  In the Use case mappings page, select **New**.

7.  On the form, fill in the fields.

    For a description of the field values, see [Contract obligation extraction use case mapping form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-use-case-map-form-obe.md).

    \[Omitted image "cmpro-na-ob-map.png"\] Alt text: Create new use case mapping form to map obligations with request tables and repository tables.

8.  Select **Save**.


## Result

The use case is mapped to specific tables and conditions, and it’s applied for obligation extraction when the conditions are met.

## What to do next

[Activate business rules for the Manage contract repository agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/conf-repository-agentic-ai.md)

-   **[Contract obligation extraction use case mapping form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-use-case-map-form-obe.md)**  
Use the Create use case mapping form in the contract obligation extraction skill to map the use case to specific tables and conditions.

**Parent Topic:**[Configuring contract obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-conf-obligation-extraction.md)

**Related topics**  


[Create use cases for contract obligation extraction]()

[Create use cases for contract obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-use-case-obext.md)

