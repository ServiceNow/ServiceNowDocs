---
title: Using Software Asset Workspace
description: Use the Software Asset Workspace, the intuitive and streamlined user interface of the Software Asset Management application, to manage software licenses, compliance, and optimization.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-03-05"
reading_time_minutes: 8
breadcrumb: [Software Asset Management, IT Asset Management]
---

# Using Software Asset Workspace

Use the Software Asset Workspace, the intuitive and streamlined user interface of the Software Asset Management application, to manage software licenses, compliance, and optimization.

-   **[Create entitlements in workspace](../task/create-entitlements-workspace.md)**  
Create entitlements in the Software Asset Workspace to enter your license details and allocate purchased software rights to users or devices.
-   **[Import bulk entitlements in workspace](../task/import-entitlements-workspace.md)**  
You can import multiple entitlements at one go in the Software Asset Workspace.
-   **[Install Software Asset Management Guided Experiences](../task/install-sam-playbook.md)**  
Install the Software Asset Management Guided Experiences \(com.sn\_sam\_playbook\) application for step-by-step guidance for completing tasks in your daily software management activities. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.
-   **[Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md)**  
Use the guided walk-through playbook for a step-by-step process of creating entitlements.
-   **[Create software models in workspace](../task/create-swmodels-workspace.md)**  
Create a software model in the Software Asset Workspace to add product details that are used to connect software rights you purchased with software installations discovered on your system.
-   **[Run software reconciliation in the workspace](../task/run-recon-workspace.md)**  
Reconciliation is run as a scheduled job \(default is weekly\), but you can also run reconciliation manually to reconcile software products in the Software Asset Workspace environment on-demand.
-   **[Create a software removal candidate in workspace](../task/add-sw-removal-workspace.md)**  
Removal candidates reclaim software resources in your environment. They are created automatically from reclamation rules or can be created manually.
-   **[Create device allocation](../task/create-device-allocation.md)**  
Create a device allocation for a software entitlement to specify devices that have been granted rights.
-   **[Copy user or device allocations](../task/copy-allocations.md)**  
Copy user or device allocations from one entitlement to the other.
-   **[Create consumption rules](../task/create-consumption-rule.md)**  
Create consumption rules to restrict license consumption to certain entities within your organization.
-   **[Link consumption rules to entitlements](../task/link-consumption-rules.md)**  
After you've created a consumption rule, you must link the rule to one or more entitlements.
-   **[View discovered engineering licenses in workspace](../task/view-disco-englicenses-workspace.md)**  
View a list of all the discovered and normalized software for your engineering applications in the Software Asset Workspace.
-   **[View engineering license servers in workspace](../task/view-englicenses-server-workspace.md)**  
View the list of license management servers that OpenLM or Open iT connect with to get data into your ServiceNow instance in the Software Asset Workspace.
-   **[Add custom software products in workspace](../task/add-custom-software-products-workspace.md)**  
Add a custom software product for any publicly available software product that does not exist in the Software Asset Management Content Library. Custom software products enable you to normalize and account for software products that aren’t part of the Software Asset Management Content Library yet.
-   **[View custom software product suggestions in workspace](../task/view-custom-software-product-suggestions-workspace.md)**  
View the product suggestions that enable you to consolidate your custom software products with corresponding software products in the Software Asset Management Content Library. By consolidating these software products, you can update all references to your custom software products with references to the software products in the Content Library. You can choose to accept or reject these suggestions.
-   **[View license usage for your installations](../task/view-install-usage.md)**  
Track your installation to license journey by connecting software installations to the licenses consumed and identifying statuses such as licensed, unlicensed, ignored, or requiring action.
-   **[Create averages for product life cycles in workspace](../task/create-lifecycle-averages-workspace.md)**  
Create averages to calculate software End of Life \(EOL\) and End of Support \(EOS\) life cycles in the Software Asset Workspace.
-   **[View normalization suggestions in workspace](../task/view-norm-sugg-workspace.md)**  
View normalization suggestion records in the Software Asset Workspace that are created for discovery models. You can accept or reject these suggestions.
-   **[Revert normalization in the workspace](../task/revert-norm-workspace.md)**  
You can revert the normalization of discovery models in the Software Asset Workspace.
-   **[Manually override edition value in workspace](../task/manually-override-edvalue-workspace.md)**  
If the edition of a software installation is not automatically discovered, you can specify the edition on the Software Installation form \(if known\) so the software can be successfully reconciled.
-   **[Manually normalize a software model in workspace](../task/manual-normalize-swmodel-workspace.md)**  
You can manually normalize a software discovery model that has not been fully normalized \(partially normalized, publisher normalized, or match not found\) in order to reconcile it.
-   **[Create parent-child relationships between software products](../task/create-parent-child-relationships-between-software-products.md)**  
Create and define the parent-child relationships between your software products so that your child products can inherit life-cycle dates from their parent products.
-   **[View the Export Classification Control Number \(ECCN\) mappings for your software products](../task/view-eccn-software-mappings.md)**  
View the list of ECCNs that are mapped to your software products. Use this information to identify the products that are subject to U.S. export control regulations.
-   **[View or create software usage](../task/view-sw-usage-workspace.md)**  
View software usage records to track the usage of software products that you have created reclamation rules for. You can also create software usage records manually from third party integrations or Microsoft SCCM integrations.
-   **[View SAP engines in workspace](../task/sap-engines-workpace.md)**  
View the monthly engine usage measurements for SAP clients based on the license metric for each engine.
-   **[View SAP users in workspace](../task/view-sapusers-workspace.md)**  
View all the discovered users pulled from the SAP systems in the Software Asset Workspace.
-   **[Create a custom named user type in workspace](../task/sap-named-usertypes-workspace.md)**  
Create a custom named user type that can be used with your SAP software entitlement in the Software Asset Workspace. Creating a custom named user type allows users to track licenses that are specific to their SAP systems.
-   **[Create custom SAP price lists in workspace](../task/sap-prcielists-workspace.md)**  
Create custom SAP price lists so that you can track and manage SAP licenses based on the contracts that are specific to your SAP system.
-   **[View SSO applications in workspace](../task/view-ssoapps-workspace.md)**  
View details related to applications that you can connect through a SSO provider in the Software Asset Workspace.
-   **[View SSO groups in workspace](../task/view-ssogroups-workspace.md)**  
View details related to all SSO groups that have access to a SSO application in the Software Asset Workspace.
-   **[View SSO users in workspace](../task/view-ssousers-workspace.md)**  
View details of all users that have direct access to a SSO application in the Software Asset Workspace, but not through membership in a group.
-   **[Create a software client access record in workspace](../task/create-clientaccess-workspace.md)**  
Add a client access record to track and manage the users or devices that are accessing a particular version of your server software using a client access license \(CAL\).
-   **[Create a resource value record](../task/create-resource-value-record.md)**  
Create a resource value record for each software model for which you want to calculate licensing requirements.
-   **[Create user subscriptions in the workspace](../task/view-user-subscription-workspace.md)**  
Create software subscriptions for SaaS and SSO applications for users in the Software Asset Workspace.
-   **[View publisher part number \(PPN\) suggestions in workspace](../task/view-customppn-workspace.md)**  
View Content Service suggestions for your custom PPNs and DMAPS in the Software Asset Workspace.
-   **[Manage phase-wise Software Asset Management implementation](manage-phasewise-imp-of-sam.md)**  
Carry out phase-wise Software Asset Management implementation by publishing only on a few software products that you want to manage initially. You can also remove the software products from the published list when you no longer want to manage those products.
-   **[Create product install conditions](../task/create-product-install-condition.md)**  
Create product install conditions in the Software Asset Workspace that apply across all software models of a product during reconciliation.
-   **[Create or update an override license cost record](../task/create-edit-override-license-cost.md)**  
Create or update an override license cost record for your software entitlements based on your requirements.
-   **[Reclaim software](../task/reclaiming-software-sam.md)**  
Optimize your environment by reclaiming or removing installed software that is not being used or used infrequently.
-   **[Create a catalog request to reclaim assets](../task/create-catalog-req-offboardingsam.md)**  
Create a catalog request to efficiently reclaim software assets when an employee leaves an organization or moves to a different role.
-   **[Create and manage reports in workspace](../task/create-new-report-workspace.md)**  
Create and manage your report tiles in the Software Asset Workspace.
-   **[View your cluster setup in 360 degrees](../task/view-360-sam-cluster.md)**  
Get a 360-degree perspective of your cluster setup to manage license consumption across the cluster.
-   **[View calculations for your licenses in workspace](../task/licenses-required-workspace.md)**  
Evaluate the license compliance of software applications by viewing the details for all required licenses through the Software Asset Workspace License usage view.
-   **[License usage publisher fields in workspace](../reference/workbench-publisherfields-workspace.md)**  
Field descriptions for the related lists for publishers in the Publishers page in the License usage view.
-   **[Create an end of life workflow request for your software products](../task/manage-eol-risk.md)**  
Manage risks associated with your software product installations that have reached the end of life \(EOL\) or are reaching EOL in the next 18 months. You can create an EOL request and take the required action for the EOL software.
-   **[Complete the end of life workflow request for your software product](../task/complete-eol-workflow-request.md)**  
Perform all the tasks that are required to remove the end of life \(EOL\) software products from your asset inventory. If you set the **Action** field to **Remove EOL Software** in the Decide on IT strategy task, you must perform these software EOL tasks.
-   **[Run a health check scan for Software Asset Management](../task/run-healthcheck.md)**  
Run a health check scan on your Software Asset Management configurations and get recommendations on fixing any errors that might exist.
-   **[Create a Value builder task](../task/create-valuebuilder-task.md)**  
Manually create a Value builder task for publisher packs not being fully utilized in your instance.
-   **[View all maturity items for Software Asset Management](../task/view-maturity-items.md)**  
View the maturity of your Software Asset Management \(SAM\) program to analyze the status of each maturity stage, where each stage shows the number of maturity items completed.
-   **[Create success goals for Software Asset Management](../task/create-success-goals.md)**  
Create success goals to track the success of the Software Asset Management application in your instance.
-   **[Create success activities for Software Asset Management](../task/create-success-activity.md)**  
Create success activities to track the success of your goals.
-   **[Create a success goal category for software assets](../task/create-sam-suc-cat.md)**  
Create a success goal category for adding the category to the Software Asset Management success goal.
-   **[Create demand to rationalize software applications](../task/soft-asset-demand.md)**  
Create demands to rationalize SaaS and SSO applications by discontinuing software subscriptions, reducing software usage, and migrating users to approved software.
-   **[Create a demand requirement](../task/create-demand-req.md)**  
Create a demand requirement for rationalizing your SaaS and SSO applications.
-   **[Install Content library portal for Software Asset Management](../task/install-contentlookup.md)**  
Install the Content library portal store application to view the data stored in the Software Asset Management Content Service.

**Parent Topic:**[Software Asset Management](c_SoftwareAssetMgmt.md)

