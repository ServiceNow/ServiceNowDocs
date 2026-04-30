---
title: Roles installed with customer access management
description: Customer access management uses different predefined functional and granular roles to establish relationships between users and entities. The granular and functional roles help provide user access to information and maintain data security.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Configuring customer access management, User management, Set up your environment, Configure, Customer Service Management]
---

# Roles installed with customer access management

Customer access management uses different predefined functional and granular roles to establish relationships between users and entities. The granular and functional roles help provide user access to information and maintain data security.

## Functional and granular roles overview

Functional and granular roles help provide authorized related parties access to the case, and provide additional contacts or additional consumers access to the sold product.

Granular roles provide access to cases, sold product, and related entities. One or more granular roles can be bundled together as a functional role to perform a meaningful action. Linking multiple granular roles to a functional role enables you to build your own access rules by applying the functional and granular roles for various Customer Service Management \(CSM\) entities.

A granular model helps to protect data by granting the required level of access to the relevant CSM entities. With this functionality, each role is associated with a set of privileges or responsibilities that determine users’ access to certain information. You can set granular policies that authorize individuals to do their jobs efficiently and effectively, which helps to improve the customer experience.

## Roles and descriptions

Functional roles are a set of granular roles that are required to perform a function that requires access on multiple entities. The following table lists the functional roles for customer access management.

<table id="table_cwg_hg2_rrb"><thead><tr><th>

Role title \[name\]

</th><th>

Plugins required

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Case Authorized Contact\[sn\_customerservice.case\_authorized\_contact\]

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

This role provides access to add additional comments and attachments, accept or reject a solution, receive notifications on case updates, close a case, and update case tasks.

</td><td>

sn\_customerservice.case\_write\_granular

</td></tr><tr><td>

Case Authorized Consumer\[sn\_customerservice.case\_authorized\_consumer\]

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

This role provides access to add additional comments and attachments, accept or reject a solution, receive notifications on case updates, close a case, and update case tasks.

</td><td>

sn\_customerservice.case\_write\_granular

</td></tr><tr><td>

Case Authorized Contributor\[sn\_customerservice.case\_authorized\_contributor\]

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

This role provides access to add additional comments and attachments, accept or reject a solution, receive notifications on case updates, close a case, and update case tasks.

</td><td>

sn\_customerservice.case\_write\_granular

</td></tr><tr><td>

