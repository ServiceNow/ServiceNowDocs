---
title: Components installed with Knowledge Product Entitlements
description: Several types of components are installed with the Knowledge Product Entitlements application.Business rules are added with activation of Knowledge Product Entitlements.Properties are added with activation of Knowledge Product Entitlements.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins for Customer Service Management, Reference, Customer Service Management]
---

# Components installed with Knowledge Product Entitlements

Several types of components are installed with the Knowledge Product Entitlements application.

## Business rules installed with Knowledge Product Entitlements

Business rules are added with activation of Knowledge Product Entitlements.

<table id="table_fgq_n12_z5"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge Product Entitlement

</td><td>

Knowledge\[kb\_knowledge\]

</td><td>

Implements the needed access controls for users with the sn\_customerservice.customer role.

</td></tr><tr><td>

KB Product Entitlements

</td><td>

Knowledge Base\[kb\_knowledge\_base\]

</td><td>

 

</td></tr></tbody>
</table>## Properties installed with Knowledge Product Entitlements

Properties are added with activation of Knowledge Product Entitlements.

<table id="table_kb_rel_prod_z5"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

kb\_product\_entitlement.knowledge\_base.enable

</td><td>

Enable access control of Knowledge Bases based on product entitlements.If enabled, customers can access all of the knowledge bases related to the products for which they have entitlements.

 -   **Type**: true/false
-   **Default value**: false
-   **Location**: **Knowledge Product Entitlements** &gt; **Properties**

</td></tr><tr><td>

kb\_product\_entitlement.knowledge\_base.allow\_empty\_products

</td><td>

Allow access to Knowledge Bases with empty **Related Products** field. If enabled, customers can access all knowledge bases even if no products have been specified in the **Related Products** field on the Knowledge Base form.

 -   **Type**: true/false
-   **Default value**: false
-   **Location**: **Knowledge Product Entitlements** &gt; **Properties**

</td></tr><tr><td>

kb\_product\_entitlement.article.enable

</td><td>

Enable access control of Knowledge Articles based on product entitlements.If enabled, customers can access all of the knowledge articles related to the products for which they have entitlements.

 -   **Type**: true/false
-   **Default value**: false
-   **Location**: **Knowledge Product Entitlements** &gt; **Properties**

</td></tr><tr><td>

kb\_product\_entitlement.article.allow\_empty\_products

</td><td>

Allow access to Knowledge Articles with empty **Related Products** field. If enabled, customers can access all knowledge articles even if no products have been specified in the **Related Products** field on the Knowledge form.

 -   **Type**: true/false
-   **Default value**: false
-   **Location**: **Knowledge Product Entitlements** &gt; **Properties**

</td></tr></tbody>
</table>