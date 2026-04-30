---
title: Components installed with Sourcing and Procurement Operations
description: Several types of components are installed with the activation of Sourcing and Procurement Operations, including tables, user roles, and scheduled jobs.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 14
breadcrumb: [Install Sourcing and Procurement Operations, Configuring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Components installed with Sourcing and Procurement Operations

Several types of components are installed with the activation of Sourcing and Procurement Operations, including tables, user roles, and scheduled jobs.

Demo data is available for this feature.

## Roles installed

<table id="table_y5t_xj1_2lb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Shopping Hub Administrator

 \[sn\_shop.shopping\_hub\_admin\]

</td><td>

Access to all modules of the Source-to-Pay Common Architecture application.

</td><td>

-   decision\_table\_admin
-   sn\_fin.procurement\_user
-   model\_manager
-   category\_manager

</td></tr><tr><td>

Shopper

 \[sn\_shop.shopper\]

</td><td>

Access to the Shopping Hub portal to make requests and purchases.

</td><td>

None

</td></tr><tr><td>

Procurement Administrator

 \[sn\_shop.procurement\_administrator\]

</td><td>

Access to the primary data and administration sections of the Purchase Automation module.

</td><td>

-   sn\_fin.procurement\_primary\_data\_admin
-   sn\_shop.procurement\_specialist

</td></tr><tr><td>

Procurement Specialist

 \[sn\_shop.procurement\_specialist\]

</td><td>

Access to all the data of the Sourcing and Purchasing Automation module, except the primary data.

</td><td>

-   sn\_fin.procurement\_user
-   contract\_manager

</td></tr><tr><td>

Accounts Payable Viewer

 \[sn\_shop.accounts\_payable\_viewer\]

</td><td>

Read access to purchase orders, invoices, and other task-related objects that arise from purchase order creation.

</td><td>

None

</td></tr><tr><td>

Purchasing Task Owner

 \[sn\_shop.purchasing\_task\_owner\]

</td><td>

Access to all purchase orders, requisitions, negotiations, sourcing requests, and purchasing tasks.

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

Procurement Common Administrator

 \[sn\_shop.procurement\_common\_admin\]

</td><td>

Access to all tables, including deletion of records, in the Source-to-Pay Common Architecture application.

</td><td>

sn\_shop.procurement\_common\_user

</td></tr><tr><td>

Procurement Common Reader

 \[sn\_shop.procurement\_common\_reader\]

</td><td>

Read access to all tables available in the Source-to-Pay Common Architecture application.

</td><td>

sn\_fin.procurement\_user

</td></tr><tr><td>

Procurement Common User

 \[sn\_shop.procurement\_common\_user\]

</td><td>

Access to perform, create, and update operations on all tables in the Source-to-Pay Common Architecture application.

</td><td>

sn\_shop.procurement\_common\_reader

</td></tr><tr><td>

sn\_spend\_mgmt.category\_manager\_admin

</td><td>

Can import the category taxonomy, update the Spend Category and Spend Category Stage tables and update the Spend category to Product category mappings.

</td><td>

None

</td></tr><tr><td>

sn\_spend\_mgmt.sourcing\_category\_manager

</td><td>

Can view and access the Category management tab and the Savings dashboard in Spend and Savings Management.

</td><td>

sn\_shop.procurement\_specialist

</td></tr><tr><td>

sn\_spend\_pipeline.pipeline\_management\_admin

</td><td>

Can configure the Pipeline project creation rule decision table to automate the creation of pipeline projects.

</td><td>

decision\_table\_admin

</td></tr><tr><td>

sn\_spend\_pipeline.sourcing\_pipeline\_user

</td><td>

Can view and access the Pipeline management tab.

</td><td>

None

</td></tr></tbody>
</table>**Note:** An application-specific admin role enables a user to manage application-level configurations, roles, and access controls. Your system-level admin on the production instance must grant the application-specific admin role to the appropriate users, and then remove the application-specific admin role from all users with the system-level admin role to help prevent system-level admins from viewing sensitive application data via forms, lists, and the UI. For more information, see [Application administration](https://www.servicenow.com/docs/access?context=application-administration&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## Roles installed with Procurement Case Management \(sn\_spend\_psd\)

<table id="table_ot2_zh4_vfc"><thead><tr><th>

Role title \[name\]

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Procurement Team Agent

 \[sn\_spend\_psd.agent\]

</td><td>

-   sn\_spend\_sdc.agent
-   sn\_slm.fulfiller
-   sn\_shop.shopper
-   canvas\_user

</td></tr><tr><td>

Procurement Team Manager

 \[sn\_spend\_psd.manager\]

</td><td>

-   sn\_spend\_sdc.manager
-   sn\_spend\_psd.agent

</td></tr><tr><td>

Procurement Task Owner

 \[sn\_spend\_psd.procurement\_task\_owner\]

</td><td>

sn\_slm.fulfiller

</td></tr><tr><td>

Procurement Service Delivery Admin

 \[sn\_spend\_psd.psd\_admin\]

</td><td>

-   sla\_admin
-   sn\_spend\_sdc.admin

</td></tr><tr><td>

Employee Requestor

 \[sn\_spend\_psd.requestor\]

</td><td>

sn\_spend\_sdc.requestor

</td></tr></tbody>
</table>## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|\[PSM\] Approval Due Date Breached|Creates a breached approvals review task if a due date for an approval is breached.|
|\[PSM\] Clear Recently Viewed Data|Clears the recently viewed data in ShoppingHub. This data comprises entries that were created more than 90 days ago by the logged-in user.|
|\[PSM\] Create Receiving Task|Creates receipt tasks against the purchase order, grouped by calendar month and recipient, on the first of every month.|
|\[PSM\] Create Service Acknowledgment Task|Creates service acknowledgment tasks on a monthly basis. This job automatically picks all purchase order lines that have started and are yet to reach their end dates, and have some remaining amount or percentage or quantity to be delivered.|
|\[PSM\] Execute Credit Allocation Rules|Runs the credit allocation rules that are set up. Employee credit records are created as per this rule.|
|\[PSM\] Execute Shopping Controls|Runs the shopping controls that are set up. User control records are created as per the shopping controls, and the respective supplier products are updated as well.|
|\[PSM\] Monitor Milestone Tasks|Fetches any active milestone whose completion date is today and updates the state of the milestone to Confirmation Required.|
|\[PSM\] Populate Spend Task – Due Date Bucket|Calculates the due date bucket of purchasing tasks to determine the category to which they belong to. The categories are Others, Due within 7 Days, and Overdue.|
|\[PSM\] Purchasing Data Aggregation|Populates the following aggregate tables: Product Purchases by Job Code, Supplier Use by Shopper, and Supplier Use by Department.|
|\[PSM\] Retiring Supplier Products|Updates the Published flag on the supplier product to False when the current date is the same as the sales end date on the supplier product.|
|\[PSM\] Revoke Expired Credits|Sets the credit status to Credit Expired after the expiration date on the credit is reached.|

## Tables installed

**Note:** The following tables are commonly available, within the Source-to-Pay Common Architecture application.

<table id="table_sgq_s5k_flb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

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

Delivery Location

 \[sn\_shop\_delivery\_location\]

</td><td>

Stores the delivery location for a given shop line or cart line.

</td></tr><tr><td>

ERP Address Mapping

 \[sn\_shop\_erp\_address\_map\]

</td><td>

Stores the mapping between the ERP address and the location.

</td></tr><tr><td>

ERP Asset Category Mapping

 \[sn\_shop\_erp\_asset\_category\_map\]

</td><td>

Stores the mapping between the ERP source and the capitalization policy.

</td></tr><tr><td>

ERP Material Group Mapping

 \[sn\_shop\_erp\_material\_group\_map\]

</td><td>

Stores the mapping between the ERP source, model category, and material group.

</td></tr><tr><td>

Integration Error

 \[sn\_shop\_erp\_error\_task\]

</td><td>

Stores integration errors that might occur when communicating or processing a request with ERP.

</td></tr><tr><td>

Invoice

 \[sn\_shop\_invoice\]

</td><td>

Stores the invoice that is associated with a purchase order.

</td></tr><tr><td>

Invoice Line

 \[sn\_shop\_invoice\_line\]

</td><td>

Stores the invoice lines for each corresponding purchase order line.

</td></tr><tr><td>

Job Code

 \[sn\_shop\_job\_code\]

</td><td>

Stores the job codes that are associated with business owners that primarily drive the approval hierarchy.

</td></tr><tr><td>

Milestone

 \[sn\_shop\_milestone\]

</td><td>

Extends the Acknowledgment Task table and stores the acknowledgment of services received.

</td></tr><tr><td>

Office Location

 \[sn\_shop\_office\_location\]

</td><td>

Stores delivery locations marked as office.

</td></tr><tr><td>

Order Line Template

 \[sn\_shop\_order\_line\]

</td><td>

Extends the Shop Line table and stores the purchase order line for any purchase order.

</td></tr><tr><td>

Order Template

 \[sn\_shop\_order\]

</td><td>

Stores all purchase orders. This is a base table.

</td></tr><tr><td>

Order to Contract Relationships

 \[sn\_shop\_m2m\_order\_contract\]

</td><td>

Stores the mapping between the purchase order and contract.

</td></tr><tr><td>

Payment Terms

 \[sn\_shop\_payment\_term\]

</td><td>

Stores the term in which a payment would be made. For example, a term could be seven days after the invoice date.

</td></tr><tr><td>

Price Break

 \[sn\_shop\_price\_break\]

</td><td>

Stores the price divided based on the number of quantities purchased for a given supplier product contract.

</td></tr><tr><td>

Pricing

 \[sn\_shop\_m2m\_product\_contract\]

</td><td>

Stores the mapping of a supplier product and its price that is based on the associated contract.

</td></tr><tr><td>

Product Group

 \[sn\_shop\_product\_group\]

</td><td>

Stores the name that is associated with an attribute set that is then referenced by the supplier product and product model.

</td></tr><tr><td>

Product Visuals

 \[sn\_shop\_supplier\_product\_artifact\]

</td><td>

Stores the artifacts that are used to display product appearances on the user interface.

</td></tr><tr><td>

Purchase Order

 \[sn\_shop\_purchase\_order\]

</td><td>

Extends the Order Template table and stores the purchase order for a given purchase.

</td></tr><tr><td>

Purchase Order Line

 \[sn\_shop\_purchase\_order\_line\]

</td><td>

Extends the Order Line Template table and stores the purchase order line for a purchase.

</td></tr><tr><td>

Receipt

 \[sn\_shop\_receipt\]

</td><td>

Stores the receipt of a supplier product received as part of a purchase order line.

</td></tr><tr><td>

Shipment Details

 \[sn\_shop\_shipment\_details\]

</td><td>

Stores the shipment details that are associated with a purchase order line.

</td></tr><tr><td>

Shipment Product

 \[sn\_shop\_shipment\_product\]

</td><td>

Stores the shipment product details that are associated with a purchase order line.

</td></tr><tr><td>

Shipping Method

 \[sn\_shop\_shipping\_method\]

</td><td>

Stores the shipping method details that are associated with a purchase order line.

</td></tr></tbody>
</table>**Note:** The following tables are installed as part of the Sourcing and Purchasing Automation application.

<table id="table_yct_jwt_d5b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Acknowledgment Task

 \[sn\_shop\_acknowledgment\_task\]

</td><td>

Stores acknowledgments such as the milestone and receipt task. This is a parent table within the Common Service Delivery \(SDC\) application.

</td></tr><tr><td>

Approval Plan

 \[sn\_shop\_approval\_plan\]

</td><td>

Stores the approval plan details for a purchase requisition such as the approval routing method and approval decision method.

</td></tr><tr><td>

Approval Plan Detail

 \[sn\_shop\_approval\_plan\_detail\]

</td><td>

Stores an instance of the approval record for a purchase line that is created based on the approval plan.

</td></tr><tr><td>

Approval Rule

 \[sn\_shop\_approval\_rule\]

</td><td>

Stores the rule that triggers the creation of an approval record. It uses a condition builder to build the trigger condition for approvals.

</td></tr><tr><td>

Capitalization Policy

 \[sn\_shop\_capitalization\_policy\]

</td><td>

Stores the condition based on which an asset is capitalized, and a fixed asset record is created.

</td></tr><tr><td>

Cart Line

 \[sn\_shop\_cart\_line\]

</td><td>

Stores the details of a purchase line that is added to a cart. It has various details such as the supplier product selected, checkout type, business owner, delivery location, and so on.

</td></tr><tr><td>

Contract Task

 \[sn\_shop\_contract\_task\]

</td><td>

Extends the Purchasing Task table and stores instances of various types of contract tasks that are associated with a purchase line.

</td></tr><tr><td>

Purchase Cost Allocation

 \[sn\_shop\_cost\_allocation\]

</td><td>

Stores the type of cost allocation, associated cost center, and the amount that is allocated for a shopper that can be used to buy a supplier product.

</td></tr><tr><td>

Credit Allocation Rules

 \[sn\_shop\_credit\_allocation\_rules\]

</td><td>

Stores the credit allocation rules that are based on how a credit is allocated to an individual shopper. The allocation can be based on the inventory asset or user condition.

</td></tr><tr><td>

Delivery Address Task

 \[sn\_shop\_delivery\_address\_task\]

</td><td>

Extends the Purchasing Task table and stores the tasks that are associated with verifying and validating the delivery location for a purchase line.

</td></tr><tr><td>

Employee Credit

 \[sn\_shop\_employee\_credit\]

</td><td>

Stores the credit amount that is allocated for a user with supporting information such as the responsible cost center and credit allocation rule.

</td></tr><tr><td>

Ledger Assignment Rules

 \[sn\_shop\_ledger\_assignment\_rule\]

</td><td>

Stores the rules that apply to the supplier products, product model or product category, and cost center. These rules are based on the accounting details, such as the capex and expense accounts, that are populated on a purchase line.

</td></tr><tr><td>

Model Map

 \[sn\_shop\_m2m\_model\_map\]

</td><td>

Stores the mapping between a CMDB model and a third-party category.

</td></tr><tr><td>

Negotiation

 \[sn\_shop\_negotiation\]

</td><td>

Stores the negotiation object that is created for a supplier product in a sourcing activity.

</td></tr><tr><td>

Negotiation Event

 \[sn\_shop\_negotiation\_event\]

</td><td>

Stores the sourcing events that are created for a supplier product in a sourcing activity.

</td></tr><tr><td>

Non Catalog Intake

 \[sn\_shop\_non\_catalog\_intake\]

</td><td>

Extends the Import Set Row table and acts like a staging table for the non-catalog intake flow.

</td></tr><tr><td>

Order Permission

 \[sn\_shop\_m2m\_order\_users\_covered\]

</td><td>

Stores the mapping between the purchasing permission and purchase order.

</td></tr><tr><td>

Paycheck Periods

 \[sn\_shop\_paycheck\_periods\]

</td><td>

Stores the number of paychecks through which a payment would be made.

</td></tr><tr><td>

Payment Methods

 \[sn\_shop\_payment\_method\]

</td><td>

Stores the payment method that is selected by the shopper and the cost center or person responsible for the payment.

</td></tr><tr><td>

Percent Complete Configuration

 \[sn\_shop\_percent\_complete\_config\]

</td><td>

Stores the configurations to determine the percentage of payment that is completed for an order.

</td></tr><tr><td>

Pre-Payment

 \[sn\_shop\_pre\_payment\]

</td><td>

Stores a record of prepayment done for a purchase line as per a contract.

</td></tr><tr><td>

Product Purchases by Job Code

 \[sn\_shop\_user\_product\_purchase\]

</td><td>

Stores the aggregation of products purchased by the job code.

</td></tr><tr><td>

Product Stage

 \[sn\_shop\_imp\_product\]

</td><td>

Extends the Import Set Row table. This staging table is used to import supplier products.

</td></tr><tr><td>

Properties

 \[sn\_shop\_properties\]

</td><td>

Stores the Shopping Hub specific properties such as the requisition auto order.

</td></tr><tr><td>

Purchase

 \[sn\_shop\_purchase\]

</td><td>

Stores the purchase record that is created for each purchasing or sourcing activity.

</td></tr><tr><td>

Purchase Line

 \[sn\_shop\_purchase\_line\]

</td><td>

Extends the Request Line table and stores the purchase line that is associated with a purchasing or sourcing activity.

</td></tr><tr><td>

Purchase Order History

 \[sn\_shop\_order\_history\]

</td><td>

Extends the Order Template table and stores the older purchase order record when an order is revised.

</td></tr><tr><td>

Purchase Order Line History

 \[sn\_shop\_order\_line\_history\]

</td><td>

Extends the Order Line Template table and stores the older purchase order line record when a purchase order line is revised.

</td></tr><tr><td>

Purchase Requisition

 \[sn\_shop\_purchase\_requisition\]

</td><td>

Stores the purchase requisition for a purchase or sourcing activity.

</td></tr><tr><td>

Purchases by Category

 \[sn\_shop\_user\_category\_purchase\]

</td><td>

Stores the analytical data for purchases by product category.

</td></tr><tr><td>

Purchasing Permission

 \[sn\_shop\_covered\_user\]

</td><td>

Stores the purchasing permission for a user, group, cost center, or department.

</td></tr><tr><td>

Purchasing Task

 \[sn\_shop\_task\]

</td><td>

Stores the various tasks that are associated with a purchase such as finance and contract tasks. This is a base table within the Common Service Delivery \(SDC\) application.

</td></tr><tr><td>

Receipt Task

 \[sn\_shop\_receipt\_task\]

</td><td>

Extends the Acknowledgment Task table and stores the state of a receipt confirmation.

</td></tr><tr><td>

Request Line Template

 \[sn\_shop\_request\_line\]

</td><td>

Extends the Shop Line table and stores the purchase request line items.

</td></tr><tr><td>

Requisition Permission

 \[sn\_shop\_m2m\_purchasing\_users\_covered\]

</td><td>

Stores the mapping between the purchasing permission and purchase requisition.

</td></tr><tr><td>

Requisition to Contract Relationships

 \[sn\_shop\_m2m\_requisition\_contract\]

</td><td>

Stores the mapping between the requisition and contract.

</td></tr><tr><td>

Revision Line

 \[sn\_shop\_rev\_request\_line\]

</td><td>

Extends the Request Line Template table and stores the revision line for a purchase.

</td></tr><tr><td>

Revision Request

 \[sn\_shop\_revision\_request\]

</td><td>

Extends the Purchasing Task table and stores the state of a revision request for a purchase.

</td></tr><tr><td>

Service Acknowledgment

 \[sn\_shop\_service\_acknowledgment\]

</td><td>

Stores the acknowledgment tasks of services received.

</td></tr><tr><td>

Shop Line

 \[sn\_shop\_line\]

</td><td>

Stores the order line template and request line template. This is a base table.

</td></tr><tr><td>

Shopper's Top Suppliers

 \[sn\_shop\_usr\_preferred\_supplier\]

</td><td>

Stores the mapping between the shopper and preferred supplier.

</td></tr><tr><td>

Shopping Control

 \[sn\_shop\_shopping\_control\]

</td><td>

Stores the security rules that determine the access of supplier products for a given user.

</td></tr><tr><td>

ShoppingHub API Cache

 \[sn\_shop\_shopnow\_api\_cache\]

</td><td>

Stores the cached data for quicker access by APIs. An example is the CachedCagetoryMap.

</td></tr><tr><td>

ShoppingHub Configuration

 \[sn\_shop\_shopnow\_content\]

</td><td>

Stores configurations that determine certain aspects of the application appearance and behavior. An example is the terms and conditions page URL.

</td></tr><tr><td>

Sourcing Bid Stage

 \[sn\_shop\_imp\_sourcing\_bid\]

</td><td>

Stores the bids that are received for a supplier product by the third-party providers. This is a staging table.

</td></tr><tr><td>

Sourcing Line Outbound Queue

 \[sn\_shop\_sourcing\_line\_out\_queue\]

</td><td>

Stages the sourcing line for the third-party providers.

</td></tr><tr><td>

Sourcing Outbound Queue

 \[sn\_shop\_sourcing\_out\_queue\]

</td><td>

Stages the sourcing request for the third-party providers.

</td></tr><tr><td>

Sourcing Request

 \[sn\_shop\_sourcing\_activity\]

</td><td>

Stores requests to source for supplier products.

</td></tr><tr><td>

Sourcing Task

 \[sn\_shop\_sourcing\_task\]

</td><td>

Extends the Purchasing Task table and stores the tasks that are related to a sourcing request.

</td></tr><tr><td>

Sourcing Vendor

 \[sn\_shop\_sourcing\_vendor\]

</td><td>

Stores the mapping between the sourcing vendor code and sourcing vendor name.

</td></tr><tr><td>

Supplier Product

 \[sn\_shop\_supplier\_product\]

</td><td>

Stores the supplier products that represent goods or services that can be listed on the portal.

</td></tr><tr><td>

Supplier Product View

 \[sn\_shop\_supplier\_product\_view\]

</td><td>

Stores the analytics of the number of views for a supplier product.

</td></tr><tr><td>

Supplier Use by Department

 \[sn\_shop\_dept\_supplier\_purchase\]

</td><td>

Stores the analytics of suppliers that are used by departments.

</td></tr><tr><td>

Supplier Use by Shopper

 \[sn\_shop\_user\_supplier\_purchase\]

</td><td>

Stores the analytics of suppliers that are used by shoppers.

</td></tr><tr><td>

Third-Party Category

 \[sn\_shop\_third\_party\_category\]

</td><td>

Stores an external category that is provided by a supplier that maps to an existing model.

</td></tr><tr><td>

User Controls

 \[sn\_shop\_user\_control\]

</td><td>

Stores the mapping of a user and a shopping control.

</td></tr></tbody>
</table>## Purchasing properties

The following list contains the purchasing properties that are used by Sourcing and Procurement Operations.

|Property|Description|
|--------|-----------|
|sn\_shop.atf.threshold.days|Number of days before an expected delivery date for goods, or a start date for services and blankets, in which time a purchase requisition would be considered after the fact.|
|sn\_shop.credit.allocation.batchsize|Total number of employee records that are processed in a batch, during credit allocation.|
|sn\_shop.default.contract.model.type|Default contract model when creating contracts.|
|sn\_shop.default.purchasing.time|Initial value of the purchasing time in days.|
|sn\_shop.default.shipping.estimate|Default shipping estimate, in percentage.|
|sn\_shop.default.sourcing.time|Initial sourcing time in days.|
|sn\_shop.default.supplier.onboard.time|Initial supplier onboarding time in days.|
|sn\_shop.non.pricing.contract|List of non-pricing contracts. The default is NDA.|
|sn\_shop.shipping.estimate.inclusion|Shipping estimate included in purchase request approvals.|
|sn\_shop.approval.reassessment.resend|Approvals that must be reassessed during a revision if the same approval rule is triggered. It applies to both purchase requisition and purchase order revisions.|
|sn\_shop.log.property|Logging level for Sourcing and Purchasing Automation.|
|sn\_shop.spend.requisition.autoorder|Purchase order that can be automatically created on completion of purchasing tasks without having to undergo a manual final review.|
|sn\_shop.spend.requisition.autoorder.threshold|Dollar amount threshold above which a final review is required before a purchase order is created even when the automatic creation of purchase orders property is set to Yes.|
|sn\_shop.spend.sla.due.days|Minimum due date for SLA calculation.|
|sn\_shop.supported.artifact.formats|Formats that are supported for supplier product artifacts.|
|sn\_shop.tax.estimate.inclusion|Includes generated tax estimate in purchase requests for the approval process.|

## Watchlist properties

Set the `sn_shop.watchlist.user.limit` system property to restrict the maximum number of users in the watchlist to 20.

Role required:

-   sn\_shop.procurement\_administrator, sn\_shop.shopping\_hub\_admin - Edit and view.
-   sn\_shop.procurement\_administrator, sn\_shop.shopping\_hub\_admin, sn\_shop.shopper, sn\_shop.procurement\_specialist, sn\_spend\_psd.agent - View \(read-only\).

To modify the user limit, do the following:

1.  Navigate to **All**.
2.  On the left navigation pane, enter `sys_properties_list.do`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

3.  In the Name search field, look for **sn\_shop.watchlist.user.limit** and open the system property.

    The system property **sn\_shop.watchlist.user.limit** opens as a record. The **Value** field displays the default value as 20. You can edit the record in editing mode.

4.  In the **Value** field, you can modify the value as per your requirement.

    For example, 5.

5.  Select **Update**.

## Property to automate the edit receipt flow

Enable the s`n_spend_cp.enable_automated_edit_receipt_flow` system property to automate the approval and processing of edit receipt requests without manual intervention. The automated process updates the purchase order \(PO\) and purchase order line \(POL\) quantities, while also automatically closing the associated procurement case in the Source-to-Pay Workspace.

Role required: admin

This property is enabled by default. However, if this property is disabled, do the following to enable it:

1.  Navigate to **All**.
2.  On the left navigation pane, enter `sys_properties_list.do`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

3.  In the Name search field, look for **sn\_spend\_cp.enable\_automated\_edit\_receipt\_flow** and open the system property.

    The system property is enabled by default. The **Value** field displays the default value as **ON**.

4.  If the **Value** field shows **OFF**, change it to **ON** to enable this property.
5.  Select **Update**.

**Parent Topic:**[Install Sourcing and Procurement Operations](../task/activate-finance-spend-central.md)

