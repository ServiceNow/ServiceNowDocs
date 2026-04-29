---
title: Components installed with Major Issue Management
description: Several types of components are installed with the major issue management feature.Major Issue Management provides these roles.Major Issue Management provides these properties.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Major issue management overview, Administer, Customer Service Management]
---

# Components installed with Major Issue Management

Several types of components are installed with the major issue management feature.

## Roles installed with Major Issue Management

Major Issue Management provides these roles.

<table id="table_h4s_m35_ndb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

Major issue manager\[sn\_majorissue\_mgt.major\_issue\_manager\]

</td><td>

Users with this role can:-   Create major cases
-   Approve or reject major case candidates
-   Add or remove child cases from major cases
-   Add or remove impacted accounts \(B2B\) or consumers \(B2C\)

 The customer service manager role \[sn\_customerservice\_manager\] contains the major issue manager role.

</td><td>

-   sn\_customerservice\_agent
-   sn\_customerservice\_consumer\_agent
-   sn\_publications\_recipients\_user
-   sn\_publications\_recipients\_list\_user

</td></tr></tbody>
</table>## Properties installed with Major Issue Management

Major Issue Management provides these properties.

To access these properties, navigate to **Customer Service** &gt; **Administration** &gt; **Properties**.

**Note:** To open the System Property \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_rr5_fk5_ndb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Synchronize fields from parent to child casesn\_customerservice.parent\_child\_case\_sync

</td><td>

Enable this property to synchronize fields from a major, or parent, case to the associated child cases. -   Type: true\|false
-   Default value: false
-   Location: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Comma-separated list of fields that synchronize from parent case to child casessn\_customerservice.case\_fields\_to\_sync

</td><td>

Specifies the list of fields to synchronize from the major, or parent, case to the associated child cases. -   Type: string
-   Default value: priority,state,comments,work\_notes,assigned\_to,close\_notes,resolution\_code
-   Location: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Processes SLA asynchronously during parent to child case creation and synchronizationsn\_customerservice.parent\_child\_case\_sla\_async

</td><td>

Enables major issue management to process the SLA asynchronously during child case creation and parent-to-child case synchronization. -   Type: true\|false
-   Default value: true
-   Location: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Enable case type support for major cases

 enable\_case\_type\_for\_major\_case

</td><td>

Enable this property to create major cases with the same case type as the candidate case. When enabled, the system preserves the sys\_class\_name of the candidate case when creating the major case and uses extension point implementations to determine fields to copy.

 -   Type: true\|false
-   Default value: true \(new installations\), false \(upgrades\)
-   Location: Go to **System Properties** and search for `enable_case_type_for_major_case`.

 **Note:** For upgrade installations, this property defaults to false to preserve existing behavior where all major cases are created as base cases. Before you enable case type support, determine whether the default implementation is sufficient, or whether you need extension point implementations for your custom case types.

</td></tr></tbody>
</table>