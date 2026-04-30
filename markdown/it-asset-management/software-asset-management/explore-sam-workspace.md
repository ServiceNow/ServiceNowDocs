---
title: Exploring Software Asset Management
description: The Software Asset Management application's user interface is enhanced to make it more user friendly and intuitive, allowing you to better manage your software installations.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Software Asset Management, IT Asset Management]
---

# Exploring Software Asset Management

The Software Asset Management application's user interface is enhanced to make it more user friendly and intuitive, allowing you to better manage your software installations.

Beginning with the ServiceNow AI Platform Yokohama release, we will provide limited support for the Software Asset Management classic user interface. While it will remain active in your instance, including when you upgrade to a new ServiceNow AI Platform release, we encourage you to move to the new workspace experience.

The Software Asset Management application's core functionality remains the same in both the user interfaces.

## Using the Software Asset Workspace

The Software Asset Management application is available with activation of the new Activate all Software Asset Management Professional plugins including Software Asset Workspace \(com.sn\_samp\_master\_ws\). Activating this plugin automatically activates the Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\) and the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the new plugin is activated, you can't access the classic user interface.

For releases prior to Yokohama, if you activated the older Software Asset Management Professional plugin \(com.sn\_samp\_master\), the Software Asset Workspace is available with activation of the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the Workspace plugin is activated, you can't revert to the classic Software Asset Management application.

**Note:** After the Software Asset Workspace is activated, the menus in the classic Software Asset Management application are hidden for the features that have been moved to the Software Asset Workspace.

For detailed information on configuring and using the Software Asset workspace, refer to [Configuring Software Asset Management](Config-sam-workspace.md) and [Software Asset Workspace](sam-workspace.md).

## Using the classic Software Asset Management application

To continue using the classic Software Asset Management application, you need to activate the Software Asset Management Professional \(com.sn\_samp\_master\) plugin.

If you later decide to use the Software Asset Workspace, you need to activate the Software Asset Workspace \(com.sn\_sam\_workspace\) plugin.

For detailed information on configuring and using the classic Software Asset Management application, refer to [Configuring Software Asset Management](Config-sam-workspace.md) and [Using Software Asset Management classic](using-sam-classic.md).

## Menus that continue to reside in Software Asset Management classic

Even after you activate the Software Asset Workspace \(com.sn\_sam\_workspace\) plugin, the following menus continue to remain in the classic framework:

**Software Asset Demand**:

-   Create New
-   Demands
-   Demand Requirement

**Administration**:

-   Custom Products
-   Custom part Numbers
-   Custom License Metrics
-   Software Asset Demand Actions
-   Pattern Normalization Rules
-   Reclamation Rules
-   Job Results
-   Content Service Setup
-   Refresh Processor Definitions
-   Migrate Software Results
-   Properties
-   Revert Customizations
-   Software Model with De-activated Discovery Maps

**SaaS License**:

-   Unrecognized Subscription Identifier
-   SSO Integration Profiles
-   Direct Integration Profiles

**SAP Compliance and Optimization**:

-   SAP Connections
-   Connection Setup
-   Scheduled Import
-   Transform History

