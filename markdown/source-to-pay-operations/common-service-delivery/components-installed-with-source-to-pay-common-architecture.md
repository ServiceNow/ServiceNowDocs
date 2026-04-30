---
title: Components installed with Source-to-Pay Common Architecture
description: Several types of components are installed with the installation of the Source-to-Pay Common Architecture application, including tables and user roles.
locale: en-US
release: yokohama
product: Common Service Delivery
classification: common-service-delivery
topic_type: reference
last_updated: "2025-02-18"
reading_time_minutes: 10
breadcrumb: [Install the Finance and Supply Chain common applications, Configuring FSC common applications, Finance and Supply Chain common applications, Finance and Supply Chain applications, Finance and Supply Chain]
---

# Components installed with Source-to-Pay Common Architecture

Several types of components are installed with the installation of the Source-to-Pay Common Architecture application, including tables and user roles.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Accounts Payable Viewer

 \[sn\_shop.accounts\_payable\_viewer\]

</td><td>

Read access to purchase orders, invoices, and other task-related objects that arise from purchase order creation.

</td><td>

None

</td></tr><tr><td>

Acknowledgment Task Owner

 \[sn\_shop.acknowledgment\_task\_owner\]

</td><td>

Access to all purchase orders and purchase requisitions. Read-only access to the main objects, but can update assigned tasks.

</td><td>

None

</td></tr><tr><td>

Business Owner\[sn\_shop.invoice\_owner\]

</td><td>

Access only to their own invoices and related data.

</td><td>

None.

</td></tr><tr><td>

Procurement Administrator

 \[sn\_shop.procurement\_administrator\]

</td><td>

Access to the primary data and administration sections of the Purchase Automation module.

</td><td>

-   Procurement Primary Data Admin \[sn\_fin.procurement\_primary\_data\_admin\]
-   Procurement Specialist \[sn\_shop.procurement\_specialist\]

</td></tr><tr><td>

Procurement Common Administrator

 \[sn\_shop.procurement\_common\_admin\]

</td><td>

Access to all tables, including deletion of records, in the Source-to-Pay Common Architecture application.

</td><td>

Procurement Common User \[sn\_shop.procurement\_common\_user\]

</td></tr><tr><td>

Procurement Common Reader

 \[sn\_shop.procurement\_common\_reader\]

</td><td>

Read access to all tables available in the Source-to-Pay Common Architecture application.

</td><td>

Procurement User \[sn\_fin.procurement\_user\]

</td></tr><tr><td>

Procurement Common User

 \[sn\_shop.procurement\_common\_user\]

</td><td>

Access to perform, create, and update operations on all tables in the Source-to-Pay Common Architecture application.

</td><td>

Procurement Common Reader \[sn\_shop.procurement\_common\_reader\]

</td></tr><tr><td>

Procurement Specialist

 \[sn\_shop.procurement\_specialist\]

</td><td>

Access to all the data of the Sourcing and Purchasing Automation module, except the primary data.

</td><td>

-   Procurement User \[sn\_fin.procurement\_user\]
-   Contract Manager \[contract\_manager\]

</td></tr><tr><td>

Procurement Specialist\_Manager\[sn\_shop.procurement\_specialist\_manager\]

</td><td>

Access to the Procurement Team Performance Dashboard to view your organization's overall performance. This role has the same access as a procurement specialist, except that they have access to the manager dashboards.

</td><td>

-   Procurement Specialist \[sn\_shop.procurement\_specialist\]
-   Procurement Team Manager \[sn\_spend\_psd.manager\]

</td></tr><tr><td>

Purchasing Task Owner

 \[sn\_shop.purchasing\_task\_owner\]

</td><td>

Access to all purchase orders, requisitions, negotiations, sourcing requests, and purchasing tasks.

</td><td>

None

</td></tr><tr><td>

Shopper

 \[sn\_shop.shopper\]

</td><td>

Access to the Shopping Hub portal to make requests and purchases.

</td><td>

None

</td></tr><tr><td>

Shopping Hub Administrator

 \[sn\_shop.shopping\_hub\_admin\]

</td><td>

Access to all modules of the Source-to-Pay Common Architecture application.

</td><td>

-   Decision Table Admin \[decision\_table\_admin\]
-   Procurement User \[sn\_fin.procurement\_user\]
-   Model Manager \[model\_manager\]
-   Category Manager \[category\_manager\]

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Acknowledgement Task\[sn\_shop\_acknowledgement\_task\]

