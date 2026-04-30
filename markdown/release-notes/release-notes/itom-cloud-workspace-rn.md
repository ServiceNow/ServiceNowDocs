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

See [Cloud Account Management](https://www.servicenow.com/docs/access?context=cam-landing&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

**Important:** Cloud Account Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Cloud Account Management features

-   **[About data visualization in Cloud Account Management](https://www.servicenow.com/docs/access?context=about-data-visualzation-cam&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Identify account violations and their severity using prebuilt policies in the Cloud Configuration Governance component. These scans support AWS, Azure, and GCP accounts. Confirm compliance and strengthen security by automatically detecting violations and categorizing them by severity across multiple cloud platforms.

    Support for AWS account and Azure subscription requests via direct API integrations or Terraform and GitHub integrations.

    Track cloud account spending details through integration with the Cloud Cost Management Workspace component. Provides real-time visibility into cloud expenditures, helping organizations stay within budget and optimize cost management.

    **Note:** Tracking of cloud account spending only works when you've a Cloud Cost Management Workspace subscription.

-   **[About provision modes in Cloud Account Management](https://www.servicenow.com/docs/access?context=about-provision-modes&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Take advantage of flexible infrastructure management through provision mode, which also supports both Terraform Cloud/Terraform Enterprise \(supported in AWS\) and cloud native interface \(supported in AWS and Azure\).

-   **[Set up suspension of an AWS account using service control policy](https://www.servicenow.com/docs/access?context=configure-suspension-policy&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)[Set up suspension of a subscription using Azure policy](https://www.servicenow.com/docs/access?context=configuring-lock-unlock-policy-for-azure&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Suspend and reactivate accounts quickly in response to security or operational issues by leveraging a predefined AWS or Azure policy.

-   **[Add an unmanaged cloud account](https://www.servicenow.com/docs/access?context=add-unmanaged-account-cam&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Confirm consistent governance across all accounts with the ability to onboard accounts \(AWS and Azure\) created outside the CAM workflow, even for accounts that weren’t initially created through CAM.

-   **[Set up Terraform API key in ServiceNow](https://www.servicenow.com/docs/access?context=admin-setup&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Automate account provisioning and management using popular tools through integration with Terraform Cloud/Terraform Enterprise and AWS APIs.

-   **[Update cloud account details](https://www.servicenow.com/docs/access?context=update-account-ownership&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Manage account ownership for an account and optionally propagate the change to all CIs associated with that account.

-   **[Certify an account](https://www.servicenow.com/docs/access?context=certify-account&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Promote compliance with organizational standards by certifying cloud accounts using defined data certification processes.

-   **[Review request policies](https://www.servicenow.com/docs/access?context=viewing-pace-policy&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Set guardrails for processes like account approval, budget approval, and configuration assignments through customizable default automated policies. Manage these policies using the existing Policy as Code Engine component.

    Customize the sequence of your approval process by using the standard playbook designer, also known as the Playbooks.


## Activation information

Install Cloud Workspace \( sn\_itom\_cam\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

Implemented zoom functionality in all screens offering zoom levels of 110%, 125%, 150%, 175%, 200%, 250%, 300%, and 400%.

## Localization information

Localization is applicable to CAM in all languages supported by the ServiceNow AI Platform.

## Related ServiceNow applications and features

-   **[Cloud Configuration Governance](https://www.servicenow.com/docs/access?context=cloud-configuration-governance&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The CCG Content Pack application provides a set of ready-to-use policies that enable you to check the configuration settings of cloud resources in your organization to identify configuration violations.

-   **[Cloud Insights](https://www.servicenow.com/docs/access?context=cloud-insights-landing-page&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Cloud Cost Management application enables you to analyze all costs that are associated with your cloud assets. You can use this information to optimize operations and reduce your cloud spend.

-   **[Manage PaCE policies](https://www.servicenow.com/docs/access?context=pace-admin-manage-policies&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Cloud Account Management confirms compliance through account certification and offers customizable policies for general and budget approvals and for configuration assignment, supported by the Policy as Code Engine component.

-   **[Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    ServiceNow® Playbooks enables process owners to author cross-enterprise workflows and create a single, unified process. You can also use Playbooks to provide end users with a simplified, task-oriented view of your process.


**Parent Topic:**[ITOM Cloud Accelerate release notes](itom-cloud-accelerate-rn.md)

