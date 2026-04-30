---
title: Domain system properties and user preferences
description: Administrators have access to properties and user preferences that control domain scope.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Setup and administration, Domain separation for service providers, Access Management]
---

# Domain system properties and user preferences

Administrators have access to properties and user preferences that control domain scope.

## Properties

New activations of domain separation automatically restrict domain scope to the record's domain for all related data or processes. When the user views a record in a form, the record's related data \(such as reference picker and related list data\) and applied processes \(such as business rules and client scripts\) are restricted to the record's domain scope. If there are records in multiple tabs, each tab has its own domain scope based on the record opened within that tab. The following properties restrict domain scope to either the record’s domain and the user’s current session domain.

<table id="table_zqj_nkp_1r"><thead><tr><th>

Property

</th><th>

Details

</th></tr></thead><tbody><tr><td>

glide.sys.domain.use\_record\_domain\_for\_processes

</td><td>

Restricts domain scope to the record's domain for all processes. This property does not apply to business rules. Business rules are always processed from the domain record. -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.sys.domain.use\_record\_domain\_for\_data

</td><td>

Restricts domain scope to the record's domain for all data.-   Type: true \| false
-   Default value: true in new domain activations from Fuji onwards \(upgrades from instances older than Fuji do not have this property in the table\)
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>When either the **glide.sys.domain.use\_record\_domain\_for\_processes** or the **glide.sys.domain.use\_record\_domain\_for\_data** property is set to **true**, the following properties are not used, regardless of their setting:

-   **glide.sys.domain.use\_record\_domain**
-   **glide.sys.domain.use\_record\_domain\_for\_client\_scripts**
-   **glide.sys.domain.domain\_change\_notify**
-   **glide.sys.domain.no\_change\_roles**

For a full list of properties see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:**

In new activations of domain separation starting with the Jakarta release, the session domain determines the business rules executed on the domain table. In previous versions, business rules executed on the domain table were set based on the newly created domain’s hierarchy. This behavior is modified by the **glide.sys.domain.skip\_domain\_insert\_businessrules** property. Setting this property to true significantly improves domain insert performance.

<table id="table_svj_pjk_dy"><thead><tr><th>

Property

</th><th>

Details

</th></tr></thead><tbody><tr><td>

glide.sys.domain.skip\_domain\_insert\_businessrules

</td><td>

Specifies the domain scope for business rules executed on the domain table. In new activations of domain separation, the property default is true and business rules are determined by the session domain. In existing implementations, the property default is false and the business rules are determined by the newly created domain’s hierarchy. -   Type: true \| false
-   Default value: True in new domain activations starting with Jakarta. False in existing implementations.

</td></tr><tr><td>

glide.sys.domain.skip\_non\_global\_businessrule\_if\_nodomain

</td><td>

Ensures that only bus.rules from global domain are executed when using queryNoDomain\(\) or when table is not domain-separated, so you can skip any other business rules-   Type: true \| false
-   Setting the property to false restores the old behavior and doesn't align with ServiceNow® recommended practices.
-   Recommended: Domain-separate your tables; always try to use the record's domain rather than the session domain.

</td></tr></tbody>
</table>## User preferences

In addition, user administrators can set the following user preference globally or on a per-user basis:

<table id="table_kgr_jlp_1r"><thead><tr><th>

Preference

</th><th>

Category

</th><th>

Updated By

</th><th>

Details

</th></tr></thead><tbody><tr><td>

glide.domain.session\_scope

</td><td>

Domain

</td><td>

Admin Only

</td><td>

When true, sets the default scope to the user's session domain rather than the record's domain. When false, the default scope is the record's domain. Users with the domain\_expand\_scope user role can still change the domain scope as needed.-   **Type**: true \| false
-   **Default value**: false

</td></tr><tr><td>

glide.domain.session\_scope\_notification

</td><td>

Domain

</td><td>

Admin Only

</td><td>

When true, displays a visual cue that record values include an expanded domain scope. When false, the notification is hidden.-   **Type**: true \| false
-   **Default value**: true

</td></tr></tbody>
</table>**Related topics**  


[Domain separation application properties](../concept/ds-application-properties.md)

