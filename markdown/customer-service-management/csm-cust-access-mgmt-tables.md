---
title: Customer access management tables and plugins
description: Learn about the tables and plugins that you can use with customer access management.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure customer access management, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Customer access management tables and plugins

Learn about the tables and plugins that you can use with customer access management.

The customer access management feature adds new tables or modifies existing tables. You can activate the following plugins that enable features, such as enabling restricted contact access. To activate these plugins, you must have the admin role. For details, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

<table id="table_pqr_4xf_fsb"><thead><tr><th>

Plugin

</th><th>

Description

</th><th>

Tables

</th></tr></thead><tbody><tr><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

Enables customers to provide service and support to external customers by using several communication channels, such as email, web, and telephone.

</td><td>

-   Account Access

\[sn\_csm\_account\_access\]

-   Case

\[sn\_customerservice\_case\]​

-   Related Party

\[sn\_customerservice\_related\_party\]

-   Related Party Configuration

\[sn\_customerservice\_related\_party\_configuration\]​


</td></tr><tr><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

Enables customers to capture the current state of a customer's install base and establish the relationship to any downstream entities that might impact their functioning.

</td><td>

-   Sold Product

\[sn\_install\_base\_sold\_product\]​

-   Sold Product Related Party

\[sn\_install\_base\_sold\_product\_related\_party\]

-   Install Base Related Party

\[sn\_install\_base\_related\_party\]


</td></tr></tbody>
</table><table id="table_hsx_ctg_nrb"><thead><tr><th>

Table

</th><th>

Columns

</th></tr></thead><tbody><tr><td rowspan="2">

Account Access\[sn\_csm\_account\_access\]

 Enable restricted access to account contacts for sold products and install bases.

</td><td>

Account\[customer\_account\]

 Account associated with the sold product.

</td></tr><tr><td>

Restrict Contact AccessAccess that is restricted to entities due to their associated contacts.

 If the value of the field is **False**, the contacts that are associated with the account can read the sold products and install bases that are associated with the account.

 If the value of the field is **True**, the contacts that are associated with the accounts don’t get access to the sold products and install bases, unless they're added as a contact on the record or as a related party. The following contacts get access to the sold products and install bases:

-   Contacts that are associated with the sold product and install base records.
-   Contacts that are added as related parties with an Authorized Representative responsibility.
-   Contacts that belong to accounts that are added as related parties with an Authorized Account responsibility.

</td></tr><tr><td>

Responsibility Definition\[sn\_customerservice\_responsibility\_def\]

</td><td>

-   Name
-   Applicable to
-   Type
-   Unique

For more information on the column types, see [Create a responsibility definition](../task/t_CreateAResponsibilityDefinition.md).

</td></tr><tr><td>

Related Party Configuration\[sn\_customerservice\_related\_party\_configuration\]​

</td><td>

Default Responsibility\[sn\_customerservice\_responsibility\_def\]

 Reference to the sn\_customerservice\_responsibility\_def table.

**Note:** Starting with the Washington DC release, the Related Party Configuration \[sn\_customerservice\_related\_party\_configuration\] table is reparented to the Application file \[sys\_metadata\] table.

</td></tr><tr><td rowspan="3">

Sold Product \[sn\_install\_base\_sold\_product\]​

</td><td>

​Contact\[customer\_contact\]​

 Primary contact for the sold product.

</td></tr><tr><td>

Additional Consumers\[additional\_consumers\]​

 Additional consumers that are associated with the sold product. The **Additional Consumers** field isn’t exposed to customers through any forms or lists and is added for performance reasons.

</td></tr><tr><td>

Additional Users\[additional\_users\]

 Additional users that are associated with the sold product. The **Additional Users** field isn’t exposed to customers through any forms or lists and is added for performance reasons.

</td></tr><tr><td rowspan="6">

Sold Product Related Party\[sn\_install\_base\_sold\_product\_related\_party\]

</td><td>

​Sold Product\[sn\_install\_base\_sold\_product\]

 Products and components that are sold to an account or a consumer.

</td></tr><tr><td>

Type\[sn\_customerservice\_related\_party\_configuration\]

 Type of relationship that the related party has with the sold product.

</td></tr><tr><td>

