---
title: Enable users to view email details in activity stream
description: As a contract configurator, enable users to view email details in the activity stream of contract requests.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [glide.ui.activity.email\_roles, system properties]
breadcrumb: [Configure additional features in CM Pro, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Enable users to view email details in activity stream

As a contract configurator, enable users to view email details in the activity stream of contract requests.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Add the roles to the property.

<table id="choicetable_iwz_dg4_d1c"><thead><tr><th align="left" id="d212138e58">

Method

</th><th align="left" id="d212138e61">

Steps

</th></tr></thead><tbody><tr><td id="d212138e67">

**Add role using user interface \(UI\)**

</td><td>

-   Navigate to **All** &gt; **System Properties** &gt; **UI Properties** your workspace.
-   In the **Roles that can view email in the Activity formatter when including "Sent/Received Emails"** property field, add roles for which you want to enable viewing of sent email details in the activity stream. Use comma separator while adding additional roles.

For example, to enable contract fulfillers to view email details in the activity stream, add `sn_cm_core.contract_fulfiller`.

-   Select **Save**.


</td></tr><tr><td id="d212138e112">

**Add role to the system property**

</td><td>

-   In the filter navigator, enter `sys_properties.list`
-   In the **Name** column, search for the `glide.ui.activity.email_roles` property.
-   Select the property.
-   In the **Value** field, add roles for which you want to enable viewing of email details in the activity stream. Use comma separator while adding additional roles.

For example, to enable contract fulfillers to view email details in the activity stream, add `sn_cm_core.contract_fulfiller`.

-   Select **Update**.


</td></tr></tbody>
</table>
**Parent Topic:**[Configure additional features in Contract Management Pro](../concept/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace with UI Builder components](../concept/cncore-conf-cntrct-wrkspc.md)

[Configure signature pause duration when modifying signatories](cncore-pause-sig-property.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Enable keyword search for contract templates](cncore-enable-search-cont-tmplts.md)

[Configuring contract summarization for Contract Management Pro](cmpro-conf-cntr-summary.md)

[Configure conditions to send reminder notifications for expiring contracts](cncore-config-rem-exp-cont.md)

[Copy fields from parent request to amendment request](cncore-cpy-fld-parent-amedreq.md)

[Manage notifications in Contract Management Pro](../concept/cmpro-manage-notifications.md)