Sold Product Authorized Contact\[sn\_install\_base.sold\_product\_authorized\_contact\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides access to view sold product and associated install base items, create cases, and access cases that are related to the sold product. Also, this role provides access to sold product related parties, affected install base items, and manage service catalog requests from the sold product.

</td><td>

-   sn\_customerservice.case\_authorized\_contact
-   sn\_install\_base.sold\_product\_contact\_read\_granular
-   sn\_install\_base.sold\_product\_read\_granular
-   sn\_install\_base.install\_base\_read\_granular
-   sn\_install\_base.installed\_product\_read\_granular

</td></tr><tr><td>

Sold Product Authorized Consumer\[sn\_install\_base.sold\_product\_authorized\_consumer\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides access to view sold product and associated install base items, create cases, and access cases related to the sold product. Also, this role provides access to sold product related parties, affected install base items, and manage service catalog requests from the sold product.

</td><td>

-   sn\_customerservice.case\_authorized\_consumer
-   sn\_install\_base.sold\_product\_consumer\_read\_granular
-   sn\_install\_base.sold\_product\_read\_granular
-   sn\_install\_base.install\_base\_read\_granular
-   sn\_install\_base.installed\_product\_read\_granular

</td></tr><tr><td>

Install Base Authorized Contact\[sn\_install\_base.install\_base\_authorized\_contact\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides the contact access to view the install base and its associated sold products when added as a related party. Additionally, it enables the contact to create and manage cases for the related install base records.​ Creation of case is only allowed if the contact and install base belong to the same account.

</td><td>

-   sn\_customerservice.case\_write\_granular​
-   sn\_install\_base.install\_base\_related\_party\_write\_granular​
-   sn\_install\_base.sold\_product\_read\_granular
-   sn\_install\_base.install\_base\_read\_granular
-   sn\_install\_base.installed\_product\_read\_granular

</td></tr><tr><td>

Install Base Authorized Consumer\[sn\_install\_base.install\_base\_authorized\_consumer\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides the consumer access to view the install base and its associated sold products when added as a related party. Additionally, it enables the user to create and manage cases for the related install base records.​

</td><td>

-   sn\_customerservice.case\_write\_granular​
-   sn\_install\_base.install\_base\_related\_party\_write\_granular​
-   sn\_install\_base.sold\_product\_read\_granular
-   sn\_install\_base.install\_base\_read\_granular
-   sn\_install\_base.installed\_product\_read\_granular

</td></tr><tr><td>

Install Base Authorized Contributor\[sn\_install\_base.install\_base\_authorized\_contributor\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides the internal user to view the install base and its associated sold products when added as a related party. Additionally, it enables the user to create and manage cases for the related install base records.​​

</td><td>

-   sn\_customerservice.case\_write\_granular​
-   sn\_install\_base.install\_base\_related\_party\_write\_granular​
-   sn\_install\_base.sold\_product\_read\_granular
-   sn\_install\_base.install\_base\_read\_granular
-   sn\_install\_base.installed\_product\_read\_granular

</td></tr><tr><td>

Install Base Authorized Member\[sn\_install\_base.install\_base\_authorized\_member\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides the service organization member to view the install base and its associated sold products when added as a related party. Additionally, it enables the user to create and manage cases for the related install base records.​

</td><td>

-   sn\_customerservice.case\_write\_granular​
-   sn\_install\_base.install\_base\_related\_party\_write\_granular​
-   sn\_install\_base.sold\_product\_read\_granular
-   sn\_install\_base.install\_base\_read\_granular
-   sn\_install\_base.installed\_product\_read\_granular

</td></tr><tr><td>

Install Base Authorized Account

</td><td>

Customer Service Install Base Management \[com.snc.install\_base

</td><td>

Provides access to all the contacts of the account to view the install base and its associated sold products when added as a related party. Additionally, it enables the contact to create and manage cases for the related install base records. Creation of case is only allowed if contact and install base belongs to same account.

</td><td>

-   sn\_customerservice.case\_write\_granular​
-   sn\_install\_base.install\_base\_related\_party\_write\_granular​
-   sn\_install\_base.sold\_product\_read\_granular
-   sn\_install\_base.install\_base\_read\_granular
-   sn\_install\_base.installed\_product\_read\_granular

</td></tr><tr><td>

Install Base Service Organization

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

Provides access to all the members of service organization to view the install base and its associated sold products when added as a related party. Additionally, it enables the users to manage cases for the related install base records.

</td><td>

-   sn\_customerservice.case\_write\_granular​
-   sn\_install\_base.install\_base\_related\_party\_write\_granular​
-   sn\_install\_base.sold\_product\_read\_granular
-   sn\_install\_base.install\_base\_read\_granular
-   sn\_install\_base.installed\_product\_read\_granular

</td></tr><tr><td>

sn\_install\_base.install\_base\_admin

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

Enables user with feature admin role to manage administrative tasks like read, write, create, delete, data view, and case view related to install base and sold product related entities.

</td><td>

-   sn\_install\_base.install\_base\_read
-   sn\_install\_base.install\_base\_write
-   sn\_install\_base.install\_base\_create
-   sn\_install\_base.install\_base\_delete
-   sn\_customerservice.customer\_data\_viewer
-   sn\_customerservice.case.viewer

</td></tr></tbody>
</table>The following table lists the granular roles for customer access management.

<table id="table_bxx_zpb_kt"><thead><tr><th>

Role title \[name\]

</th><th>

Plugin required

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Sold Product Read\[sn\_install\_base.sold\_product\_read\_granular\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides granular read access to the sold product.

</td><td>

None

</td></tr><tr><td>

Sold Product Contact Read\[sn\_install\_base.sold\_product\_contact\_read\_granular\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides granular read access to related parties of the sold product.

</td><td>

None

</td></tr><tr><td>

Sold Product Contact Write\[sn\_install\_base.sold\_product\_contact\_write\_granular\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides granular write access to related parties of the sold product.

</td><td>

sn\_install\_base.sold\_product\_contact\_read\_granular

</td></tr><tr><td>

Sold Product Consumer Read\[sn\_install\_base.sold\_product\_consumer\_read\_granular\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides granular read access to additional consumers of the sold product and sold product-related parties.

</td><td>

None

</td></tr><tr><td>

Sold Product Consumer Write\[sn\_install\_base.sold\_product\_consumer\_write\_granular\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides granular write access to additional consumers of the sold product and sold product-related parties.

</td><td>

sn\_install\_base.sold\_product\_consumer\_read\_granular

</td></tr><tr><td>

Case Read\[sn\_customerservice.case\_read\_granular\]

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

This role provides granular read access to the case.

</td><td>

None

</td></tr><tr><td>

Cases Create\[sn\_customerservice.case\_create\_granular\]

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

This role provides granular create access to the case.

</td><td>

sn\_customerservice.case\_read\_granular

</td></tr><tr><td>

Case Write\[sn\_customerservice.case\_write\_granular\]

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

This role provides granular write access to the case.

</td><td>

-   sn\_customerservice.case\_read\_granular
-   sn\_customerservice.case\_create\_granular

</td></tr><tr><td>

Case Related Party Write \[sn\_customerservice.case\_related\_party\_write\_granular\]

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

This role provides granular write access to case-related parties.

</td><td>

None

</td></tr><tr><td>

Install Base Read\[sn\_install\_base.install\_base\_read\_granular\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides granular read access to the install base.

</td><td>

None

</td></tr><tr><td>

Install Base Related Party Read\[sn\_install\_base.install\_base\_related\_party\_read\_granular​\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides granular read access to install base related party records.​

</td><td>

None

</td></tr><tr><td>

Install Base Related Party Write\[sn\_install\_base.install\_base\_related\_party\_write\_granular\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides granular write access to install base related party records.​

</td><td>

\[sn\_install\_base.install\_base\_related\_party\_read\_granular​\]

</td></tr><tr><td>

Installed Product Read\[sn\_install\_base.installed\_product\_read\_granular\]

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

This role provides granular read access to the installed product.

</td><td>

None

</td></tr></tbody>
</table>**Related topics**  


[Assign granular roles to a functional role](../task/assign-granular-to-func-role-cam.md)

