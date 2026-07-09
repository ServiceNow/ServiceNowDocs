---
title: ITOM Optimization release notes
description: The ServiceNow ITOM Optimization application automates the cloud workflows that you use to manage the cloud resources throughout their life cycles. You can also deploy certified and enterprise-compliant clouds, get visibility into your costs, and manage other cloud management processes. Cloud Provisioning and Governance was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# ITOM Optimization release notes

The ServiceNow® ITOM Optimization application automates the cloud workflows that you use to manage the cloud resources throughout their life cycles. You can also deploy certified and enterprise-compliant clouds, get visibility into your costs, and manage other cloud management processes. Cloud Provisioning and Governance was enhanced and updated in the Yokohama release.

## ITOM Optimization highlights for the Yokohama release

Legacy workflows have been upgraded and seamlessly migrated to the advanced Workflow Studio to align with the latest standards and ensure modern compliance. Additionally, all default \(Out of Box\) workflows have been redesigned to provide enhanced performance, improved usability, and a more streamlined experience.

See [ITOM Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-optimization-landing-page.md) for more information.

## UI changes

-   ****

    The following UI changes are applicable for workflow migration:

    -   In the **Resource Block** &gt; **Operations** &gt; **Steps**, within the **Add Operations Steps** dialog box, the **Invoke Workflow** option has been removed from the Operation Type field.
    -   In the **Resource Block** &gt; **Operations** &gt; **Steps**, within the **Add Operations Steps** dialog box, the **Workflow** check box has been removed from the Add Operations Steps field.
    -   In the **Cloud Catalog Items**, under the **Operation Implementation** drop-down list, the **Workflow** option has been removed.

## Changed in this release

-   ****
    -   Migration of legacy workflows to Workflow Studio flows or subflows.
    -   Policy Rule Actions now supports Workflow Studio subflows instead of legacy workflows.

## Removed in this release

-   In the **Resource Block** &gt; **Operations** &gt; **Steps**, within the **Add Operations Steps** dialog box, the **Invoke Workflow** option has been removed from the Operation Type field.
-   In the **Resource Block** &gt; **Operations** &gt; **Steps**, within the **Add Operations Steps** dialog box, the **Workflow** check box has been removed from the Add Operations Steps field.
-   In the **Cloud Catalog Items**, under the **Operation Implementation** drop-down list, the **Workflow** option has been removed.

## Deprecations

These workflows have been deprecated:

-   Retrieve cloud billing data
-   Retrieve cloud billing month
-   Cloud operation step workflow launcher

**Note:** See  to learn more about the workflow migration.

For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Related ServiceNow applications and features

-   ****

    The ServiceNow® ITOM Cloud Accelerate provides the workflows to evaluate the cloud readiness of your organization and enforce the cloud accelerate guidelines.

    [Cloud Services Catalog](https://www.servicenow.com/docs/access?context=csc-home&version=xanadu) is now a part of ITOM Cloud Accelerate to access and manage cloud resources, and publish cloud offerings to a catalog, in a simplified way.

    [Cloud Configuration Governance](https://www.servicenow.com/docs/access?context=exploring-cloud-configuration-governance&version=xanadu) application provides a set of ready-to-use policies that enable you to check the configuration settings of the cloud resources in your organization identify configuration violations.

    [Cloud Action Library](https://www.servicenow.com/docs/access?context=exploring-cloud-actions-library&version=xanadu) provides ready-to-use actions and subflows that enable you to interact with the cloud resources of the organization.

    Cloud Migration Assessment enables you to plan, organize, and track the process of relocating your enterprise IT resources and workloads to cloud platforms.

-   **[Cloud Discovery Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/cow-landing-page.md)**

    Cloud Operations Workspace offers a comprehensive solution to manage the cloud operations of your organization.

-   **[ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-visibility-landing-page.md)**

    The ITOM Visibility product consists of Discovery, Service Mapping and Tag Governance. For more information, see [Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=xanadu), [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=xanadu), [Tag Governance](https://www.servicenow.com/docs/access?context=tag-governance&version=xanadu), Certificate Inventory and Management, Service Graph Connectors, CMDB 360, and Firewall Audits and Reporting. Discovery and [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=xanadu) give you a unified, connected view of your entire IT network and the services that it supports.

-   **[ITOM/OT SU Licensing and subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-su-licensing-landing-page.md)**

    ITOM/OT SU Licensing enables you to view the total number of licenses assigned to your applications.

-   **Third-party products that integrate with the [Cloud Service Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/csc-home.md):**

    Extend the capabilities of ITOM Cloud Accelerate and its connectors by integrating the following third-party products with it:

    -   Cloud Services
        -   Amazon Web Services
        -   Microsoft Azure
        -   Google Cloud Platform
        -   Terraform Opensource
    -   Ansible configuration management to radically automate the deployment of catalog items, across platforms and cloud service providers, with job templates.

**Parent Topic:**[IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/it-operations-management-rn-landing.md)

