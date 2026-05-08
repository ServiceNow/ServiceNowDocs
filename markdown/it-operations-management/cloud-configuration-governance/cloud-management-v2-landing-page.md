---
title: Cloud Provisioning and Governance
description: The ServiceNow Cloud Provisioning and Governance \(CPG\) application serves as a unified interface for accessing cloud resources, delivering cloud offerings to a catalog, and overseeing resource usage. This application is transformed as Cloud Services Catalog application, offering refined and streamlined management of usage and life cycle of cloud resources.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Provisioning and Governance

The ServiceNow® Cloud Provisioning and Governance \(CPG\) application serves as a unified interface for accessing cloud resources, delivering cloud offerings to a catalog, and overseeing resource usage. This application is transformed as Cloud Services Catalog application, offering refined and streamlined management of usage and life cycle of cloud resources.

Cloud Provisioning and Governance is integrated with both private and public cloud providers, such as Amazon Web Services, Microsoft Azure, Google Cloud Platform and VMware.

**Note:**

Migration from workflow to subflows:

-   If the default workflows aren’t customized, the flows are migrated to subflows.
-   If the default workflows are customized, the flows continue to use the existing workflow.

The Cloud Provisioning and Governance application is incompatible and cannot be used simultaneously with the legacy v1 Cloud Management application. The Cloud Provisioning and Governance \(previously Cloud Management\) application is compatible starting with the Jakarta release.

## Workflow migration

As the automation experience evolves, legacy workflows are no longer supported starting with the Zurich release. You can continue using existing custom workflows and deprecated base system workflows only if already in place, but use the new base system flows for all future needs. For more information, see the following articles in the Now Support Knowledge Base:

-   [How to update Cloud Provision Service Request PAD or Cloud Resource Operation Request PAD \[KB2265927\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2265927)
-   [How to migrate Cloud Service Catalog to use flow in case any of the Out of Box Workflows has been modified \[KB2262737\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2262737)

All default predefined workflows have been redesigned using Workflow Studio.

Policy Rule Actions can now use Workflow Studio subflows instead of legacy workflows. If you have not customized the default workflows, the legacy workflows are migrated to subflows automatically. If you have customized the default workflows, they aren’t migrated, and their use cases continue to work with the existing workflows.

The following workflows have been migrated to Workflow Studio flows or subflow:

-   Cloud operation change request
-   Cloud task processing
-   Cloud approval workflow
-   Post-process workflow
-   Pre-process workflow
-   Cloud resource operation request
-   Blueprint request

The following workflows have been deprecated:

-   Retrieve cloud billing data
-   Retrieve cloud billing month
-   Cloud operation step workflow launcher

<table id="simpletable_g33_wwg_vt" class="simpletableBody"><tbody><tr><td>

Explore

 -   Australia
-   [Domain separation and Cloud Provisioning and Governance](domain-separation-cloud-management.md)

</td><td>

Set up

 -   [Day 1 setup guide for Amazon Web Services on Cloud Provisioning and Governance](../../cloud-management-v2-setup/concept/cloud-mgt-aws-setup-day-1.md)
-   [Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance](../../cloud-management-v2-setup/concept/cloud-mgt-azure-setup-guide.md)
-   [Day 1 setup guide for VMware on Cloud Provisioning and Governance](../../cloud-management-v2-setup/concept/cloud-mgt-vmware-setup-guide.md)

</td><td>

Administer

 [Cloud Provisioning and Governance administration guide](cloud-configuration.md)

</td></tr><tr><td>

Use

 -   [Cloud Admin Portal](cloud-admin-portal.md)
-   [Cloud User Portal](../../cloud-management-v2-user/concept/cloudmgt-cloud-user-portal.md)

</td><td>

Develop

 -   [Developer training](https://developer.servicenow.com/app.do#!/training/landing)
-   [Developer documentation](https://developer.servicenow.com/app.do#!/documentation)

</td><td>

Troubleshoot and get help

 -   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Ask or answer questions in the ITOM community](https://community.servicenow.com/community/operations-management)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

</td></tr></tbody>
</table>## Using guided setup to implement Cloud Provisioning and Governance

Cloud Provisioning and Governance guided setup provides a sequence of tasks that help you configure Cloud Provisioning and Governance on your instance. To open Cloud Provisioning and Governance guided setup, navigate to **Guided Setup** &gt; **ITOM Guided Setup**.

For more information about using the guided setup interface, see Using guided setup.

