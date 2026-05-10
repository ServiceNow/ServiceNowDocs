---
title: Domain admin considerations
description: Before configuring domain separation for customers, ensure that you review the following considerations ahead of provisioning cloud resources for each domain you are managing in the Cloud Provisioning and Governance application.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Domain separation in Cloud Provisioning and Governance - considerations for service providers, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Domain admin considerations

Before configuring domain separation for customers, ensure that you review the following considerations ahead of provisioning cloud resources for each domain you are managing in the Cloud Provisioning and Governance application.

## Domain administrator activities in a Service Provider's organization

The following section lists activities that a domain's administrator performs for the company that a Service Provider manages. Set up service accounts and cloud accounts using the Cloud Admin Portal. Create pre-provisioning operations that you can configure for cloud resources before your users provision them or perform life-cycle operations.

Strong universal process standards, data-driven process design, strict governance, and centralized administration maximize the benefits of domain separation in Cloud Provisioning and Governance in a single instance. The domain admin role must strictly be restricted to users in the Service Provider's organization, and not be assigned to the Cloud Admin users from the customer's organization. This restriction enables the SP to ensure that a customer does not get full access to other domain's data. Since data is often shared across multiple clients, as domain admins, don't expose or provide permissions that could result in data leakage.

## Provisioning Cloud resources

-   Ensure that you map relevant service accounts to cloud accounts in each domain. For instance, discovering a primary subscription from Azure cloud creates one or more child service accounts and are created in the same domain. This means that all service accounts in a master subscription from Azure cloud must belong to a single company and domain alone.

    Log in using a user with a root\_admin or cloud\_admin role, while setting up cloud and service accounts and running discovery for any domain. Use the domain picker while performing actions such as discovery or cloud and service account creation and mapping.

    **Note:**

    -   Cloud Provisioning and Governance does not support the expand and collapse domain scope capability.
    -   For more information on what a user can and cannot access, see [Domain Scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainScope.md)
    A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

    Ensure that management keys and service account credentials are unique to each domain and are not shared. To set up cloud accounts and service accounts for multiple cloud providers, perform Day 1 Setup actions:

    -   [Day 1 setup guide for Amazon Web Services on Cloud Provisioning and Governance](../../cloud-management-v2-setup/concept/cloud-mgt-aws-setup-day-1.md)
    -   [Day 1 setup guide for Azure on Cloud Provisioning and Governance](../../cloud-management-v2-setup/concept/cloud-mgt-azure-setup-guide.md)
    -   [Day 1 setup guide for Google Cloud Connector on Cloud Provisioning and Governance](../../cloud-management-v2-setup/concept/cloud-mgt-gcp-setup-day-1.md)
    -   [Day 1 setup guide for VMware on Cloud Provisioning and Governance](../../cloud-management-v2-setup/concept/cloud-mgt-vmware-setup-guide.md)
-   [Cloud API \(CAPI\)](../concept/cloud-management-api.md) and [Cloud scripts and cloud script templates](../concept/cloud-scripts-and-templates.md)

    CAPI is not domain separated as, domain separation support in Cloud Provisioning and Governance. Since CAPI is set up at a global domain and shared across leaf domains, ensure that scripts do not contain hard-coded sensitive information such as account details, credentials, or names even in comments or annotations.

    CAPI enables you to integrate Cloud Provisioning and Governance with cloud providers using REST APIs. Cloud scripts are simple java scripts that use platform features. In the Cloud Provisioning and Governance application, script execution is divided into cloud scripts and cloud script templates. Use scripts in templates, resource blocks, OS profiles, and use policy scripts to set request form attributes. Policy scripts cannot override user data. Cloud script templates are actual executables which are passed to target a virtual machine for execution. Create a cloud template first and then associate it with a cloud script.

