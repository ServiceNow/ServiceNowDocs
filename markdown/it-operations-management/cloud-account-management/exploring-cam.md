---
title: Exploring Cloud Account Management
description: The ServiceNow Cloud Account Management in Cloud Workspace application provides a framework to streamline the cloud account creation and management process.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Explore Cloud Workspace, Explore CW, What is Cloud Workspace, Benefits of Cloud Workspace, Subscription accounts in Cloud Workspace, personas in Cloud Workspace]
breadcrumb: [Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Exploring Cloud Account Management

The ServiceNow Cloud Account Management in Cloud Workspace application provides a framework to streamline the cloud account creation and management process.

## Cloud Account Management overview

The automation capabilities of Cloud Account Management in Cloud Workspace simplify administrative tasks related to account management, such as creation, suspension, reactivation, and certification. Data certification confirms the integrity and security of user accounts within the organization's cloud environment.

As a Cloud Account Management admin, you can view the account statistics displayed on the **Home** tab, which include critical severity accounts, high severity accounts, suspended accounts, accounts due for certification, and accounts with undefined budgets.

![Cloud Account Management overview infographic](../image/overview-cam.png)

## About Cloud Workspace entitlements

Cloud Account Management dynamically adjusts the features available to you based on your entitlements.

-   Cloud Account Management entitlement becomes available with the ITOM Cloud Accelerate license.
-   The Cloud Governance Suite \(CGS\) license is a prerequisite to have Cloud Workspace. The CGS license provides the following capabilities:
    -   Access the home page
    -   Access the asset explorer, which provides an overview of your cloud assets and asset details
-   The Cloud Governance Suite with the Cloud Account Management entitlements \(CGS + CAM\) provides the following additional capabilities:
    -   View an overview of your accounts and account details
    -   Submit, view, or approve account requests
    -   Certify an account
    -   View the compliance dashboard
    -   Configure Cloud Account Management or view configuration details
    -   Create request policies to automate the complete account creation and suspension process

## Compliance dashboard in Cloud Workspace

The compliance dashboard consolidates data from ITOM Visibility, Cloud Account Management to provide a unified view of cloud data and key metrics critical for security and compliance reporting.

For more details, see [Viewing the compliance dashboard](viewing-compliance-dashboard.md).

## Cloud account terminology

Cloud Account Management uses the term "cloud account," but other cloud providers use different terms for similar concepts. The terms are as follows:

-   Microsoft Azure Cloud \(Azure\) refers to subscriptions
-   Amazon AWS Cloud \(AWS\) refers to management and member accounts
-   Google Cloud Platform \(GCP\) refers to projects

Cloud providers offer two main access mechanisms for performing operations:

-   Console user access
-   Programmatic user access

For Cloud Account Management, these operations are referred to as IAM service accounts. However, other cloud providers use different terminology:

-   AWS refers to the IAM user
-   Azure refers to service principals
-   GCP refers to service accounts

## Cloud Account Management user personas

|User|Description|
|----|-----------|
|Requester|Initiates cloud account creation requests and requests for suspension or reactivation of their own accounts.|
|Approver|Reviews account requests and either approves or denies them.|
|Admin|Confirms that the Cloud Account Management configurations align with cloud configurations. Customizes the default data certification policy. Onboards accounts created outside the Cloud Account Management application.|
|Certifier|Approves an account as certified or failed. Acts as a verification entity by confirming the accuracy and integrity of the data.|
|Asset viewer|Can view all the configuration items \(CIs\) in Asset Explorer and access the compliance dashboard.|
|Account manager|Can view all account details and associated assets. Account managers have edit access to accounts with primary ownership and read-only access to those with secondary ownership.|

For more information about Cloud Account Management groups and responsibilities, see [Cloud Account Management ACL groups, roles, and responsibilities](../reference/cam-acl-groups-and-roles.md).

## Cloud Account Management Benefits

The Cloud Account Management provides several benefits.

<table id="table_wrb_pgq_dcc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Simplifies subscription account creation by defining standardized procedures and user roles and permissions to promote consistency and compliance with security policies.

</td><td>

[Request a cloud account](../task/request-account.md)

 [Cancel a Cloud account request](../task/cancel-cam-account.md)

</td><td>

Requester

</td></tr><tr><td>

Enables suspending or reactivating accounts, and adding unmanaged accounts.

 Offers a visualization dashboard to manage accounts and request policies to automate account creation, approvals, and budget checks.

</td><td>

[Suspend a Cloud account](suspend-account.md)

 [Reactivate a cloud account](../task/reactivate-account.md)

 [Add an unmanaged cloud account](add-unmanaged-account-cam.md)

 [Creating configurations](cam-config.md)

 [About data visualization in Cloud Account Management](about-data-visualzation-cam.md)

 [Review request policies](viewing-pace-policy.md)

</td><td>

Admin

</td></tr><tr><td>

Streamlines performing verifications that a person or entity has legitimate ownership or control over an account for security, compliance, and regulatory purposes.

</td><td>

[Certify an account](../task/certify-account.md)

</td><td>

Certifier

</td></tr></tbody>
</table>**Related topics**  


[About Amazon Web Services API permissions](about-aws-api-permissions.md)

[Components installed with Cloud Account Management](../reference/components-installed-with-cam.md)

[About provision modes in Cloud Account Management](about-provision-modes.md)