-   **[Software Asset Management overview](c_SAMOverview.md)**  
An overview of the functionality of the Software Asset Management application.
-   **[Now Mobile app for Software Asset Management](now-moile-app-for-sam.md)**  
Use the Now Mobile app to view the hardware and software assets that are assigned to you.
-   **[Virtual Agent for software requests](virtual-agent-software-request-auto-allocation.md)**  
You can implement ServiceNow® Virtual Agent to enable your employees to request software through a predefined conversational interface that is powered by artificial intelligence. Virtual Agent helps address software requests automatically so that your IT fulfillment professionals can focus on more complex requests and incidents.
-   **[Software Asset Management Content Service](c_SAMContentService.md)**  
Opt in to the Software Asset Management Content Service to share unnormalized software installation data from your organization with ServiceNow® to improve the normalization process.
-   **[Software models and Software entitlements](software-models-and-entitlements.md)**  
A software model is a profile of the software that you've purchased, including information about the publisher, version, and discovery map. Software entitlements are used to relate the software model to the rights that you've purchased.
-   **[Software Asset Management migration](c_SAMMigration.md#)**  
Migrate from the Software Asset Management plugin \(ITSM Software Asset Management feature of Asset Management\) to the Software Asset Management application to take advantage of more powerful features. Manual actions by the customer are required after plugin activation.
-   **[Software model relationship to software installation](swmodel-swinstall-rel.md)**  
Associating each software installation with a software model lets you perform audit reporting of licensable and non-licensable software.
-   **[Software license metrics](c_SAMLicenseMetrics.md)**  
License metrics are set in software entitlements and used for reconciliation in various metric groups and software model combinations.
-   **[Software discovery and normalization](c_SAMDiscovery.md)**  
After you've imported your entitlements, use ServiceNow Discovery or Microsoft SCCM to discover software installations in your environment and transfer that data into the ServiceNow AI Platform.
-   **[Software Asset Management software suites](software-suites.md)**  
Software Suites is a way for a software publisher to group related applications as a set.
-   **[Discovery models and software installations](c_DiscoveryModels.md)**  
Software discovery models are automatically created during discovery to identify and normalize the software installed in your environment.
-   **[File Signature Normalization](sam-file-based-discovery.md)**  
File-based discovery finds files on UNIX or Windows servers and processes them with an established set of rules that enhance the identification of installed software. Use the results to monitor specific file types on network servers for security purposes or to manage your software licenses with the File Signature Normalization plugin for Software Asset Management - Professional \(SAMP\).
-   **[Product life cycles](calculated-lifecycles.md)**  
In the absence of vendor-provided life cycles, there are various capabilities that the Software Asset Management application provides to improve life cycle coverage.
-   **[Downgrade Rights](downgrade-rights.md)**  
The concept of downgrading licenses is built into the Software Asset Management plugin feature. Downgrading rights is the process of having acquired the rights to the latest version of software but using the rights to license earlier versions of the same software.
-   **[Software license maintenance](software-license-maintenance.md)**  
Get visibility into your software maintenance entitlements to effectively manage these licenses throughout their life cycle.
-   **[Software Asset Management health check](sam-health-check.md)**  
The Health Check ServiceNow Store application gives a correct and reliable overview of your Software Asset Management configurations and recommends you to correct any errors that may exist.
-   **[Reconciliation of licenses across global entities](reconcile-licenses-global-entities.md)**  
Share entitlements across different entities within your organization by creating consumption rules for entitlements.
-   **[Software reconciliation for compliance](c_SAMReconciliation.md)**  
Automated license reconciliation keeps license positions accurate and up-to-date without manual calculations. Reconciliation runs weekly or on demand.
-   **[Software reclamation rules](sw-reclamation-rules.md)**  
Reclamation rules aggregate usage over time and specify a minimum number of hours or the latest date that a software unit must be used before the software is flagged for reclamation.
-   **[Microsoft SCCM software usage](sccm-software-usage.md)**  
Activate the Microsoft SCCM software usage plugin to integrate your software usage data with the ServiceNow AI Platform.
-   **[Allocation management on Software Asset Management](allocation-management-sam.md)**  
Software Asset Management \(SAM\) offers optimal license assignment confirming that licensing entities are allocated according to the available entitlements.
-   **[Software installation optimization and removal](c_SAMOptimization.md)**  
You can optimize your environment by reclaiming unused software as well as removing unauthorized software.
-   **[License usage analysis](install-licenseusage-journey.md)**  
Gain visibility into the end-to-end journey from installing software to consuming licenses.
-   **[Employee off-boarding process for asset reclamation](itasset-offboarding.md)**  
Coordinate an employee's off-boarding process via a workflow that lets you request, assess, and remove assets.
-   **[Windows Server cluster license optimization](windows-cluster-optimization.md)**  
Optimize rights used for Windows Server clustering based on costs and compliance criteria.
-   **[Bring your own license or subscription to the public cloud](byol-concepts.md)**  
Bring your own license \(BYOL\) support enables you to determine the license compliance of your Microsoft and Oracle software products across hybrid infrastructures. Bring your own subscription \(BYOS\) support enables you to determine the license compliance of your Red Hat Enterprise Linux \(RHEL\) software products across hybrid infrastructures.
-   **[Understanding your cluster infrastructure](understand-sam-cluster.md)**  
Get a holistic and strategic analysis of all the entities in your clusters in one view on the Software Asset Management application.
-   **[Executive insights into KPIs using the Asset Management Executive dashboard](itam-exec-dashboard.md)**  
Use the Asset Management Executive dashboard to gain visibility into critical KPIs for the Software Asset Management application, Hardware Asset Management application, and the Cloud Cost Management application via a single dashboard.
-   **[Cloud cost simulation](cloud-cost-simulator.md)**  
Simulate the cost of moving your on-premise resources to the cloud environment before performing the migration.
-   **[Software asset connections](third-party-discovery-sam.md)**  
Use third-party discovery sources to discover the installed software data that you can integrate with the Software Asset Management application.
-   **[Use Software Asset Management with Governance, Risk, and Compliance](sam_riskmgmt.md)**  
Use the Software Asset Management application in conjunction with the Governance, Risk, and Compliance suite of applications to holistically work on compliance, risk, and regulatory aspects.
-   **[Using Software Asset Management with Agent Client Collector](sam-agentclientcollector.md)**  
Use the Agent Client Collector application to collect software inventory and usage data for the Software Asset Management application.
-   **[Use Software Asset Management and Application Portfolio Management to manage technology onboarding](sam-tpm.md)**  
Use the Software Asset Management application along with Technology Reference Model \(TRM\) of Application Portfolio Management to manage onboarding of technologies.
-   **[Software Asset Management Guided Experiences](playbook-entitlementsetup-workspace.md)**  
The Software Asset Management Guided Experiences application provides step-by-step guidance for completing tasks in your daily software management activities.

**Parent Topic:**[Software Asset Management](c_SoftwareAssetMgmt.md)

