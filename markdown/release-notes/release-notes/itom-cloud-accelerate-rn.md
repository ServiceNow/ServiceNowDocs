---
title: ITOM Cloud Accelerate release notes
description: The ServiceNow ITOM Cloud Accelerate application provides workflows to govern the provisioning and management of your cloud and on-premises virtual infrastructure. It leverages ServiceNow Orchestration and integrations with automation tools such as Ansible, Azure DevOps, and Terraform. ITOM Cloud Accelerate was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-24"
reading_time_minutes: 2
---

# ITOM Cloud Accelerate release notes

The ServiceNow® ITOM Cloud Accelerate application provides workflows to govern the provisioning and management of your cloud and on-premises virtual infrastructure. It leverages ServiceNow Orchestration and integrations with automation tools such as Ansible, Azure DevOps, and Terraform. ITOM Cloud Accelerate was enhanced and updated in the Yokohama release.

## ITOM Cloud Accelerate highlights for the Yokohama release

Cloud Workspace highlights:

-   The new Cloud Workspace application has includes a new feature called Cloud Account Management, which automates account creation, improves transparency, and integrates policy-based governance and certification processes, enhancing efficiency and control across multiple cloud platforms.
-   Support for AWS account and Azure subscription requests via direct API integrations or Terraform and GitHub integrations.

Cloud Services Catalog highlight:

Performance enhancements for the predefined catalog items in CSC Content Pack.

See [Cloud Governance](https://www.servicenow.com/docs/access?context=cloud-governance&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

**Important:** ITOM Cloud Accelerate is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Cloud Account Management](https://www.servicenow.com/docs/access?context=cam-landing&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Cloud Account Management is the first feature from ITOM Cloud Accelerate in the Cloud Workspace application that brings together ServiceNow cloud solutions in a unified experience as part of the Cloud Governance Suite.


## Changed in this release

-   **[Cloud Services Catalog Terraform Connector](https://www.servicenow.com/docs/access?context=cpg-terraform-connector-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Cloud Provisioning and Governance: Terraform Connector has been renamed Cloud Services Catalog Terraform Connector


## Deprecations

-   Support for Cloud Provisioning and Governance: Google Cloud Connector has been removed. If you are on a legacy release, you cannot continue to use the Google Cloud Connector but you can use the Cloud Services Catalog Terraform Connector.
-   Support for Cloud Migration Assessment has been removed.

## Activation information

The ITOM Cloud Accelerate features are available as an application at [Cloud Accelerate](https://store.servicenow.com/sn_appstore_store.do#!/store/search?listingtype=allintegrations%253Bancillary_app%253Bcertified_apps%253Bcontent%253Bindustry_solution%253Boem%253Butility%253Btemplate%253Bgenerative_ai%253Bsnow_solution&q=cloud%20governance), which is available on the ServiceNow Store. Contact your ServiceNow sales representative to procure the ITOM Cloud Accelerate entitlement. For details, see [Request the Cloud Provisioning and Governance application](https://www.servicenow.com/docs/access?context=request-plugin-cloud-mgt&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Cloud Configuration Governance](https://www.servicenow.com/docs/access?context=exploring-cloud-configuration-governance&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The [Cloud Configuration Governance](https://www.servicenow.com/docs/access?context=exploring-cloud-configuration-governance&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) application provides a set of ready-to-use policies that enable you to check the configuration settings of cloud resources in your organization identify configuration violations.

-   **[Cloud Action Library](https://www.servicenow.com/docs/access?context=exploring-cloud-actions-library&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The [Cloud Action Library](https://www.servicenow.com/docs/access?context=exploring-cloud-actions-library&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) provides ready-to-use actions and subflows that enable you to interact with the cloud resources of the organization.

-   **Third-party products that integrate with the [Cloud Service Catalog](https://www.servicenow.com/docs/access?context=csc-home&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) Cloud Services Catalog application**

    Extend the capabilities of ITOM Cloud Accelerate and its connectors by integrating the following third-party products with it:

    -   Cloud Services
        -   Amazon Web Services
        -   Microsoft Azure
        -   VMware
        -   Google Cloud Platform
    -   Ansible configuration management to automate the deployment of catalog items, across platforms and cloud service providers, with job templates.

-   **[Cloud Account Management release notes](itom-cloud-workspace-rn.md)**  
The ServiceNow® Cloud Account Management \(CAM\) application automates account creation, improves transparency, and integrates policy-based governance and certification processes, enhancing efficiency and control across multiple cloud platforms. Cloud Account Management is a new application in the Yokohama release.

**Parent Topic:**[IT Operations Management release notes](it-operations-management-rn-landing.md)

