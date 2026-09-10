---
title: Case exclusion reference fields
description: The Case Exclusion Rule table stores the rules that determine when Invoice Case Management ignores an inbound email instead of creating an invoice inquiry case. This reference describes the table, its fields, and who can manage it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/case-exclusion-reference-fields.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-08-27"
reading_time_minutes: 2
breadcrumb: [Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Case exclusion reference fields

The Case Exclusion Rule table stores the rules that determine when Invoice Case Management ignores an inbound email instead of creating an invoice inquiry case. This reference describes the table, its fields, and who can manage it.

Case exclusion rules are stored in the Case Exclusion Rule table \(`sn_spend_sdc_case_exclusion_rule`\), which is built on the Common Service Delivery application by extending the S2P Custom Configuration table \(`sn_fin_s2p_custom_config`\). Rule records use the **Case Exclusion Rule Config** configuration type.

## Case Exclusion Rule table fields

|Field|Description|Type|
|-----|-----------|----|
|**Rule ID**|Unique identifier generated automatically for each rule.|Auto-updated|
|**Name**|Name of the case exclusion rule.|String|
|**Rule Applies To**|Case type that the rule applies to. Currently, **Invoice Inquiry Case**.|Choice|
|**Order**|Controls the execution precedence of rules, from lowest to highest number.|Integer|
|**Active**|Indicates whether the rule is in effect.|True/False|
|**Conditions**|Condition builder that defines which inbound emails the rule matches. Available fields are Body Text, Keywords, Recipients, Subject, User, and User ID.|Conditions|

**Parent Topic:**[Accounts Payable Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/acc-pay-reference.md)

**Related topics**  


[Accounts Payable Operations properties]()

[Create New Invoice Line form]()

[Create invoice cost allocation form]()

[Outbound cost allocation staging table]()

[Distribution set form]()

[Create New Invoice case form]()

[Create New Invoice task form]()

[Invoice processing case form]()

[Tax lines]()

[Invoice exception form]()

[Request Help form]()

[Data required for invoice processing]()

[Invoice exception definition form]()

[Approval Rule form]()

[Approval Plan form]()

[Jurisdictions main table]()

[Accounts Payable Operations glossary]()