</td><td>

Extends the Finance Task table and stores acknowledgments such as the milestone and receipt task.

</td></tr><tr><td>

Approval Group\[sn\_shop\_approval\_group\]

</td><td>

Stores a set of approval rules.

</td></tr><tr><td>

Approval Group Plan\[sn\_shop\_approval\_group\_plan\]

</td><td>

Stores the approval plans that determine how the overall approval process is run.

</td></tr><tr><td>

Approval Plan Detail\[sn\_shop\_approval\_plan\_detail\]

</td><td>

Stores an instance of the approval record for a purchase line that is created based on the approval plan.

</td></tr><tr><td>

Approval Reminder Task\[sn\_shop\_approval\_reminder\_task\]

</td><td>

Extends the Purchasing task table and stores information about the specific tasks required to complete the approval process.

</td></tr><tr><td>

Approval Rule\[sn\_shop\_approval\_rule\]

</td><td>

Stores the rule that triggers the creation of an approval record. It uses a condition builder to build the trigger condition for approvals.

</td></tr><tr><td>

Approval Rule Composition\[sn\_shop\_approval\_rule\_composition\]

</td><td>

Stores information about the approval rule and its associated approval group.

</td></tr><tr><td>

Attribute

 \[sn\_shop\_attribute\]

</td><td>

Stores specific attribute types and the values that are associated with a product model. For example, a laptop can have an attribute for the type of memory used, which can be SSD or Hard disk.

</td></tr><tr><td>

Attribute Set

 \[sn\_shop\_attribute\_set\]

</td><td>

Stores a group of attribute types that can later be associated with a supplier product. For example, Memory, Graphic card, and CPU can be an attribute set that can be associated with a product group.

</td></tr><tr><td>

Attribute Type

 \[sn\_shop\_attribute\_type\]

</td><td>

Stores the various types of attributes that are used when creating a product attribute.

</td></tr><tr><td>

Capitalization Policy\[sn\_shop\_capitalization\_policy\]

</td><td>

Stores the condition based on which an asset is capitalized, and a fixed asset record is created.

</td></tr><tr><td>

Cart Delivery\[sn\_shop\_cart\_delivery\]

</td><td>

Stores information related to the delivery details of items in a shopping cart or purchase requisition. It has various details, such as order type, delivery location, expected delivery date, estimated shipping, payment allocations, and so on.

</td></tr><tr><td>

Cart Header\[sn\_shop\_cart\_header\]

</td><td>

Stores high-level information about the purchase requisition. It has various details, such as requisition ID, shopper details, requisition date, shopper payable amount, status, and so on.

</td></tr><tr><td>

Cart Line\[sn\_shop\_cart\_line\]

</td><td>

Stores the details of a purchase line that is added to a cart. It has various details such as the supplier product selected, checkout type, business owner, delivery location, and so on.

</td></tr><tr><td>

Credit Allocation Rules\[sn\_shop\_credit\_allocation\_rules\]

</td><td>

Stores the credit allocation rules that are based on how a credit is allocated to an individual shopper. The allocation can be based on the inventory asset or user condition.

</td></tr><tr><td>

Delivery Address Task\[sn\_shop\_delivery\_address\_task\]

</td><td>

Extends the Purchasing Task table and stores the tasks that are associated with verifying and validating the delivery location for a purchase line.

</td></tr><tr><td>

Delivery Location\[sn\_shop\_delivery\_location\]

</td><td>

Stores the delivery location for a given shop line or cart line.

</td></tr><tr><td>

Employee Credit\[sn\_shop\_employee\_credit\]

</td><td>

Stores the credit amount that is allocated for a user with supporting information such as the responsible cost center and credit allocation rule.

</td></tr><tr><td>

ERP Address Mapping\[sn\_shop\_erp\_address\_map\]

</td><td>

Stores the mapping between the ERP address and the location.

</td></tr><tr><td>

ERP Asset Category Mapping\[sn\_shop\_erp\_asset\_category\_map\]

</td><td>

Stores the mapping between the ERP source and the capitalization policy.

</td></tr><tr><td>

ERP Material Group Mapping\[sn\_shop\_erp\_material\_group\_map\]

</td><td>

