---
title: Properties installed to configure contracts integrations
description: There are several properties that you can use to configure integrations for Contract Management Pro.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-properties.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
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
</table>**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro]()

[Components installed with Contract Workspace]()

[Components installed with Analytics Pack for Contract Management Pro]()

[Contract request State and Contract document status in Contract Management Pro]()

[Clause Variation form]()

[Contract Configuration form]()

[Properties installed to configure expiry notifications]()

[Expiring Contracts Condition form fields]()

[Action assignment form]()

[UFX Add on Event mapping form]()

[Obligation form]()

[Obligation Management notifications]()

[Contract Management Pro glossary]()

[Contract Management solutions]()

