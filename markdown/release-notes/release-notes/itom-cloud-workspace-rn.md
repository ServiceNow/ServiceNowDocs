---
title: Cloud Account Management release notes
description: The ServiceNow Cloud Account Management \(CAM\) application automates account creation, improves transparency, and integrates policy-based governance and certification processes, enhancing efficiency and control across multiple cloud platforms. Cloud Account Management is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-18"
reading_time_minutes: 3
---

# Cloud Account Management release notes

The ServiceNow® Cloud Account Management \(CAM\) application automates account creation, improves transparency, and integrates policy-based governance and certification processes, enhancing efficiency and control across multiple cloud platforms. Cloud Account Management is a new application in the Yokohama release.

## Cloud Account Management highlights for the Yokohama release

-   Create and manage cloud accounts efficiently either by manual or automated processes.
-   Manage and track cloud account requests using the requester dashboard.
-   Visualize data tailored for the admin persona with deeper insights into cloud accounts.
-   Scan accounts for configuration violations and take appropriate actions for weak passwords, pending certifications, undefined account ownership, discovery schedules, and so on.
-   Provision both Terraform Cloud/Terraform Enterprise and cloud native interface accounts.

See [Cloud Account Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/cam-landing.md) for more information.

**Important:** Cloud Account Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Cloud Account Management features

-   **[About data visualization in Cloud Account Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/about-data-visualzation-cam.md)**

    Identify account violations and their severity using prebuilt policies in the Cloud Configuration Governance component. These scans support AWS, Azure, and GCP accounts. Confirm compliance and strengthen security by automatically detecting violations and categorizing them by severity across multiple cloud platforms.

    Support for AWS account and Azure subscription requests via direct API integrations or Terraform and GitHub integrations.

    Track cloud account spending details through integration with the Cloud Cost Management Workspace component. Provides real-time visibility into cloud expenditures, helping organizations stay within budget and optimize cost management.

    **Note:** Tracking of cloud account spending only works when you've a Cloud Cost Management Workspace subscription.

-   **[About provision modes in Cloud Account Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/about-provision-modes.md)**

    Take advantage of flexible infrastructure management through provision mode, which also supports both Terraform Cloud/Terraform Enterprise \(supported in AWS\) and cloud native interface \(supported in AWS and Azure\).

-   **[Set up suspension of an AWS account using service control policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/configure-suspension-policy.md)[Set up suspension of a subscription using Azure policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/configuring-lock-unlock-policy-for-azure.md)**

    Suspend and reactivate accounts quickly in response to security or operational issues by leveraging a predefined AWS or Azure policy.

-   **[Add an unmanaged cloud account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/add-unmanaged-account-cam.md)**

    Confirm consistent governance across all accounts with the ability to onboard accounts \(AWS and Azure\) created outside the CAM workflow, even for accounts that weren’t initially created through CAM.

-   **[Set up Terraform API key in ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/admin-setup.md)**

    Automate account provisioning and management using popular tools through integration with Terraform Cloud/Terraform Enterprise and AWS APIs.

-   **[Update cloud account details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/update-account-ownership.md)**

    Manage account ownership for an account and optionally propagate the change to all CIs associated with that account.

-   **[Certify an account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/certify-account.md)**

    Promote compliance with organizational standards by certifying cloud accounts using defined data certification processes.

-   **[Review request policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/viewing-pace-policy.md)**

    Set guardrails for processes like account approval, budget approval, and configuration assignments through customizable default automated policies. Manage these policies using the existing Policy as Code Engine component.

    Customize the sequence of your approval process by using the standard playbook designer, also known as the Playbooks.


## Activation information

Install Cloud Workspace \( sn\_itom\_cam\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

Implemented zoom functionality in all screens offering zoom levels of 110%, 125%, 150%, 175%, 200%, 250%, 300%, and 400%.

## Localization information

Localization is applicable to CAM in all languages supported by the ServiceNow AI Platform.

## Related ServiceNow applications and features

-   **[Cloud Configuration Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/cloud-configuration-governance.md)**

    The CCG Content Pack application provides a set of ready-to-use policies that enable you to check the configuration settings of cloud resources in your organization to identify configuration violations.

-   **[Cloud Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/cloud-insights-landing-page.md)**

    The ServiceNow® Cloud Cost Management application enables you to analyze all costs that are associated with your cloud assets. You can use this information to optimize operations and reduce your cloud spend.

-   **[Manage PaCE policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/pace-admin-manage-policies.md)**

    Cloud Account Management confirms compliance through account certification and offers customizable policies for general and budget approvals and for configuration assignment, supported by the Policy as Code Engine component.

-   **[Process Automation Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/process-automation-designer.md)**

    ServiceNow® Playbooks enables process owners to author cross-enterprise workflows and create a single, unified process. You can also use Playbooks to provide end users with a simplified, task-oriented view of your process.


**Parent Topic:**[ITOM Cloud Accelerate release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/itom-cloud-accelerate-rn.md)