-   [Cloud Discovery](../../discovery/concept/cloud-discovery-wizard.md)

    Service Providers \(SPs\) use domain separation to segregate data for each customer. Users in a given domain have visibility only to the data in their own domains or in child domains. SPs typically control the top-level domain, which gives them visibility to data associated with all domains. Though domain separation support for Discovery is considered Level 2, there is no delegated administration to the child domains in Cloud Provisioning and Governance. The SPs must retain administrative control. As a SP, always run discovery from a leaf domain by logging in as or impersonating a domain administrator to discover your cloud resources.

    Cloud Discovery provides a wizard that allows you to create and run cloud schedules in a single interface. When you create a schedule with the Discovery Manager, you select the accounts to discover, the credentials for accessing these accounts, and the MID Servers to scan the resources. You can then view the results in the Discovery Home page and track any errors that might have occurred.

    For more information see,

    -   [Discovery Manager](../../discovery/concept/discovery-manager.md#)
    -   [Running discoveries in your network](../../discovery/concept/running-discoveries.md)
        -   [Microsoft Azure Cloud Discovery](../../discovery/concept/azure-cloud-discovery.md)
        -   [VMware Cloud Discovery](../../discovery/concept/vmware-cloud-discovery.md)
        -   [Google Cloud Platform Discovery](../../service-mapping/reference/google-gcp-discovery-pattern.md)
        -   [IBM Cloud Discovery](../../discovery/concept/ibm-cloud-discovery.md)
-   Set up and configure event management to receive external events and generates alerts based on event and alert management rules. The visibility of events depends on the associated service account's domain. Only users belonging that domain can see the event details for processed events. Events that are not associated to a service account are visible to all domains.

    Monitor the health of business services and infrastructure using a single management console and respond appropriately to any issues that come up. Event Management provides intelligent event and alert analysis to ensure continuity of your business service performance. Event Management receives and processes events via the MID Server.

    For more information, see

    -   [Exploring Event Management](../../event-management/concept/exploring-event-management.md)
    -   [Event Management Setup](../../event-management/concept/c_EMConfiguration.md)
        -   [AWS events-driven discovery](../../it-operations-management/concept/aws-events-driven-discovery.md)
        -   [Configure the Microsoft Azure Alert service to auto-update the CMDB](../../it-operations-management/concept/microsoft-azure-alert-driven-discovery.md#)
        -   [Configure the Google Cloud Logging service to auto-update the CMDB](../../it-operations-management/task/gcp-stackdriver-service.md)
        -   [Configure the VMware Events service to auto-update the CMDB](../../it-operations-management/task/vmware-events-service-cloud-mgt.md)
-   The Cloud Provisioning and Governance application supports integration with continuous delivery solutions \(also known as configuration management\). Create an Ansible or Terraform configuration management provider and then run Discovery on the provider to find its resources. For more information, see [Support for continuous delivery \(configuration management\)](../../cloud-management-v2-user/concept/support-config-management-providers.md) and [Create a workload provider type](../task/create-workload-provider-type.md) for each new configuration management provider. This information appears in the order catalog form as management attributes that your users can select when provisioning a virtual resource through a configuration management provider.

-   If you are creating catalogs based on terraform templates and sharing the catalog with multiple domains. Perform module listing \(config discovery\) in the global domain. The MID Server should be created in the global domain and should only be assigned with Terraform capability for its discovery. This allows SPs to share catalogs with multiple domains.

    **Warning:**

    Don't create a global MID Server with any other capability other than configuration management for Terraform.

    Create a common terraform catalog and share it with multiple customers:

    -   Create MID Server in global domain as a global admin.
    -   [Create a Terraform Open Source config provider](../task/setup-cpg-terraform-connector-for-terraform-open-source.md).

        **Note:** Add only “Terraform” as the config provider.

    -   [Create a catalog item based on a Terraform template](../task/catalog-item-terraform-template.md).
-   Cloud Provisioning and Governance supports using ServiceNow AI Platform with subflows. Rules are collections of conditions and actions. ​If all conditions of a rule evaluate to true, the system performs the actions. If any condition evaluates to false, the system does not perform the actions. Creating rules helps you track activities and more quickly respond to and resolve issues. Take advantage of the flow designer subflow to automate your Day 2 operations. Quickly write a subflow that communicates with a Cloud API or a particular resource. Use SSH, PowerShell, or a similar tool, to access and then extend the subflow capabilities. For more information, see [Day 2 operations using subflows](../concept/day-2-ops-using-workflows.md).

-   [Budget-based notification and approval](../concept/cloud-dashboards.md#)

    Domain Separation in Cloud Provisioning and Governance supports data separation of budgets. You can assign domain-specific budgets. Assign a budget for a group and a user within the group. When the user or group reaches the budget limit threshold, notifications are sent alerting them about it. For more information, see [Configure budgets](../concept/cloud-dashboards.md#)

    -   [Create Tags for cloud resources](../concept/cloud-tagging.md#)

        Tags categorize cloud resources to provide richer and more detailed tracking and billing report data. Tag keys are not domain separated and are shown to users of other domains. Tag visibility depends on the associated CI domain or associated billing record domain. Tags that are not associated to any CI or billing record are visible to all domain admins. When a tag is created, it shows up in any new catalog that you create. The cloud admin has to choose the tags they want for their catalog.

    -   Billing data can be viewed separately for each domain. Billing jobs use the domain of service account configured. Configure the Billing setup to enable cloud admins and cloud users to view reports like cloud billing data and cloud tag usage on the billing dashboard.

        Define the scheduled job that regularly uses a MID Server to download billing data from the provider. Cloud Provisioning and Governance saves the data in a cost table and uses the information to generate reports.

        For more information on setting up billing schedules and downloading billing reports, see:

        -   [Define the schedule for downloading AWS billing data](../../cloud-management-v2-setup/task/aws-bill-dwnld-sched-cloud-mgt.md)
        -   [Define the schedule for downloading Azure billing data](../../cloud-management-v2-setup/task/azure-bill-dwnld-sched-cloud-mgt.md)

## Next Steps

**Important:**

While creating custom operations invoking workflows on resource blocks, ensure that you change the context to the appropriate domain.

To change the context to the right domain, edit the **Workflow Activity** to call the following script from within the workflow. Ensure that an appropriate user is obtained from the Service Account creator, or the order user. Invoking this impersonation script enables the workflow to be executed in the correct context and choose the right MID Server belonging to the associated domain.

```
//var orderContext = json.decode(workflow.inputs.ordercontext) ;
new CMPDomainSeparationUtil() .impersonateUser(current.request.requested_for);

```

For more information on performing Cloud Provisioning and Governance life-cycle operations that are available for each domain that you are managing in your instance, see [Cloud User Portal](../../cloud-management-v2-user/concept/cloudmgt-cloud-user-portal.md).

**Related topics**  


[Additional Cloud Provisioning and Governance setup on Day 2](../../cloud-management-v2-setup/concept/cloud-mgt-general-setup-day-2.md)

[Discovery patterns used by ITOM Visibility](../../service-mapping/concept/c_MappingPatternsCustomization.md)

