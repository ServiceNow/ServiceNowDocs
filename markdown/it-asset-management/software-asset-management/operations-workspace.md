---
title: License operations view
description: Use the License operations view in Software Asset Workspace to manage software asset operations. These operations include management of licenses, contracts, discovery, client access, resource value, user subscriptions, content suggestions, software asset success, cloud cost simulation, SAM implementation, IBM ASP, IBM ILMT V2 integrations, and engineering apps integrations.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# License operations view

Use the License operations view in Software Asset Workspace to manage software asset operations. These operations include management of licenses, contracts, discovery, client access, resource value, user subscriptions, content suggestions, software asset success, cloud cost simulation, SAM implementation, IBM ASP, IBM ILMT V2 integrations, and engineering apps integrations.

You can access the License operations view by navigating to **Software Asset Workspace** &gt; **License operations**.

The list view for the software assets on the License operations view shows the total number of records for your organization based on the value specified in the system property **SAM Workspace License operations list count limit** \(**sn\_sam\_workspace.sam\_license\_operations\_list\_count**\). The default value for the record count is set to **5000000**. However, the SAM administrator can set the value for the count in the system property as required. If there are less than five million records, then the exact count is shown. If there are more than five million records, then the count is shown as 5000000+.

![License operations view](../image/license-operations-view.png "License operations view")

The License operations view includes the following categories:

-   **Licensing**
    -   **Software entitlements**

        View the details of the software entitlements that record the terms of your software licenses. You can also create entitlements to enter your license details and allocate purchased rights to users or devices. For more information, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).

    -   **Software models**

        View the details of the software models created and also create a software model. For more information, see [Create a software model in the Software Asset Workspace](../task/create-swmodels-workspace.md).

    -   **Entitlement import**

        View the details of the imported entitlements and also import entitlements at one go. For more information, see [Import bulk entitlements in workspace](../task/import-entitlements-workspace.md).

    -   **Entitlement import error**

        View the details on entitlement import errors that are generated while importing software entitlements. For more information, see [Entitlement import error fields](../reference/entitlement-import-error-fields.md).

    -   **Software lifecycle averages**

        Create averages to calculate the End of Life \(EOL\) and End of Support \(EOS\) life cycles of your software. For more information, see [Create averages for product life cycles in workspace](../task/create-lifecycle-averages-workspace.md).

    -   **Consumption rules**

        Create consumption rules to restrict license consumption to certain entities within your organization. You must link this rule to one or many entitlements. For more information, see [Create consumption rules](../task/create-consumption-rule.md) and [Link consumption rules to entitlements](../task/link-consumption-rules.md).

    -   **Product install condition**

        View the product install condition that accounts for all software model installations for a product during reconciliation. These installation conditions are applicable for the software product and all its components. For example, if you have purchased Microsoft Visual Studio, set  up product installation conditions for using Visual Studio only to consume licenses in your non-production  environment. These same conditions then apply across all software models under Visual Studio, including downgrades and  editions. For more information, see [Create product install conditions](../task/create-product-install-condition.md).

    -   **Software installs**

        View the details of software installation such as discovery model, publisher, and reconciliation details. The list view also shows the total number of software installation records for your organization. For more information, see [Software installation fields](../reference/software-installation-fields.md).

-   **Contract - Software contracts**

    Create a software contract to bind agreement between two parties. [Create a contract](../../contract-management/task/t_CreateAContract.md).

-   **Discovery**
    -   **Discovery models**

        View and update software discovery models that are created when a version of software is discovered in a network environment. For more information, see [Discovery models and software installations](c_DiscoveryModels.md).

    -   **Software usage**

        View software usage records to track the usage of software products for which you have created reclamation rules. You can also create software usage records manually from third party integrations or Microsoft System Center Configuration Manager \(SCCM\) integrations. For more information, see [View or create software usage](../task/view-sw-usage-workspace.md).

    -   **All SAP engines**

        View the monthly engine usage measurements for SAP clients based on the license metric for each engine.

    -   **All SAP users**

        View all the discovered users pulled from the SAP systems and their details such as SAP user roles, SAP user active transactions, SAP user activities, and SAP web activities. For more information, see [View SAP users in workspace](../task/view-sapusers-workspace.md).

    -   **SAP named user types**

        Create a custom-named user type that can be used with your SAP software entitlement. Creating a custom-named user type enables users to track licenses of their SAP systems. For more information, see [Create a custom named user type in workspace](../task/sap-named-usertypes-workspace.md).

    -   **SAP price lists**

        Create custom SAP price lists so that you can track and manage SAP licenses based on the contracts of your SAP system. For more information, see [Create custom SAP price lists in workspace](../task/sap-prcielists-workspace.md).

    -   **SAP USMM rules**

        View SAP User License Measurement \(USMM\) rules that map roles to the named user type for an SAP client. For more information, see [SAP USMM-based optimization](usmm-optimization.md).

    -   **SSO applications**

        View details related to applications that you can connect through an SSO provider. For more information, see [View SSO applications in workspace](../task/view-ssoapps-workspace.md).

    -   **SSO groups**

        View details related to all SSO groups that have access to an SSO application. For more information, see [View SSO groups in workspace](../task/view-ssogroups-workspace.md).

    -   **SSO users**

        View details of all users that have direct access to an SSO application, but not through membership in a group. For more information, see [View SSO users in workspace](../task/view-ssousers-workspace.md).