Stores the mapping between the ERP source, model category, and material group.

</td></tr><tr><td>

Handling Fee\[sn\_shop\_handling\_fee\]

</td><td>

Stores details about handling fees, which are additional charges added to purchase requests under specific conditions.

</td></tr><tr><td>

Integration Error\[sn\_shop\_erp\_error\_task\]

</td><td>

Single table to address all integration errors.

</td></tr><tr><td>

Invoice\[sn\_shop\_invoice\]

</td><td>

Stores important data about shopping invoices temporarily before this data is sent to the primary table.

</td></tr><tr><td>

Invoice cost allocation\[sn\_shop\_invoice\_cost\_allocation\]

</td><td>

Stores the allocated invoice line cost across multiple cost centers or ledger accounts.

</td></tr><tr><td>

Invoice Line\[sn\_shop\_invoice\_line\]

</td><td>

Stores important data about imported invoice line temporarily before this data is sent to the primary table.

</td></tr><tr><td>

Invoice Payment Detail\[sn\_shop\_invoice\_payment\_detail\]

</td><td>

Stores important data about supplier data temporarily before this data is sent to the primary table.

</td></tr><tr><td>

Invoice Tax Line\[sn\_shop\_invoice\_tax\_line\]

</td><td>

Extends the Base Tax Line table and stores the tax lines for purchases that are invoiced.

</td></tr><tr><td>

Job Code\[sn\_shop\_job\_code\]

</td><td>

Stores the job codes that are associated with business owners that primarily drive the approval hierarchy.

</td></tr><tr><td>

Ledger Assignment Rules\[sn\_shop\_ledger\_assignment\_rule\]

</td><td>

Stores the rules that apply to the supplier products, product model or product category, and cost center. These rules are based on the accounting details, such as the capex and expense accounts, that are populated on a purchase line.

</td></tr><tr><td>

Milestone\[sn\_shop\_milestone\]

</td><td>

Extends the Acknowledgment Task table and stores the acknowledgment of services received.

</td></tr><tr><td>

Negotiation\[sn\_shop\_negotiation\]

</td><td>

Stores the negotiation object that is created for a supplier product in a sourcing activity.

</td></tr><tr><td>

Negotiation to Contract Relationships\[sn\_shop\_m2m\_negotiation\_contract\]

</td><td>

Stores the mapping between the negotiation and contract.

</td></tr><tr><td>

Negotiation Event\[sn\_shop\_negotiation\_event\]

</td><td>

Stores the negotiation events that are created for a supplier product in a sourcing activity.

</td></tr><tr><td>

Non Catalog Intake\[sn\_shop\_non\_catalog\_intake\]

</td><td>

Extends the Import Set Row table and acts like a staging table for the non-catalog intake flow.

</td></tr><tr><td>

Order Template\[sn\_shop\_order\]

</td><td>

Stores all purchase orders. This is a base table.

</td></tr><tr><td>

Order to Contract Relationships\[sn\_shop\_m2m\_order\_contract\]

</td><td>

Stores the mapping between the purchase order and contract.

</td></tr><tr><td>

Order Permission\[sn\_shop\_m2m\_order\_users\_covered\]

</td><td>

Stores the mapping between the purchasing permission and purchase order.

</td></tr><tr><td>

Order Line Template\[sn\_shop\_order\_line\]

</td><td>

Extends the Shop Line table and stores the purchase order line for any purchase order.

</td></tr><tr><td>

Purchase Cost Allocation

 \[sn\_shop\_cost\_allocation\]

</td><td>

Stores the type of cost allocation, associated cost center, and the amount that is allocated for a shopper that can be used to buy a supplier product.

</td></tr><tr><td>

Purchasing Permission\[sn\_shop\_covered\_user\]

</td><td>

Stores the purchasing permission for a user, group, cost center, or department.

</td></tr><tr><td>

PSM FX Currency\[sn\_shop\_fx\_currency\_instance\]

</td><td>

Stores the converted Fx2 currency amount into legal entity local currency amount and legal entity reporting currency amount by using the conversion rate from the Finance Exchange Rates table.

</td></tr><tr><td>

Pricing\[sn\_shop\_m2m\_product\_contract\]

</td><td>

Stores the mapping of a supplier product and its price that is based on the associated contract.

</td></tr><tr><td>

