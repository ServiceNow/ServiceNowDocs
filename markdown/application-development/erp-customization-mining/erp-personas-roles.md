---
title: ERP Semantic Mining roles
description: Administrators assign roles to give team members permission to configure or use ERP Semantic Mining \(ERP-CM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-customization-mining/erp-personas-roles.html
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Semantic Mining, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# ERP Semantic Mining roles

Administrators assign roles to give team members permission to configure or use ERP Semantic Mining \(ERP-CM\).

**Important:** When you assign ERP-CM roles to a user, you must include the scope. For example, assign the `sn_erp_mining.erp_admin` role, not just `erp_admin`.

For more on assigning roles, see .

To learn more about managing per-user subscriptions, see  and contact your account representative.

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
</table>**Parent Topic:**[Configuring ERP Semantic Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-customization-mining/configuring-ecm.md)

