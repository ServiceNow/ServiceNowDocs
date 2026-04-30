---
title: Properties installed to configure contracts integrations
description: There are several properties that you can use to configure integrations for Contract Management Pro.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Contract Management Pro reference, Contract Management Pro, Employee Service Management]
---

# Properties installed to configure contracts integrations

There are several properties that you can use to configure integrations for Contract Management Pro.

These properties are available for Contract Management Pro.

**Note:** To configure these properties, navigate to Navigate to **All** &gt; **Contracts Core** &gt; **Contract Integrations** &gt; **Properties**.

<table id="table_zpv_stv_b5b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

External Storage section

</td></tr><tr><td>

Maximum number of attempts before removing the permission records with errors

 sn\_cm\_core.external\_storage\_clear\_errored\_records\_after

</td><td>

The number of retries permitted before removing all errored permission entries from the job execution queue.

 -   Type: integer
-   Default value: 5

</td></tr><tr><td>

Maximum number of permission records to include in a job execution

 sn\_cm\_core.external\_storage\_job\_batch\_limit

</td><td>

The number of permission records that can be included in single job execution.

 -   Type: integer
-   Default value: 30

</td></tr><tr><td>

Time in minutes to retry permission records execution

 sn\_cm\_core.external\_storage\_apis\_retry\_after

</td><td>

The amount of time the system waits in minutes before retrying to execute permission records.

 -   Type: integer
-   Default value: 60

</td></tr><tr><td>

Maximum number of failed calls before marking the flow status as errored

 sn\_cm\_core.external\_storage\_mark\_flow\_status\_errored

</td><td>

The maximum number of failed job execution calls permitted before the flow status is marked as errored.

 -   Type: integer
-   Default value: 5

</td></tr><tr><td class="sub-head" colspan="2">

Electronic Signature section

</td></tr><tr><td>

Specifies whether the user needs audit certificate combined with the signed contract

 sn\_cm\_core.enable\_executed\_contract\_audit\_certificate

</td><td>

Generate a certificate of completion for electronically signed contracts.

</td></tr></tbody>
</table>**Parent Topic:**[Contract Management Pro reference](../concept/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro](cncore-comp-ccore.md)

[Components installed with Contract Workspace](cncore-comp-contract-workspace.md)

[Components installed with Analytics Pack for Contract Management Pro](cncore-comp-analytics-pack-cmpro.md)

[Contract request State and Contract document status in Contract Management Pro](cncore-cr-state-status.md)

[Clause Variation form](cncore-cv-form.md)

[Contract Configuration form](cncore-contract-config-form.md)

[Properties installed to configure expiry notifications](cncore-properties-installed.md)

[Expiring Contracts Condition form fields](cncore-email-notif-expcont-form.md)

[Action assignment form](cmpro-actn-assignment-form.md)

[UFX Add on Event mapping form](cmpro-ufx-event-map-form.md)

[Obligation form](cncore-obligation-form.md)

[Obligation Management notifications](cncore-ob-mgmt-notification.md)

[Contract Management Pro glossary](../concept/contract-management-pro-glossary.md#)

