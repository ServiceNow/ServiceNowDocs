---
title: ERP Customization Mining roles
description: Administrators assign roles to give team members permission to configure or use ERP Customization Mining \(ERP-CM\).
locale: en-US
release: xanadu
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Customization Mining, ERP Customization Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# ERP Customization Mining roles

Administrators assign roles to give team members permission to configure or use ERP Customization Mining \(ERP-CM\).

**Important:** When you assign ERP-CM roles to a user, you must include the scope. For example, assign the `sn_erp_mining.erp_admin` role, not just `erp_admin`.

For more on assigning roles, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and contact your account representative.

<table id="table_u4j_ykv_cwb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Additional access

</th></tr></thead><tbody><tr><td>

sn\_erp\_mining.erp\_admin

</td><td>

Grants the user access to updating application setup.

</td><td>

Contains sn\_erp\_mining.erp\_user.

</td></tr><tr><td>

sn\_erp\_mining.erp\_user

</td><td>

Grants the user read access on all tables needed for ERP Customization Mining, as well as some field-level write access in the sn\_erp\_mining\_app\_candidate table.

</td><td>

Contains the following roles:-   sn\_erp\_integration.erp\_data\_pill
-   sn\_erp\_integration.erp\_user

</td></tr></tbody>
</table>**Parent Topic:**[Configuring ERP Customization Mining](configuring-ecm.md)