Product Purchases by Job code and Department\[sn\_shop\_user\_product\_purchase\]

</td><td>

Stores the aggregation of products purchased by the job code.

</td></tr><tr><td>

Purchase\[sn\_shop\_purchase\]

</td><td>

Stores the purchase record that is created for each purchasing or sourcing activity.

</td></tr><tr><td>

Purchases by Category\[sn\_shop\_user\_category\_purchase\]

</td><td>

Stores the analytical data for purchases by product category.

</td></tr><tr><td>

Product Purchases by Job code and Department\[sn\_shop\_user\_product\_purchase\]

</td><td>

Stores the aggregation of products purchased by the job code.

</td></tr><tr><td>

Purchasing Task\[sn\_shop\_task\]

</td><td>

Extends the Finance Task table and stores the various tasks that are associated with a purchase such as finance and contract tasks.

</td></tr><tr><td>

Purchase Order History\[sn\_shop\_order\_history\]

</td><td>

Extends the Order Template table and stores the older purchase order record when an order is revised.

</td></tr><tr><td>

Purchase Order Line History\[sn\_shop\_order\_line\_history\]

</td><td>

Extends the Order Line Template table and stores the older purchase order line record when a purchase order line is revised.

</td></tr><tr><td>

Purchase Order Line\[sn\_shop\_purchase\_order\_line\]

</td><td>

Extends the Order Line Template table and stores the purchase order line for a purchase.

</td></tr><tr><td>

Purchase Order\[sn\_shop\_purchase\_order\]

</td><td>

Extends the Order Template table and stores the purchase order for a given purchase.

</td></tr><tr><td>

Product Visuals\[sn\_shop\_supplier\_product\_artifact\]

</td><td>

Stores the artifacts that are used to display product appearances on the user interface.

</td></tr><tr><td>

Purchase Requisition\[sn\_shop\_purchase\_requisition\]

</td><td>

Stores the purchase requisition for a purchase or sourcing activity.

</td></tr><tr><td>

Purchase Line\[sn\_shop\_purchase\_line\]

</td><td>

Extends the Request Line table and stores the purchase line that is associated with a purchasing or sourcing activity.

</td></tr><tr><td>

Purchase\[sn\_shop\_purchase\]

</td><td>

Extends the Order Template table and stores the purchase order for a given purchase.

</td></tr><tr><td>

PSM State Mapper\[sn\_shop\_psm\_state\_mapper\]

</td><td>

Stores the unique states of tasks related to negotiation, sourcing request, purchase requisition, and procurement case.

</td></tr><tr><td>

Product group\[sn\_shop\_product\_group\]

</td><td>

Stores the name that is associated with an attribute set that is then referenced by the supplier product and product model.

</td></tr><tr><td>

Price Break\[sn\_shop\_price\_break\]

</td><td>

Stores the price divided based on the number of quantities purchased for a given supplier product contract.

</td></tr><tr><td>

Pre-Payment\[sn\_shop\_pre\_payment\]

</td><td>

Stores a record of prepayment done for a purchase line as per a contract.

</td></tr><tr><td>

Percent Complete Configuration\[sn\_shop\_percent\_complete\_config\]

</td><td>

Stores the configurations to determine the percentage of payment that is completed for an order.

</td></tr><tr><td>

Payment Terms\[sn\_shop\_payment\_term\]

</td><td>

Stores the term in which a payment would be made. For example, a term could be seven days after the invoice date.

</td></tr><tr><td>

Payment Methods\[sn\_shop\_payment\_method\]

</td><td>

Stores the payment method that is selected by the shopper and the cost center or person responsible for the payment.

</td></tr><tr><td>

Paycheck Periods\[sn\_shop\_paycheck\_periods\]

</td><td>

Stores the number of paychecks through which a payment would be made.

</td></tr><tr><td>

Purchase Order Line History\[sn\_shop\_order\_line\_history\]

</td><td>

Extends the Order Line Template table and stores the older purchase order line record when a purchase order line is revised.

</td></tr><tr><td>

Receipt\[sn\_shop\_receipt\]

</td><td>

Stores the receipt of a supplier product received as part of a purchase order line.

</td></tr><tr><td>

Receipt Task\[sn\_shop\_receipt\_task\]

</td><td>

Extends the Acknowledgment Task table and stores the state of a receipt confirmation.

