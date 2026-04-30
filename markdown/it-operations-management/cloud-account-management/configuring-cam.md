---
title: Configuring Cloud Account Management
description: Configuring the Cloud Account Management application involves a set of required tasks, integrations, and setups to be completed before initiating service account creation and provisioning.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
keywords: [Configure Cloud Account Management, Configure Cloud Workspace, Configure CAM, setup Cloud Account Management]
breadcrumb: [Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Configuring Cloud Account Management

Configuring the Cloud Account Management application involves a set of required tasks, integrations, and setups to be completed before initiating service account creation and provisioning.

The steps involved are different for AWS and Azure. These configurations are listed in the following tables.

<table id="AWS_table"><thead><tr><th>

No.

</th><th>

Task

</th><th>

Task Owner

</th><th>

Impacted Feature

</th><th>

Input

</th><th>

Output

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

1

</td><td>

![](../../../reuse/icons/brand-icons/bus-email-server.svg)[Set up and verify root email in AWS](../task/aws-setup.md)

</td><td>

Email Admin

</td><td>

Create an account

</td><td>

None

</td><td>

Email Alias

</td><td>

A single AD email across multiple AWS accounts streamlines management, enhances security, and boosts collaboration.

</td></tr><tr><td>

2

</td><td>

![](../../../reuse/icons/brand-icons/bus-person.svg)[Set up an Identity Access Manager account for a ServiceNow user in AWS](set-up-iam-account-in-aws.md)

</td><td>

AWS Admin

</td><td>

All features

</td><td>

None

</td><td>

AWS Access Key

 AWS Secret Key

</td><td>

A centralized IAM user in the management account efficiently manages multiple AWS accounts via a CloudFormation template.

</td></tr><tr><td>

3

</td><td>

![](../../../reuse/icons/brand-icons/bus-whitepaper.svg)[Set up suspension of an AWS account using service control policy](../task/configure-suspension-policy.md)

</td><td>

AWS Admin

</td><td>

Account suspension

</td><td>

None

</td><td>

SCP Policy ID

</td><td>

Adding an account number to the AWS organization's Service Control Policy blocks the creation of new resources and helps prevent overspending, while existing resources remain unaffected.

</td></tr><tr><td>

4

</td><td>

![](../../../reuse/icons/brand-icons/bus-actionable-analytics.svg)[Setting up Terraform and GitHub](about-terraform-git-and-servicenow_0.md)

**Note:** This step isn’t required if cloud native interface is used for provisioning the account.

</td><td>

Terraform Admin

 DevOps Admin

</td><td>

Create an account for AWS

</td><td>

AWS Access Key

 AWS Secret Key

</td><td>

Terraform API Key Token

 Terraform OAuth Token ID

 Terraform Org

 VCS Identifier

 Terraform URL

</td><td>

GitHub templates deployed to Terraform Cloud or Enterprise streamline account creation and promote consistent configurations.

</td></tr><tr><td>

5

</td><td>

![](../../../reuse/icons/brand-icons/bus-actionable-analytics.svg)[Create a cloud native interface account configuration](../task/create-cloud-native-interface-config.md)

**Note:** This step isn’t required if Terraform is used for provisioning the account.

</td><td>

ServiceNow AI Platform Admin

</td><td>

Create an account for Cloud Native Interface

</td><td>

None

</td><td>

None

</td><td>

No additional procedure is needed for cloud native interface. You can proceed to [Install Cloud Workspace](../task/activate-cloud-account-management.md).

</td></tr><tr><td>

6

</td><td>

![](../../../reuse/icons/brand-icons/bus-work-order.svg)[Populate Cloud Account Management dependent tables](add-account-details.md)

1.  [Create a service account](../task/create-service-account.md)
2.  [Define and run discovery schedule](../task/define-run-discovery-schedule.md)

</td><td>

ServiceNow AI Platform Admin

</td><td>

All features

</td><td>

Discovery Credentials

</td><td>

Cloud Organization

 AWS Org Unit

 Cloud Service Account

</td><td>

Cloud Discovery or Service Graph Connector for AWS to import cloud organization structures and create subscription accounts.

</td></tr><tr><td>

7

</td><td>

![](../../../reuse/icons/brand-icons/bus-integration-and-apis.svg)[Provisioning modes for Cloud Account Management in Cloud Workspace](supported-provision-modes.md)

-   [Set up Terraform API key in ServiceNow](../task/configure-api-key.md)
-   [Set up AWS API configuration information in ServiceNow](configure-aws-api-key-in-servicenow.md)

</td><td>

ServiceNow AI Platform Admin

</td><td>

Create an account

</td><td>

Email Alias

 Terraform Cloud API Key Token

 Terraform Cloud OAuth Token ID

 Terraform Cloud Org

 VCS Identifier

</td><td>

None

</td><td>

Streamline provisioning with flexible modes like Terraform and cloud native interface, centralizes management, enhances security, optimizes costs, and improves governance.

</td></tr><tr><td>

8

</td><td>

![](../../../reuse/icons/brand-icons/bus-investor-relations-1.svg)[Set up scan configuration for data visualization](../task/set-up-data-visualization.md)

</td><td>

ServiceNow AI Platform Admin

</td><td>

Visualization

</td><td>

None

</td><td>

None

</td><td>

Data visualization requires scanning all account violations based on the policy set.

</td></tr><tr><td>

9

</td><td>

![](../../../reuse/icons/brand-icons/bus-3-person.svg)[Add members to the group](../task/add-member-group.md)

</td><td>

ServiceNow AI Platform Admin

</td><td>

All features

</td><td>

None

</td><td>

None

</td><td>

Confirm that members are assigned to the correct group for them to perform the account request, approval, provisioning, and certification process. Assign members to the correct groups for proper permissions, helping prevent unauthorized access and promoting security.

</td></tr><tr><td>

10

</td><td>

![](../../../reuse/icons/brand-icons/bus-sdlc.svg)[Creating configurations](cam-config.md)

</td><td>

Cloud Workspace Admin

</td><td>

All features

</td><td>

None

</td><td>

None

</td><td>

Configure before creating, suspending, or scanning accounts.

</td></tr><tr><td>

11

</td><td>

![](../../../reuse/icons/brand-icons/bus-compliance.svg)[Review default Cloud Account Management certification policy](../task/policy-setup.md)

</td><td>

Cloud Workspace Admin

</td><td>

All features

</td><td>

None

</td><td>

None

</td><td>

Certify all cloud service accounts either created or boarded after discovery can be certified. The admin can also customize the default policy or create a policy. The default policy helps to certify all the available cloud service accounts once every 90 days.

</td></tr><tr><td>

12

</td><td>

![](../../../reuse/icons/brand-icons/bus-compliance.svg)[Review request policies](viewing-pace-policy.md)

</td><td>

Cloud Workspace Admin

</td><td>

All features

</td><td>

None

</td><td>

None

</td><td>

Request Policies are rules that govern the behavior of request workflows by applying data checks and conditions. Regularly reviewing and updating these policies confirms that your cloud account request process remains consistent with the procedure for creating cloud subscription accounts.

</td></tr></tbody>
</table><table id="Azure_table"><thead><tr><th>

No.

</th><th>

Name

</th><th>

Task Owner

</th><th>

Impacted feature

</th><th>

Input

</th><th>

Output

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

1

</td><td>

![](../../../reuse/icons/brand-icons/bus-whitepaper.svg)[Configure account suspension in Azure](../task/configuring-azure-suspension-permission.md)

</td><td>

Azure Admin

</td><td>

Account suspension

</td><td>

None

</td><td>

OAuth Client ID

 OAuth Client Secret

 Tenant ID

</td><td>

Configure the permission and assign the permission to a user who suspends or reactivates the account.

</td></tr><tr><td>

2

</td><td>

![](../../../reuse/icons/brand-icons/bus-person.svg)[Set up Azure Service Principal credential](set-up-azure-service-principal-credential.md)

</td><td>

ServiceNow AI Platform Admin

</td><td>

All features

</td><td>

OAuth Client ID

 OAuth Client Secret

 Tenant ID

</td><td>

None

</td><td>

Provide the Azure credentials obtained from your Azure administrator. These credentials are used to create a suspension profile and enables you to suspend temporarily or terminate Azure accounts as needed.

</td></tr><tr><td>

3

</td><td>

![](../../../reuse/icons/brand-icons/bus-actionable-analytics.svg)[Create a cloud native interface account configuration](../task/create-cloud-native-interface-config.md)

**Note:** This step isn’t required if Terraform is used for provisioning the account.

</td><td>

ServiceNow AI Platform Admin

</td><td>

Create an account for Cloud Native Interface

</td><td>

None

</td><td>

None

</td><td>

No additional procedure is needed for cloud native interface. You can proceed to [Install Cloud Workspace](../task/activate-cloud-account-management.md).

</td></tr><tr><td>

4

</td><td>

![](../../../reuse/icons/brand-icons/bus-work-order.svg)[Populate Cloud Account Management dependent tables](add-account-details.md)

1.  [Create a service account](../task/create-service-account.md)
2.  [Define and run discovery schedule](../task/define-run-discovery-schedule.md)

</td><td>

ServiceNow AI Platform Admin

</td><td>

All features

</td><td>

Discovery Credentials

</td><td>

Cloud Organization

 Azure Management Group

 Cloud Service Account

</td><td>

Cloud Discovery import cloud organization structures and create subscription accounts.

</td></tr><tr><td>

5

</td><td>

![](../../../reuse/icons/brand-icons/bus-investor-relations-1.svg)[Set up scan configuration for data visualization](../task/set-up-data-visualization.md)

</td><td>

ServiceNow AI Platform Admin

</td><td>

Visualization

</td><td>

None

</td><td>

None

</td><td>

Data visualization requires scanning all account violations based on the policy set.

</td></tr><tr><td>

6

</td><td>

![](../../../reuse/icons/brand-icons/bus-3-person.svg)[Add members to the group](../task/add-member-group.md)

</td><td>

ServiceNow AI Platform Admin

</td><td>

All features

</td><td>

None

</td><td>

None

</td><td>

Confirm that members are assigned to the correct group for them to perform the account request, approval, provisioning, and certification process. Assign members to the correct groups for proper permissions, helping prevent unauthorized access and promoting security.

</td></tr><tr><td>

7

</td><td>

![](../../../reuse/icons/brand-icons/bus-sdlc.svg)[Creating configurations](cam-config.md)

</td><td>

Cloud Workspace Admin

</td><td>

All features

</td><td>

None

</td><td>

None

</td><td>

Configure before creating, suspending, or scanning accounts.

</td></tr><tr><td>

8

</td><td>

![](../../../reuse/icons/brand-icons/bus-compliance.svg)[Review default Cloud Account Management certification policy](../task/policy-setup.md)

</td><td>

Cloud Workspace Admin

</td><td>

All features

</td><td>

None

</td><td>

None

</td><td>

Certify all cloud service accounts either created or boarded after discovery can be certified. The admin can also customize the default policy or create a policy. The default policy helps to certify all the available cloud service accounts once every 90 days.

</td></tr></tbody>
</table>