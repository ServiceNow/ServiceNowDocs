---
title: Roles installed with GRC: Approver Configurator
description: Various roles are installed with the activation of the GRC: Approver Configurator application.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use Approver Configurator for setting up approvals for setting up approvals, Common GRC features, Governance, Risk, and Compliance]
---

# Roles installed with GRC: Approver Configurator

Various roles are installed with the activation of the GRC: Approver Configurator application.

<table id="table_yg1_dmm_bxb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Approver Configurator admin \[sn\_grc\_appr.admin\]

</td><td>

Create, read, update, and delete access to the Approval Configuration, Approval Levels, and Approval Rules tables.**Note:** The Approver Configurator admin has read access to the **Script** field on the Approval Rule form.

</td><td>

None

</td></tr><tr><td>

Approver Configurator approver \[sn\_grc\_appr.approver\]

</td><td>

Create, read, update, and delete access to the Approval tables.

</td><td>

None

</td></tr><tr><td>

Approver Configurator developer\[sn\_grc\_appr.developer\]

</td><td>

-   Create, read, update, and delete access to the Approval Configuration, Approval Levels, and Approval Rules tables.
-   Create and write access to the script field.

 **Note:** The Approver Configurator developer has create and write access to the **Script** field on the Approval Rule form.

</td><td>

sn\_grc\_appr.admin

</td></tr></tbody>
</table>**Parent Topic:**[Using Approver Configurator for setting up approvals](../concept/approval-configuration.md)