</td></tr><tr><td>

Request Line Template\[sn\_shop\_request\_line\]

</td><td>

Extends the Shop Line table and stores the purchase request line items.

</td></tr><tr><td>

Requisition Additional Info\[sn\_shop\_requisition\_additional\_info\]

</td><td>

Stores additional details about a purchase requisition, including its creation and update timestamps, and the users responsible for these actions.

</td></tr><tr><td>

Requisition Permission\[sn\_shop\_m2m\_purchasing\_users\_covered\]

</td><td>

Stores the mapping between the purchasing permission and purchase requisition.

</td></tr><tr><td>

Requisition to Contract Relationships\[sn\_shop\_m2m\_requisition\_contract\]

</td><td>

Stores the mapping between the purchase requisition and contract.

</td></tr><tr><td>

Revision Request\[sn\_shop\_revision\_request\]

</td><td>

Extends the Purchasing Task table and stores the state of a revision request for a purchase.

</td></tr><tr><td>

Revision Line\[sn\_shop\_rev\_request\_line\]

</td><td>

Extends the Request Line Template table and stores the revision line for a purchase.

</td></tr><tr><td>

Supplier Use by Department\[sn\_shop\_dept\_supplier\_purchase\]

</td><td>

Stores the analytics of suppliers that are used by departments.

</td></tr><tr><td>

Service Acknowledgment\[sn\_shop\_invoice\_task\]

</td><td>

Extends the Acknowledgement Task table and stores details about invoice tasks, which are an extension of acknowledgment tasks.

</td></tr><tr><td>

Shop Line\[sn\_shop\_line\]

</td><td>

Stores the order line template and request line template. This is a base table.

</td></tr><tr><td>

Sourcing to Contract Relationships\[sn\_shop\_m2m\_sourcing\_contract\]

</td><td>

Stores the mapping between the sourcing request and contract.

</td></tr><tr><td>

Shipment Details\[sn\_shop\_shipment\_details\]

</td><td>

Stores the shipment details that are associated with a purchase order line.

</td></tr><tr><td>

Shipment Product\[sn\_shop\_shipment\_product\]

</td><td>

Stores the shipment product details that are associated with a purchase order line.

</td></tr><tr><td>

Shipping methods\[sn\_shop\_shipping\_method\]

</td><td>

Stores the shipping method details that are associated with a purchase order line.

</td></tr><tr><td>

ShoppingHub API Cache\[sn\_shop\_shopnow\_api\_cache\]

</td><td>

Stores the cached data for quicker access by APIs. An example is the CachedCagetoryMap.

</td></tr><tr><td>

ShoppingHub Configuration\[sn\_shop\_shopnow\_content\]

</td><td>

Stores configurations that determine certain aspects of the application appearance and behavior. An example is the terms and conditions page URL.

</td></tr><tr><td>

Shopping Control\[sn\_shop\_shopping\_control\]

</td><td>

Stores the security rules that determine the access of supplier products for a given user.

</td></tr><tr><td>

Sourcing Request\[sn\_shop\_sourcing\_activity\]

</td><td>

Stores requests to source for supplier products.

</td></tr><tr><td>

Sourcing Task\[sn\_shop\_sourcing\_task\]

</td><td>

Extends the Purchasing Task table and stores the tasks that are related to a sourcing request.

</td></tr><tr><td>

Supplier Product\[sn\_shop\_supplier\_product\]

</td><td>

Stores the supplier products that represent goods or services that can be listed on the portal.

</td></tr><tr><td>

Supplier Product View\[sn\_shop\_supplier\_product\_view\]

</td><td>

Stores the analytics of the number of views for a supplier product.

</td></tr><tr><td>

Supplier Use by Shopper\[sn\_shop\_user\_supplier\_purchase\]

</td><td>

Stores the analytics of suppliers that are used by shoppers.

</td></tr><tr><td>

Shopper's Top Suppliers\[sn\_shop\_usr\_preferred\_supplier\]

</td><td>

Stores the mapping between the shopper and preferred supplier.

</td></tr><tr><td>

User Controls\[sn\_shop\_user\_control\]

</td><td>

Stores the mapping of a user and a shopping control.

</td></tr></tbody>
</table>**Parent Topic:**[Install the Finance and Supply Chain common applications](../../source-to-pay-operations/task/install-fsc-common-apps.md)