Responsibility\[sn\_customerservice\_responsibility\_def\]

 Access level that the user has on the sold product and associated entities.

</td></tr><tr><td>

Consumer\[csm\_consumer\]

 Consumer that has the assigned responsibility for the sold product.

</td></tr><tr><td>

Contact\[customer\_contact\]​

 Contact that has the assigned responsibility for the sold product.

</td></tr><tr><td>

Account\[customer\_account\]

 All contacts within the account that have the assigned responsibility for the sold product.

</td></tr><tr><td rowspan="4">

Contact Sold Product\[sn\_install\_base\_rel\_soldproduct\_to\_contact\]​

 Establishes account contact relationships with the sold products.

 **Note:** Starting with the Xanadu release, the sn\_install\_base\_rel\_soldproduct\_to\_contact table has been deprecated for new customers.

For upgrade customers, the table continues to be supported and extends the sold product-related parties table \[sn\_install\_base\_sold\_product\_related\_party\].

</td><td>

​Sold Product\[sn\_install\_base\_sold\_product\]​

 Products and components that are sold to an account or a consumer.

</td></tr><tr><td>

​Contact\[customer\_contact\]​

 Contact that has the assigned responsibility for the sold product.

</td></tr><tr><td>

Type\[sn\_customerservice\_related\_party\_configuration\]

 Name for this relationship.

</td></tr><tr><td>

Responsibility\[sn\_customerservice\_responsibility\_def\]

 Access level that the contact has on the sold product and associated entities.

</td></tr><tr><td rowspan="2">

Consumer Sold Product\[sn\_install\_base\_m2m\_consumer\_sold\_product\]​

 **Note:** Starting with the Xanadu release, the sn\_install\_base\_m2m\_consumer\_sold\_product table has been deprecated for new customers.

For upgrade customers, the table continues to be supported and extends the sold product-related parties table \[sn\_install\_base\_sold\_product\_related\_party\].

</td><td>

Type\[sn\_customerservice\_related\_party\_configuration\]

 Name for this relationship.

</td></tr><tr><td>

Responsibility\[sn\_customerservice\_responsibility\_def\]

 Access level that the consumer has on the sold product and associated entities.

</td></tr><tr><td rowspan="2">

Case\[sn\_customerservice\_case\]​

</td><td>

Additional Consumers\[additional\_consumers\]​

 Additional consumers that are associated with the case. The **Additional Consumers** field isn’t exposed to customers through any forms or lists and is added for performance reasons.

</td></tr><tr><td>

Additional Users\[additional\_users\]

 Additional users that are associated with the case. The **Additional Users** field isn’t exposed to customers through any forms or lists and is added for performance reasons.

</td></tr><tr><td rowspan="9">

Install Base Related Party \[sn\_install\_base\_related\_party\]

 **Note:** The sn\_install\_base\_related\_party table is extendible and can be used to capture industry-specific attributes that correspond to a related party.​

</td><td>

Install Base Itemsn\_install\_base\_item

 Instances of the product that are configured for a customer.

</td></tr><tr><td>

Responsibility\[sn\_customerservice\_responsibility\_def\]

 Access level to install the base and related information.

</td></tr><tr><td>

Type\[sn\_customerservice\_related\_party\_configuration\]

 Name for this relationship.

</td></tr><tr><td>

Usersys\_user

 Consumer, contact, service organization, member, or internal user that has the assigned responsibility for the install base.

</td></tr><tr><td>

Consumer\[csm\_consumer\]

 Consumer that has the assigned responsibility for the install base.

</td></tr><tr><td>

Account\[customer\_account\]

 All contacts within the account that have the assigned responsibility for the install base.

</td></tr><tr><td>

Contact\[customer\_contact\]​

 Contact that is primarily responsible for the install base.

</td></tr><tr><td>

Service Organizationsn\_customer\_service\_organization

 Service organization that is primarily responsible for the install base.

</td></tr><tr><td>

Classclass

 Type of record.

</td></tr><tr><td>

Related Party\[sn\_customerservice\_related\_party\]

</td><td>

Responsibility\[sn\_customerservice\_responsibility\_def\]

 Reference to the sn\_customerservice\_responsibility\_def table.

</td></tr></tbody>
</table>