---
title: Cloud Provisioning and Governance: Terraform Connector release notes
description: Version history for the ServiceNow Cloud Provisioning and Governance: Terraform Connector on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-cloud-mgmt-terraform.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ITOM Cloud Accelerate release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Cloud Provisioning and Governance: Terraform Connector release notes

Version history for the ServiceNow® Cloud Provisioning and Governance: Terraform Connector on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.10.0 - June 2026**

    Fixed: Manage access through predefined query access controls for all Cloud Services Catalog tables

-   **Version 1.9.1 - December 2025**
    -   New: Introduced granular, feature-specific admin roles to replace the broad 'admin' role, significantly enhancing security by minimizing excess access. These new roles are seamlessly integrated into the standard administrative experience.
    -   Changed: Enabled end-to-end support for PowerShell operations across MID Servers and Windows remote machines. The system now automatically detects and selects the most appropriate PowerShell version, defaulting to PowerShell 7 where available, to ensure more consistent and reliable execution of scripts.
    -   Fixed: Implemented Read-Only Field Remediation by introducing a new ChoiceList, 'read\_only\_option,' to replace the previous 'read\_only' field \(which was prone to unauthorized client-side updates\). This change prevents client-side manipulation of read-only fields and significantly mitigates security risks across all applications.
-   **Version 1.7.3 - November 2024**
    -   Changed: Filter and restrict data access at the query level with Deny-Unless ACLs and Query ACL rules is now supported
    -   Fixed: Hosted plugins are now supported by Code Signing
-   **Version 1.6.2 - May 2024**
    -   New:
        -   GCP support in Terraform Connector App
        -   Multi-repo support in the Terraform Connector App
-   **Version 1.5.2 - September 2022**
    -   New: Support for complex variables
    -   Changed:
        -   Added support for Terraform v1.1, v1.2
        -   Added support for ADO repositories with Terraform Enterprise / Cloud
    -   Fixed: Several quality issues
    -   Removed: IBM cloud support
-   **Version 1.0.17 - June 2021**

    Fixed: Multiple quality improvements and fixes

-   **Version 1.0.16 - January 2021**
    -   New:
        -   Provisioning for AWS Cloud with Terraform Enterprise/Cloud as well as Terraform Open-Source
        -   Provisioning for vCenter through Terraform Enterprise / Cloud \(OSS was supported earlier\)
        -   Support for GitLabs as a version control system with Terraform Enterprise
        -   Change Governance workflow to manage, and update the cloud catalog items when a IaC artefact is changed
        -   IaC Discovery schedules
    -   Changed:
        -   Support for using existing workspaces when ordering catalog items
-   **Version 1.0.11 - August 2020**

    New: This application is now compatible with the Paris release

-   **Version 1.0.10 - July 2020**

    Localization changes

-   **Version 1.0.8 - February 2020**
    -   New:
        -   Integrates with Terraform Enterprise and Terraform Cloud \(versions .11 and .12\) for Microsoft Azure Cloud provisioning
        -   Supports meta-data specification, to allow linking of Terraform variables to CMDB resource pools
        -   Supports GitHub for version control system for sourcing Terraform modules in Terraform Enterprise and Terraform Cloud
-   **Version 1.0.6 - October 2019**

    New:

    -   Support for Microsoft Azure Cloud
    -   Provides a simplified mechanism to enable provisioning to more clouds, as long as these are supported by Terraform open-source
-   **Version 1.0.5 - August 2019**
    -   New: Support for VMware vSphere Terraform provider
    -   Known issue: On rare occasions, the Cloud Management app cannot provision a VMware VM. The error occurs either when the vSphere server is down/being recycled or due to issues with admin privileges on the vSphere client.
-   **Version 1.0.3 - June 2019**
    -   This version of the app supports use of Terraform for provisioning on IBM Cloud.
    -   Ability to create Service Catalog offerings by importing Terraform config templates for IBM Cloud
    -   Current version supports Terraform Open source edition

