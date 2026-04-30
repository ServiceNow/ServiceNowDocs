---
title: Enable users to view email details in activity stream
description: As a contract configurator, enable users to view email details in the activity stream of contract requests.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [glide.ui.activity.email\_roles, system properties]
breadcrumb: [Set up Contracts Core, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Enable users to view email details in activity stream

As a contract configurator, enable users to view email details in the activity stream of contract requests.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Add the roles to the property.

<table id="choicetable_iwz_dg4_d1c"><thead><tr><th align="left" id="d200854e58">

Method

</th><th align="left" id="d200854e61">

Steps

</th></tr></thead><tbody><tr><td id="d200854e67">

**Add role using user interface \(UI\)**

</td><td>

-   Navigate to **All** &gt; **System Properties** &gt; **UI Properties** your workspace.
-   In the **Roles that can view email in the Activity formatter when including "Sent/Received Emails"** property field, add roles for which you want to enable viewing of sent email details in the activity stream. Use comma separator while adding additional roles.

For example, to enable contract fulfillers to view email details in the activity stream, add `sn_cm_core.contract_fulfiller`.

-   Select **Save**.


</td></tr><tr><td id="d200854e112">

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
**Parent Topic:**[Set up Contracts Core](../concept/cncore-setup-cmpro.md)

**Related topics**  


[Create a contract type](cncore-create-contract-type.md)

[Create document template categories](cncore-create-doc-tmplt-cat.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Configure reminders for expiring contracts](cncore-config-rem-exp-cont.md)

[Configuring external applications for Contract Management Pro](../concept/cncore-set-ext-app-config.md)

[Configure extension point for notifications](cmpro-configure-action-extension-point-email-notification-admin.md)

[Use default email notifications](cmpro-send-receive-email-notification-admin.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

