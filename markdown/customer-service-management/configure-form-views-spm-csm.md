---
title: Configure form views for Service Portfolio Management integration
description: Configure the form layout and related lists for the Sold Product, Case, Account, and Service Offering forms to provide users with the correct visibility into which service offerings are associated to which sold products.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating with Service Portfolio Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Configure form views for Service Portfolio Management integration

Configure the form layout and related lists for the Sold Product, Case, Account, and Service Offering forms to provide users with the correct visibility into which service offerings are associated to which sold products.

## Before you begin

Role required: admin

Instead of doing the configuration through this procedure, consider using guided setup. For more information, see [Integrate with Service Portfolio Management using Guided Setup](../concept/spm-csm-integration.md).

## Procedure

1.  Navigate to **Customer Service**.

2.  Add the following fields to forms and related lists, as required.

<table id="table_cyv_jyc_kjb"><thead><tr><th>

Form

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Service Offering

</td><td>

Add the **Add the Sold Products** related list to provide service owners visibility into which customers have subscribed to which service offerings.

</td></tr><tr><td>

Product Model forms

</td><td>

Add the **Offerings** \( \(**Offering** &gt; **Model ID** \) related list on the Product Model/Service Model forms to enable customer service managers to associate service offerings to product models. To enable the **Edit** button on the Offerings related list:1.  Configure the list control and deselect the **Omit Edit** check box.
2.  Add the sn\_customerservice\_manager role.
 If you do not see the **Edit** button enabled, see [Assign roles for Service Portfolio Management integration](assign-roles-spm-csm.md) for more details.

 **Note:** To configure catalog items for product models, add the Catalog Items related list. For more information, see [Configure product model and catalog item relationships](create-csm-product-model-items.md).

</td></tr><tr><td>

Sold Products on the Account form

</td><td>

Add the **Service Offering** column to the Sold Products related list to enable customer service agents or managers to view service offerings associated to the sold product for an account or consumer.

</td></tr><tr><td>

Case

</td><td>

Add the **Service Offering** field for the Sold Product to the Case form. This enables customer service agents dealing with customer issues to see the service offering associated to sold product for a case.

</td></tr><tr><td>

Sold Product

</td><td>

Add the **Service Offering** field to the Sold Product form to enable customer service managers to associate a service offering to a sold product for an account or consumer.

</td></tr></tbody>
</table>
