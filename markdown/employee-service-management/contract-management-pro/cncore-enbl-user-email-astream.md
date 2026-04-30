---
title: Enable users to view email details in activity stream
description: As a contract configurator, specify the user roles to enable users to view email details in the activity stream of contract requests.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [glide.ui.activity.email\_roles, system properties, Configure user roles, View email details]
breadcrumb: [Configure additional features in CM Pro, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Enable users to view email details in activity stream

As a contract configurator, specify the user roles to enable users to view email details in the activity stream of contract requests.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Specify the user roles for a user.

    -   Add role using user interface \(UI\).
        1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.
        2.  In the **Roles that can view email in the Activity formatter when including "Sent/Received Emails"** property field, add roles for which you want to enable viewing of sent email details in the activity stream. Use comma separator while adding additional roles.

            For example, to enable contract fulfillers to view email details in the activity stream, add `sn_cm_core.contract_fulfiller`.

            ![Add roles in system properties using the UI](../image/cmpro-add-role-ui.png "Customize properties")

        3.  Select **Save**.
    -   Add role to the system property.
        1.  Select the **All** menu.
        2.  In the search bar, enter `sys_properties.list`.
        3.  In the **Name** column, search for the `glide.ui.activity.email_roles` property.
        4.  In the **Value** field, add roles for which you want to enable viewing of email details in the activity stream. Use comma separator while adding additional roles.

            For example, to enable contract fulfillers to view email details in the activity stream, add `sn_cm_core.contract_fulfiller`.

            ![Add roles using system properties](../image/cmpro-sys-prop-role.png "Customize system properties")

        5.  Select **Update**.

## Result

The users with the assigned role that has been added to the system property can view email details in the activity stream of a contract request.

**Parent Topic:**[Configure additional features in Contract Management Pro](../concept/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace](../concept/cncore-conf-cntrct-wrkspc.md)

[Configure signature pause duration when modifying signatories](cncore-pause-sig-property.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Enable keyword search for contract templates](cncore-enable-search-cont-tmplts.md)

[Configuring contract summarization for Contract Management Pro](cmpro-conf-cntr-summary.md)

[Configure conditions to send reminder notifications for expiring contracts](cncore-config-rem-exp-cont.md)

[Copy fields from parent request to amendment request](cncore-cpy-fld-parent-amedreq.md)

[Manage notifications in Contract Management Pro](../concept/cmpro-manage-notifications.md)

