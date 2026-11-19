---
title: Configuring CMDB Identification and Reconciliation
description: Configure the necessary rules for CMDB Identification and Reconciliation \(IRE\) to function effectively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/configuring-ire.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring CMDB Identification and Reconciliation

Configure the necessary rules for CMDB Identification and Reconciliation \(IRE\) to function effectively.

## Configuration overview

-   [Create identification rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_IdentificationRules.md)

    Identification rules are essential in correctly identifying CIs in the CMDB to prevent the creation of duplicate CIs. Effective identification rules help determine whether an incoming CI is added to the CMDB or used to update and existing CI.

-   [Create reconciliation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/r_ReconciliationRulesPrinciples.md)

    Static and dynamic reconciliation rules determine which discovery source is authorized to update which CI attributes. Reconciliation rules are important in preventing discovery sources from overwriting each other's updates to the same attribute values.

-   [Create data source rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/create-ire-data-source-rule.md)

    Data source rules prevent discovery sources from inserting new CIs for a specific class. Data source rules are useful in preventing untrusted discovery sources from creating new CIs while continuing to trust these discovery sources in updating existing CIs.

-   [Create dependent relationship rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_ServiceRulesMetadata.md)

    Dependent relationship rules define the dependency structure of the CI types and the relationship types in service definitions, which help in CI identification and in the construction of business service maps.


-   **[Identification rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_IdentificationRules.md)**  
The CMDB identification process relies on identification rules to uniquely identify CIs.
-   **[Reconciliation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/r_ReconciliationRulesPrinciples.md)**  
Reconciliation rules determine which discovery sources can update CI attributes.
-   **[Exclude classes from Dynamic IRE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/dynamic-ire-exclude-class.md)**  
Exclude specific classes, for which Dynamic IRE isn't beneficial, from Dynamic IRE. When a hierarchy branch \(such as the Hardware class branch\) is configured to use Dynamic IRE, you can configure specific classes within that branch, to be excluded from Dynamic IRE.
-   **[Configure CI reclassification during IRE processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_CIReclassification.md)**  
During the Identification and Reconciliation Engine \(IRE\) CI identification process, a CI might need to be reclassified to a different sys\_class\_name type. By default, CIs are reclassified automatically. If automatic reclassification is disabled, then the CI is not reclassified and the system generates a reclassification task for your review.
-   **[Create an IRE data source rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/create-ire-data-source-rule.md)**  
When using Identification and Reconciliation Engine \(IRE\), you can prevent a specific discovery \(data\) source from inserting new CIs for a specific class. Create IRE data source rules for discovery sources that you don't trust in creating CIs but continue to trust in updating those CIs that exist.
-   **[CMDB dependent relationship rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_ServiceRulesMetadata.md)**  
Service definitions consist of CI types and relationship types. Dependent relationship rules define the dependency structure of the CI types and the relationship types in these service definitions, helping in CI identification and in the construction of business service maps.

**Parent Topic:**[CMDB Identification and Reconciliation \(IRE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_CMDBIdentifyandReconcile.md)

