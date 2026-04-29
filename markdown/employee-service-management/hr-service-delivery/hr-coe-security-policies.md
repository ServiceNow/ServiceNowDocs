---
title: Configuring HR Service Delivery Center of Excellence \(COE\) security policies
description: Use COE Access Control List \(ACLs\) Configuration to allow specific groups read or write access to HR cases under a specific COE.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HR service categorization, HR Centers of Excellence data model, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configuring HR Service Delivery Center of Excellence \(COE\) security policies

Use COE Access Control List \(ACLs\) Configuration to allow specific groups read or write access to HR cases under a specific COE.

For example, you don't want the Benefits group to view the cases created by the Compensation group. You create a COE security policy that allows the Compensation group access. Groups that aren't included on the policy cannot access the cases.

Use this feature as an alternative to using ACLs rules. For more information on ACLs, see [Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=australia&pubname=australia-platform-security&ft:locale=en-US).

COE security policies don't affect case creation. COE security policies affect what cases you can view or modify after creation.

You can still reclassify \(transfer\) HR cases from one HR service to another. Depending on the security policy, you might not be able to view the case after reclassification.

COE ACL Configuration uses the COE Security Policy \[sn\_hr\_core\_coe\_security\_policy\] table to determine access to the extended HR case tables \(COEs\).

The \* next to a table indicates it was deprecated for customers taking the Rome release to support a new data model. Existing customers using the legacy COEs and tables are not affected. These tables have been replaced by the Employee Relations feature. For more information, see [Employee Relations](hr-case-employee-relations.md).

The tables you can provide security for are:

|Label|Name|
|-----|----|
|HR Benefits Case|sn\_hr\_core\_case\_benefits|
|HR Compensation Case|sn\_hr\_core\_case\_compensation|
|HR Corporate Communications Case|sn\_hr\_core\_case\_corporate\_communcations|
|\*HR Employee Relations Case|sn\_hr\_core\_case\_relations|
|\*HR Ethics Case|sn\_hr\_core\_case\_ethics|
|HR Global Mobility Case|sn\_hr\_core\_case\_global\_mobility|
|HR Payroll Case|sn\_hr\_core\_case\_payroll|
|\*HR Performance Case|sn\_hr\_core\_case\_performance|
|HR Talent Management Case|sn\_hr\_core\_case\_talent\_management|
|HR Total Rewards Case|sn\_hr\_core\_case\_total\_rewards|
|HR Workforce Administration Case|sn\_hr\_core\_case\_workforce\_admin|
|HRIT Operations Case|sn\_hr\_core\_case\_operations|
|HR Lifecycle Events Case|sn\_hr\_le\_case|

**Note:** You can also provide security to any case table you extend.

To define security for a COE:

-   Choose all or specific HR services that fall under a COE.

    **Note:** When you select specific HR services for a COE, the unselected HR services are accessible by the case reader.

-   Determine what groups have read or write access to HR services under a COE.
-   Create conditions to filter the records that apply to your security policy.

    **Note:** Condition builder is a powerful tool that filters specific actions on the COE. Use caution when using conditions on your security policy. It may also affect system performance.


**Parent Topic:**[HR service categorization](hr-service-categorization.md)