-   **Client access**

    View the details of software client access records. You can also create a record to track and manage the users or devices that are accessing a version of your server software using a client access license \(CAL\). For more information, see [Create a software client access record in workspace](../task/create-clientaccess-workspace.md).

-   **Resource value**

    View and create Resource value records for the software models. For more information, see [Create a resource value record](../task/create-resource-value-record.md).

-   **User subscription**
    -   **User subscription**

        View the details of the software subscriptions for SaaS and SSO applications. You can also create a software subscription. For more information, see [Create user subscriptions in the workspace](../task/view-user-subscription-workspace.md).

    -   **Direct integration profiles**

        View the details of the already created SaaS integration profiles. You can also create an integration profile by selecting the integration type to view software usage and optimize stale licenses. For the supported SaaS applications and procedures, see [Integrate with SaaS applications](create-integration-profile.md).

    -   **SSO integration profiles**

        View the details of the already created SSO integration profiles. You can also create an SSO integration profile by selecting the integration type to view software usage and track user login data for all connected SSO applications, and reclaim unused licenses. For the supported SSO applications and procedures, see [Integrate with SSO providers](saas-sso-integration.md).

    -   **Subscriptions without user**

        View the list of subscriptions where the User field is empty on the Software Subscription \[samp\_sw\_subscription\] table.

    -   **User resolution rules**

        Create a user resolution rule to map user subscriptions from SaaS applications to the User \[sys\_user\] table in ServiceNow AI Platform. For more information, see [Associate a user with subscription records](../task/map-user-data.md).

    -   **SaaS feature usage**

        View the event details for each SaaS and SSO integration performed by the users, such as the event ID, event name, last activity, subscription, product, subscription profile, and publisher. For more information, see [Overlapping usage view](app-ration.md).

    -   **Software storage usage**

        View the usage information for various SaaS applications including details on the allocated storage and used storage in bytes that is stored in the Software storage usage \[saas\_sw\_storage\_usage\] table. For more information, see [Software storage usage fields](../reference/software-storage-usage.md).

    -   **CrowdStrike product usage**

        View the list of usages for various CrowdStrike software models and license metrics. Select a record in the list to view its details.

    -   **CrowdStrike product workload mappings**

        View the list of CrowdStrike products mapped with the types of workloads they manage \(for example, servers, workstations, containers\). With workload mapping, you can correctly count license usage and ensure compliance. Select a record in the list to view its details. For more information on creating a new product workload mapping, see [Create a product workload mapping for CrowdStrike products](../task/create-product-workload-mapping-crowdstrike.md).

    -   **CrowdStrike raw usage**

        View the list of workloads with their metric types. Select a record in the list to view its details.

-   **Content suggestions**
    -   **Part number suggestions**

        View Content Service suggestions for your custom publisher part numbers \(PPN\). For more information, see [Custom publisher part numbers \(PPN\)](customppn-swap.md).

    -   **Normalization suggestions**

        View Content Service normalization suggestion records that are created for discovery models. For more information, see [Normalization suggestions for discovery models](normalization-suggestions.md).

-   **Software asset success**
    -   **Software maturity**

        View the list of Software Asset Management maturity item details. For more information, see [View all maturity items for Software Asset Management](../task/view-maturity-items.md).

    -   **Success goals**

        Create success goals to track the success of your Software Asset Management application and view the list of created success goals. For more information, see [Create success goals for Software Asset Management](../task/create-success-goals.md).

    -   **Success activities**

        Create success activities to track the success of your goals and view the list of already created ones. For more information, see [Create success activities for Software Asset Management](../task/create-success-activity.md).

    -   **Success categories**

        Create success categories to add categories to your success goal and view the list of already created ones. For more information, see [Create a success goal category for software assets](../task/create-sam-suc-cat.md).

    -   **All active value builder tasks**

        Create Value builder tasks for publisher packs that aren’t being fully used and view the list of already created ones. For more information, see [Create a Value builder task](../task/create-valuebuilder-task.md).

    -   **My value builder tasks**

        Create Value builder tasks and view the list of tasks assigned to you. For more information, see [Value builder](sam-value-builder.md) and [Create a Value builder task](../task/create-valuebuilder-task.md).

