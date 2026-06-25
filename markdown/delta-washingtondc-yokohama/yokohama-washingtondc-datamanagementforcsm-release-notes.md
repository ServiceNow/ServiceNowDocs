---
title: Combined Data management for CSM release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for Data management for CSM from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-datamanagementforcsm-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 16
breadcrumb: [Products combined by family]
---

# Combined Data management for CSM release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for Data management for CSM from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Data management for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Data management for CSM to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Data management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Product instance identifier](https://www.servicenow.com/docs/access?context=create-a-sync-between-an-install-base-class-and-asset-class&family=washingtondc&ft:locale=en-US)**

Connect new and existing products and services with the related assets and configurations by using the product instance identifier.

Link the install base items to an asset class, configuration item class, and product model class by using the **Model Category** field.

-   **[Synchronization of life-cycle states between the asset and install base](https://www.servicenow.com/docs/access?context=synchronizing-install-base-lifecycle-fields-state-field&family=washingtondc&ft:locale=en-US)**

Synchronize the **State** field across both the asset class and install base class to maintain the consistency of states between both entities. The synchronization of the **State** fields depends on the states that you select in the life-cycle fields.

Comply with the Common Service Data model framework by establishing a link between the existing **State** field and the new life-cycle fields on the install base form.

-   **[Data model for Sold products and Install base](https://www.servicenow.com/docs/access?context=create-sold-item&family=washingtondc&ft:locale=en-US)**

Create an install base item by using the **Specification** field on the install Base form during order fulfillment.

Support life-cycle management workflows for sold products by using the fields that are added to the Sold products table.

-   **[Sales and Order Management workflows](https://www.servicenow.com/docs/access?context=lead-to-cash-workflows&family=washingtondc&ft:locale=en-US)**

Configure the metadata for the lead-to-cash entities by mapping the entities and configurations.

Use the lead-to-cash operations like Create Instance, Delta, Effect, and Commit Instance to compose and build workflows for a seamless flow of information between entities. To learn more, see [LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&family=washingtondc&ft:locale=en-US).

-   **[Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&family=washingtondc&ft:locale=en-US)**

Manage the life cycle of your sold products by activating the Customer Life Cycle Management workflows \(com.snc.customer\_lifecycle\_mgmt\_workflows\) store application.

Update the existing products and services by triggering the sold product to order and the order to sold product flows. You use the **Modify**, **Suspend**, **Resume**, and **Disconnect** actions on the sold product related list on the accounts page to trigger this flow.

Change the current configuration of the sold product on the Configurator UI by performing the **Modify** action.

Make a definite or indefinite suspension of a sold product by using the **Suspend** action.

Restart the services of a disconnected or suspended sold product by using the **Resume** action.

Make the sold product inactive by disconnecting a sold product and its full hierarchy.

-   **[\[Placeholder link text to key lead-to-cash-workflows\]](https://www.servicenow.com/docs/access?context=lead-to-cash-workflows&family=washingtondc&ft:locale=en-US)**

Use metadata configurations to transform data and define structures and workflows like Leads, Opportunities, Orders, Install base items, Sold products and more.

-   **[Unified User-Employee as a Consumer](https://www.servicenow.com/docs/access?context=configuring-employee-as-a-consumer&family=washingtondc&ft:locale=en-US)**

Create a single, unified profile that supports both the internal and external personas from login through all interactions across the Customer Service Management product.

-   **[Business Location 360](https://www.servicenow.com/docs/access?context=using-blsp-portal&family=washingtondc&ft:locale=en-US)**

Enable agents to accurately resolve reported business location issues by using the business location 360 template. Your agents can add data sources, display extra information, and represent entities, such as stores, government agencies, healthcare organizations, automotive dealerships, or departments, for enhanced contextual insights.

-   **[Omni-channel support for the business location staff](https://www.servicenow.com/docs/access?context=add-staff-memers-to-biz-location&family=washingtondc&ft:locale=en-US)**

Enable your business location staff to interact and record all support interactions with each business location through omni-channel capabilities, including Virtual Agent, chat, and messaging applications.​


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Unified user - employee as a consumer](https://www.servicenow.com/docs/access?context=features-supp-and-unsupp-by-unified-consumer&family=xanadu&ft:locale=en-US)**

Update the additional features and workflows, such as the case types Order Management, and Field Service Management integration, to support the unified consumer \(sn\_customerservice.unified\_consumer\) role.

-   **[Inter-organization support](https://www.servicenow.com/docs/access?context=setup-bus-loc-serviced-by-bus-loc&family=xanadu&ft:locale=en-US)**

Enable your agents to get visibility into the business locations that they support so that they can resolve issues efficiently. You can provide the agents that are assigned to the fulfilling service organization with access to the cases, install base items, sold products, and member details of all the requesting service organizations that they’re assisting.

-   **[External business location as a fulfiller](https://www.servicenow.com/docs/access?context=industry-data-model-cases&family=xanadu&ft:locale=en-US)**

Enable external business locations such as partners, external agencies, and franchises to fulfill customer cases with store-related issues.

-   **[Associating assignment groups with a business location](https://www.servicenow.com/docs/access?context=setting-up-assignment-groups&family=xanadu&ft:locale=en-US)**

Associate groups with an internal or external business location through a one-to-many \(1:M\) relationship, which means that one or more assignment groups can be associated with a business location.

-   **[Install Base hierarchy visualization](https://www.servicenow.com/docs/access?context=install_base_hierarchy_visualisation&family=xanadu&ft:locale=en-US)**

View the entire hierarchy of an install base item by using the **Install Base hierarchy** tab on the CSM Configurable Workspace. You can expand the multiple nodes of the hierarchy and create cases for the install base item.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Naming customer relationship records](https://www.servicenow.com/docs/access?context=adding-related-party-to-case&family=yokohama&ft:locale=en-US)**

Use the Type field through related party configurations to name records in the account team member, contact relationship, consumer relationship, and household member relationship tables. With this functionality, you can identify the relationship that is based on the industry use case.

-   **[Ordering customer relationship records](https://www.servicenow.com/docs/access?context=adding-related-party-to-case&family=yokohama&ft:locale=en-US)**

Organize records in tables such as account team members, consumer relationships, and more by using the **Order** field. You can set the order manually or auto-populate it based on the selected Type through related party configurations. This way, you can arrange records logically based on your use case.

-   **[Enhancements to the declarative responsibility framework](https://www.servicenow.com/docs/access?context=declarative-resposibility-framework&family=yokohama&ft:locale=en-US)**

Enhance the declarative responsibility framework to simplify administration and access management by enabling administrators to do the following tasks:

    -   Add new granular roles for accessing customer data that is based on responsibility definitions.
    -   Include additional entities in the framework.
-   **[Subscription metrics for sold products](https://www.servicenow.com/docs/access?context=create-sold-item&family=yokohama&ft:locale=en-US)**

Enable agents to track and analyze the pricing information for products and services by using the pricing and subscription revenue metrics on the sold product form on the CSM Configurable Workspace.

-   **[Project Management for business locations​](https://www.servicenow.com/docs/access?context=csm-ppm-integration&family=yokohama&ft:locale=en-US)**

Integrate SPM project management with business locations to support operations such as opening, closing, or modernizing locations. With the project management integration, your teams can track the timelines, collaborate, and execute the business location-facing tasks more effectively.

-   **[Work orders for business locations​](https://www.servicenow.com/docs/access?context=track-work-orders-on-the-blsp&family=yokohama&ft:locale=en-US)**

Fulfill Field Service Management \(FSM\) work orders at business locations. This way, you can enable location members to view and complete the assigned tasks. By using the existing business location data, you can streamline work order assignments.

-   **[Enhanced data fields for business locations](https://www.servicenow.com/docs/access?context=data-model-business-location-form&family=yokohama&ft:locale=en-US)**

Track additional information about business locations by using new fields for opening and closing dates, status, and description.

-   **[Staff movement between internal business locations](https://www.servicenow.com/docs/access?context=create-internal-business-location&family=yokohama&ft:locale=en-US)**

Enable managers to transfer the staff between internal business locations. You can streamline updates for organizations that have frequent staff movements.

-   **[Company-owned, third-party operated business locations](https://www.servicenow.com/docs/access?context=add-user-internal-bus-location&family=yokohama&ft:locale=en-US)**

Assign external staff to internal business locations to support various operating models, including company-owned, third-party operated locations.

-   **[Customer Life Cycle workflows for Sold Products and Product Inventory records](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&family=yokohama&ft:locale=en-US)**

Use the Customer Life Cycle workflows to do the following tasks:

    -   Create a Modify, Suspend, Resume, and Disconnect order for single or multiple root product inventory records that are associated with a service specification.
    -   Select multiple root product inventories to perform the modify action to create both orders and quotes.
    -   Track the status of the Modify, Suspend, Resume, and Disconnect flows on sold products and product inventory record by using the Sales and Order Management Request Tracker \(sn\_tmt\_core\_inbound\_queue\) table.
-   **[Inbound Request Configuration table](https://www.servicenow.com/docs/access?context=inbound-request-configuration-table&family=yokohama&ft:locale=en-US)**

Use the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table to enable configurations that determine how a flow is executed, whether synchronous or asynchronous.

Use the **Trigger Notifications** field on the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table to enable configuration of notification types, whether default, custom,or no notifications.

-   **[Activate Customer Life Cycle Management Self-Service](https://www.servicenow.com/docs/access?context=activate-customer-life-cycle-management-self-service&family=yokohama&ft:locale=en-US)**

Enable customers who are primary contacts associated to a sold product to perform the Modify, Suspend, Resume, and Disconnect actions on the Business portal.

.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Data management for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Transfer related party configurations to sys\_metadata](https://www.servicenow.com/docs/access?context=csm-cust-access-mgmt-tables&family=washingtondc&ft:locale=en-US)**

Transfer the Related Party Configuration \[sn\_customerservice\_related\_party\_configuration\] table to the Application File \[sys\_metadata\] table across customer instances by using the update sets.

-   **[Associate an existing user to a consumer record](https://www.servicenow.com/docs/access?context=associate-an-existing-user-to-a-consumer&family=washingtondc&ft:locale=en-US)**

Starting with the Washington DC release, only administrators can associate a user with the consumer record.

-   **[Create users through the User lookup list on the Consumer form](https://www.servicenow.com/docs/access?context=create-consumer-users&family=washingtondc&ft:locale=en-US)**

Starting with the Washington DC release, you can create sys\_users directly from the User lookup list on the consumer form. This functionality applies to both internal \(snc\_internal\) and external \(snc\_external\) users.

-   **[Integrate the Service Model Foundation with request management](https://www.servicenow.com/docs/access?context=csm-integration-sm-request&family=washingtondc&ft:locale=en-US)**

Monitor the case progress as a business location staff member directly from the Business Location Service Portal \(BLSP\) after you submit a catalog request.

-   **[Support case creation for an external business location \(EBL\) staff](https://www.servicenow.com/docs/access?context=track-cases-for-blsp-portal&family=washingtondc&ft:locale=en-US)**

Enable your internal business location \(IBL\) and external business location \(EBL\) staff to track issues. Your staff can track cases on behalf of a business location against sold products that are deployed at a business location or against installed base items that are deployed at a business location.

-   **[Sales and Order Management core](https://www.servicenow.com/docs/access?context=lead-to-cash-workflows&family=washingtondc&ft:locale=en-US)**
    -   Use the enhanced entity configuration types to support covered products along with other context types like transaction headers, lines, charactersitics, and pricing adjustments.
    -   Support the multi-instance selection for different sales and order management workflows. For example, select multiple sold products to perform the **Move**, **Add**, **Change** functions.
-   **[\[Placeholder link text to key customer-life-cycle-management-workflows\]](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&family=washingtondc&ft:locale=en-US)**

Create a quote with the **Modify** action by updating the characteristics of an existing sold product, by adding new products or disconnecting existing products.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Unparenting service organizations from a company](https://www.servicenow.com/docs/access?context=associate-company-with-bus-loc&family=xanadu&ft:locale=en-US)**

Enhanced the adoption of the service organization model to accommodate the various industry verticals, such as Healthcare and Life Sciences Service Management, Public Sector Digital Services, and Financial Services Operations, by unparenting the service organizations from the company table.

-   **[Field Service Management integration with Service Model Foundation](https://www.servicenow.com/docs/access?context=track-work-orders-on-the-blsp&family=xanadu&ft:locale=en-US)**

Enabled your location staff to track the work orders for their business locations by using the business location service portal \(BLSP\).

-   **[Data model for sold products](https://www.servicenow.com/docs/access?context=create-sold-item&family=xanadu&ft:locale=en-US)**
    -   You can now view the Provider Service Organization information that has sold a product or service to the customer on the Sold Product form.
    -   You can now use the **Product Location** and **Product Specification** fields on the Sold Product table \(sn\_install\_base\_sold\_product\) to capture information about the location of the sold product and the sold product that is associated with an offer.
-   **[Product Instance directive for Install Base Management](https://www.servicenow.com/docs/access?context=create-a-sync-between-an-install-base-class-and-asset-class&family=xanadu&ft:locale=en-US)**

Synchronized the changes between the asset and corresponding install base hierarchy with the extended product instance hierarchy.

-   **[Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&family=xanadu&ft:locale=en-US)**

You can now select multiple sold products at the same time to trigger the **Suspend**, **Resume**, and **Disconnect** flows to update the existing root sold products and their services.


-   **[Compose Sales and Order Management workflows](https://www.servicenow.com/docs/access?context=compose_sales_and_order_management_workflows&family=xanadu&ft:locale=en-US)**

You can now use the sales and order management API to support use cases for order reconfiguration. To learn more about reconfiguration, see [LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&family=xanadu&ft:locale=en-US).


-   **[\[Placeholder link text to key update\_product\_inventory\_configurations\]](https://www.servicenow.com/docs/access?context=update_product_inventory_configurations&family=xanadu&ft:locale=en-US)**
    -   Perform **Modify**, **Suspend**, **Resume**, and **Disconnect** actions on product inventory records from the Product Inventories related list.

**Note:** The Product Inventories related list is available only from the Yokohama release. If you're using the Washington or Xanadu versions, you can manually add the related list.

To retain both the Product Inventory and Sold product related lists, filter out the product inventory records from the sold product list. Use the product inventories related list to perform the MACD actions.


-   **Sales and Order Management Request tracker**
    -   Monitor the status of sales and order management workflows and enable agents to track the status of synchronous and asynchronous flows.
    -   Use the enhances inbound Queue to view detailed request information for the sales and order management workflows and improve user experience.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Product Inventories configurations for Customer Life Cycle Management workflows](https://www.servicenow.com/docs/access?context=product_inventory_configurations&family=yokohama&ft:locale=en-US)**

Perform the Modify, Suspend, Resume, and Disconnect operations on product inventory records directly from the Product Inventory related list on the Accounts page.

-   **[Grant write access to account relationships](https://www.servicenow.com/docs/access?context=t_CreateAcctRelationshipRecord&family=yokohama&ft:locale=en-US)**

Enable administrators and customer service managers to update account relationship records.

-   **[Enable write access to contact relationships](https://www.servicenow.com/docs/access?context=t_CreateAContactRelationship&family=yokohama&ft:locale=en-US)**

Enable administrators and customer service managers to update the contact relationship records.

-   **[Populate the Type field in relationship tables using the fix script](https://www.servicenow.com/docs/access?context=migration-of-account-manager-responsibility-access&family=yokohama&ft:locale=en-US)**

Migrate the account manager responsibilities from the account team member relationships to the new responsibility access configurations. The updated framework enables you to manage access settings more efficiently.

-   **[Update roles within relationship agent and relationship contributor](https://www.servicenow.com/docs/access?context=features-supp-and-unsupp-by-unified-consumer&family=yokohama&ft:locale=en-US)**

Modify the roles of the relationship agent and relationship contributor to include the new granular roles that can grant access by responsibilities.

-   **[Notification for case tasks at business locations](https://www.servicenow.com/docs/access?context=manage-business-location-cases&family=yokohama&ft:locale=en-US)**

View the notifications for the case tasks that are associated with the business locations on the Business Location Service Portal \(BLSP\). This way, your location members can stay informed about their pending tasks.

-   **[Case resolution by location staff at other business locations](https://www.servicenow.com/docs/access?context=ebl-as-a-fulfiller&family=yokohama&ft:locale=en-US)**

Enable your location staff, whether at company-owned or third-party-owned organizations \(internal and external business locations\), to handle and resolve issues from other eligible business locations.

-   **[Inbound Request Configuration table](https://www.servicenow.com/docs/access?context=inbound-request-configuration-table&family=yokohama&ft:locale=en-US)**

The Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table is renamed to Inbound Request table.

Use the **Request Configuration** field on the Inbound Request \[sn\_tmt\_core\_inbound\_queue\] table to reference the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table while executing synchronous or asynchronous flows.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Data management for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Data management for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Data management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Customer Service Management is a ServiceNow AI Platform feature that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=washingtondc&ft:locale=en-US).

 Additional Customer Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&family=washingtondc&ft:locale=en-US).

 Sales and Order Management is a Order Management feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\).

</td></tr><tr><td>

Xanadu

</td><td>

Customer Service Management is a ServiceNow AI Platform feature that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=xanadu&ft:locale=en-US).

 Additional Customer Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&family=xanadu&ft:locale=en-US).

 Sales and Order Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Exploring Sales and Order Management](https://www.servicenow.com/docs/access?context=som-exploring&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Customer Service Management is a ServiceNow AI Platform feature that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=yokohama&ft:locale=en-US).

 Additional Customer Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&family=yokohama&ft:locale=en-US).

 Sales and Order Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Exploring Sales and Order Management](https://www.servicenow.com/docs/access?context=som-exploring&family=yokohama&ft:locale=en-US).

 Starting from the Yokohama release, the following plugins are available on ServiceNow Store for quicker and better maintenance:

-   Install Base Management \(com.snc.install\_base\)
-   Install base characteristics \(com.snc.install\_base\_characteristics\)
-   Customer Service with Service Portfolio management \(com.snc.csm\_spm\)

For details, see [Configure install base](https://www.servicenow.com/docs/access?context=configure-install-base&family=yokohama&ft:locale=en-US).

 Starting from the Yokohama release, the Business Location plugin \(com.snc.business\_location\) is available on ServiceNow Store for quicker and better maintenance. For details, see [Activate business locations](https://www.servicenow.com/docs/access?context=activate-business-location&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Data management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Data management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Starting with the Washington DC release, ServiceNow® Data Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Starting with the Xanadu release, ServiceNow® Data Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Starting with the Yokohama release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Data management for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Data management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Data management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Support workflows with the enhanced data model changes in the sold product table.
-   Use contracts and entitlements that are also modeled as sold products and are part of the hierarchy so that you can have complete information about the sold product and its services.
-   Identify and track the new and existing install base items by using the product instance identifier.
-   Unify a user's identity personas so that you don't need to create and manage multiple user accounts for a single user. With this feature, you can seamlessly provision business-to-consumer \(B2C\) services.
-   Get a comprehensive, 360-degree view of the business location issues so that your agents get the required contextual data to effectively resolve the reported issues.

 See [Data management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-data-management&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Enable your agents to get visibility into the business locations that they support by using the inter-organization support functionality.
-   Enhance the adoption of the service organization data model by unparenting service organizations from the company table.
-   Use the Provider Service Organization information of a sold product to enable agents to create cases.

 See [Data management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-data-management&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Track the status and other information that is related to the Customer Life Cycle workflows by using the Sales and Order Management Request Tracker \(sn\_tmt\_core\_inbound\_queue\) table.
-   Track pricing and subscription information for products and services on the CSM Configurable Workspace by using the revenue metrics on the sold product form.
-   Integrate Strategic Portfolio Management \(SPM\) project management with business locations to create and manage projects across your organization.

 See [Data management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-data-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

