---
title: Properties installed to configure expiry notifications
description: There are several properties related to Contracts Core that can be used to configure the number of days before which expiry notification should be sent and the generation of audit certificate.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2025-07-31"
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
</table>**Parent Topic:**[Contract Management Pro reference](../concept/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro](cncore-comp-ccore.md)

[Components installed with Contract Workspace](cncore-comp-contract-workspace.md)

[Components installed with Analytics Pack for Contract Management Pro](cncore-comp-analytics-pack-cmpro.md)

[Contract request State and Contract document status in Contract Management Pro](cncore-cr-state-status.md)

[Clause Variation form](cncore-cv-form.md)

[Contract Configuration form](cncore-contract-config-form.md)

[Properties installed to configure contracts integrations](cncore-properties.md)

[Expiring Contracts Condition form fields](cncore-email-notif-expcont-form.md)

[Action assignment form](cmpro-actn-assignment-form.md)

[UFX Add on Event mapping form](cmpro-ufx-event-map-form.md)

[Obligation form](cncore-obligation-form.md)

[Obligation Management notifications](cncore-ob-mgmt-notification.md)

[Contract Management Pro glossary](../concept/contract-management-pro-glossary.md#)

[Contract Management solutions](cmpro-cml-feature-compare.md)