-   **Cloud cost simulator - Settings**

    View the simulation settings, that is, the cost of moving your on-premise resources to the cloud environment. You can also create Cloud Cost Simulator settings. For more information, see [Cloud cost simulation](cloud-cost-simulator.md).

-   **IBM ASP integration**
    -   **Daily aggregated peak usage**

        View the highest daily sub capacity and full capacity usage of your IBM software products based on the edition, license metric, domain, and region of each product. For more information, see [View the daily aggregated peak usage of your IBM software products](../task/view-daily-aggregated-peak-usage-ibm-products.md).

    -   **Daily high water mark usage**

        View the breakdown for the highest daily usage of your IBM software products by physical host based on both the edition and license metric of each product. For more information, see [View devices with the highest daily usage of your IBM software products](../task/view-daily-high-water-mark-usage-ibm-products.md).

    -   **Product classification**

        View the product classifications for all IBM components that are installed in your environment. These product classifications enable you to track and manage licensing for your IBM components. For more information, see [View product classifications for your IBM components](../task/view-product-classifications-ibm-components.md).

    -   **Devices to scan**

        Specify the virtual machine \(VM\) managers, such as VMware vCenter Servers and IBM Hardware Management Consoles \(HMCs\), for which you want to track IBM licenses. You can track licenses for IBM software that is discovered within these specified VM managers only. For more information about updating the VM managers, see [Specify the virtual machine managers \(VMMs\) for which you are tracking IBM licenses](../task/specify-vm-managers-anglepoint-integration.md).

    -   **Device settings**

        To improve the accuracy of your IBM license calculations, verify the meta data for the physical hosts that your IBM software is installed on. Update any meta data that is incorrect or out of date. For information about updating meta data, see [Verify the meta data for your IBM hosts](../task/verify-ibm-device-meta-data.md).

-   **IBM ILMT V2 integration**
    -   **Peak consumption by product**

        View the highest sub capacity and full capacity usage of your IBM software products based on the product name and the discovery model. For more information, see [View the peak usage of your IBM software products](../task/view-ibm-ilmt-v2-peak-usage-product.md).

    -   **Peak consumption breakdown by device**

        View the breakdown for the highest sub capacity and full capacity usage of your IBM software products by physical host based on the discovered device. For more information, see [View the peak usage of your IBM software products by device](../task/view-ibm-ilmt-v2-peak-usage-device.md).

    -   **ILMT discovered computer**

        View details for the discovered device including the server name, server id, server type, hardware model, hardware serial number, hardware vendor, total processor, and CMDB computer. For more information, see [View the devices that are running your IBM software products](../task/view-ibm-ilmt-v2-discovered-computer.md).

-   **Engineering apps integration**
    -   **License server**

        View a list of all the license management servers that OpenLM or Open iT connect with to get data into your ServiceNow instance. Details on license management servers such as the type of the server, the name of the server, the status of the server, and the last connection time are also provided.

    -   **Discovered engineering licenses**

        View a list of all the discovered and normalized software for your engineering applications.

    -   **Session details**

        View a list of users who are currently using the product. The list shows the number of days and hours being used per user. Select a record in the list to view its details.

    -   **Daily peak concurrent usage**

        View a list of simultaneous users or devices accessing a specific application. Concurrent licenses can be floating, token, or network types. For more information, see [Software license metrics](c_SAMLicenseMetrics.md).

    -   **User denials**

        View a list of users that are denied licenses to products. Select a record in the list to view its details.

    -   **Application product map**

        View a list of mappings of the discovered file names to software products for content resolution.

    -   **Unrecognized publisher integration map**

        View or create unrecognized publisher-to-subscription integration mappings. You should create these mappings when the content resolver doesn't automatically recognize a specific publisher. For more information, see [Create an unrecognized publisher integration mapping](../task/map-unid-pub-integration.md).

-   **SAM implementation - Published products**

    View the list of software products published in a phase-wise implementation of Software Asset Management. For more information, see [Manage phase-wise Software Asset Management implementation](manage-phasewise-imp-of-sam.md).


