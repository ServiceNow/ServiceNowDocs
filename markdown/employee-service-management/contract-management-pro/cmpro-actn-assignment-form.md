---
title: Action assignment form
description: Learn about the fields of the Action Assignment form. Use this form to add the New action button to your workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-actn-assignment-form.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Action assignment form

Learn about the fields of the Action Assignment form. Use this form to add the New action button to your workspace.

Use the action assignment form to define a action button in your workspace and map it to the built-in action that initiates a contract request. For more information, see [Add a workspace action button for initiating a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-config-initiate-cont.md).

|Field|Description|
|-----|-----------|
|Action label|Label that appears on the button created through the action. For example: Initiate Contract|
|Action name|Name for your action that appears in the action assignment list. For example, `initiate_contract`.|
|Application|Application of the workspace for which the action is added. Example: To add action to Source-to-Pay workspace, select Source-to-Pay Workspace.|
|Table|Application table to which the action will be associated to. Example: To associate action to the Sourtable that stores requests to source for supplier products, select Sourcing Request \[sn\_shop\_sourcing\_activity\]|
|View|View of the form on which the action button is displayed.|
|Enable for all Configurable Experience|Determines whether the action should appear in all experiences or only in specified experiences. If true, the action appears in any applicable form regardless of experience.|
|Active|Option to activate the action.|
|Order|Integer that determines the precedence of this action in relation to matching actions with the same name. The lower the number, the more likely it is to be selected against other actions. This ordering enables you to override other actions with your own.|
|Tooltip|Text that displays when agents point their cursor over the button.|
|Description|Description for the action that's displayed in the Action Assignments list.|

**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro]()

[Components installed with Contract Workspace]()

[Components installed with Analytics Pack for Contract Management Pro]()

[Contract request State and Contract document status in Contract Management Pro]()

[Clause Variation form]()

[Contract Configuration form]()

[Properties installed to configure expiry notifications]()

[Properties installed to configure contracts integrations]()

[Expiring Contracts Condition form fields]()

[UFX Add on Event mapping form]()

[Obligation form]()

[Obligation Management notifications]()

[Contract Management Pro glossary]()

[Contract Management solutions]()

