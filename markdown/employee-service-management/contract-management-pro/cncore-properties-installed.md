---
title: Properties installed to configure expiry notifications
description: There are several properties related to Contracts Core that can be used to configure the number of days before which expiry notification should be sent and the generation of audit certificate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-properties-installed.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Properties installed to configure expiry notifications

There are several properties related to Contracts Core that can be used to configure the number of days before which expiry notification should be sent and the generation of audit certificate.

**Note:** These properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="table_ybm_p5w_qlb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cm\_core.contract\_expiring\_days

</td><td>

Indicates the number of days before which an expiry email notification is sent to the stakeholders.-   Type: Integer
-   Default value: 30

</td></tr><tr><td>

sn\_cm\_core.enable\_executed\_contract\_audit\_certificate

</td><td>

Specifies whether the user needs an audit certificate to accompany the signed contract.-   Type: true\|false
-   Default value: false

</td></tr></tbody>
</table>**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro]()

[Components installed with Contract Workspace]()

[Components installed with Analytics Pack for Contract Management Pro]()

[Contract request State and Contract document status in Contract Management Pro]()

[Clause Variation form]()

[Contract Configuration form]()

[Properties installed to configure contracts integrations]()

[Expiring Contracts Condition form fields]()

[Action assignment form]()

[UFX Add on Event mapping form]()

[Obligation form]()

[Obligation Management notifications]()

[Contract Management Pro glossary]()

[Contract Management solutions]()

