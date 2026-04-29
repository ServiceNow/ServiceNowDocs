---
title: ERP Semantic Mining roles
description: Administrators assign roles to give team members permission to configure or use ERP Semantic Mining.
locale: en-US
release: australia
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, ERP Semantic Mining overview, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# ERP Semantic Mining roles

Administrators assign roles to give team members permission to configure or use ERP Semantic Mining.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

**Note:** When you assign ERP Semantic Mining roles to a user, you must include the scope. For example, assign the `sn_erp_mining.erp_admin` role, not just `erp_admin`.

For more on assigning roles, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and contact your account representative.

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

Grants the user read access on all tables needed for ERP Semantic Mining, as well as some field-level write access in the sn\_erp\_mining\_app\_candidate table.

</td><td>

Contains the following roles:-   sn\_erp\_integration.erp\_data\_pill
-   sn\_erp\_integration.erp\_user

</td></tr></tbody>
</table>**Parent Topic:**[Configuring ERP Semantic Mining](configuring-ecm.md)

