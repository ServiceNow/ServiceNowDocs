---
title: AWS IAM Spoke
description: Integrate ServiceNow instance with AWS IAM to manage access to AWS services and resources securely. Manage groups, policies, and roles in AWS IAM from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# AWS IAM Spoke

Integrate ServiceNow instance with AWS IAM to manage access to AWS services and resources securely. Manage groups, policies, and roles in AWS IAM from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

AWS IAM spoke v1.1.0 is the latest version.

## Supported version

This spoke was built for API version 2010-05-08, but may be compatible with later versions.

**Note:** If you use different API version, ensure that you change the API version in all spoke actions.

## Spoke requirements

-   User with full access to IAM.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

For more information about creating user in IAM and providing the required access, see [AWS Identity and Access Management Documentation](https://docs.aws.amazon.com/iam/index.html) site.

## Spoke subflows

The Jenkins spoke provides sample subflows to demonstrate automating AWS IAM tasks. Available subflows are:

|Subflow|Description|
|-------|-----------|
|Delete Group|Deletes the specified AWS IAM group.|
|Delete User|Deletes the specified AWS IAM user.|
|Delete Policy|Deletes the specified policy from the AWS IAM account.|

## Spoke actions

The AWS IAM spoke provides actions to automate AWS IAM tasks when events occur in ServiceNow. Available actions include:

<table id="table_sfw_b4t_pkb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="6">

Group Management

</td><td>

Add User to Group

</td><td>

Adds user to a group in AWS IAM.

</td></tr><tr><td>

Create Group

</td><td>

Creates a group in AWS IAM.

</td></tr><tr><td>

Delete Group

</td><td>

Deletes a group in AWS IAM.

</td></tr><tr><td>

Look up Group

</td><td>

Searches for the required group in AWS IAM.

</td></tr><tr><td>

Look up Group Users

</td><td>

Lists all the users in the required group.

</td></tr><tr><td>

Remove User from Group

</td><td>

Removes a user from a group in AWS IAM.

</td></tr><tr><td rowspan="6">

Group Policy Management

</td><td>

Attach Inline Policy in Group

</td><td>

Adds or updates an inline policy document embedded in the specified IAM group.

</td></tr><tr><td>

Attach Policy to Group

</td><td>

Attaches the specified managed policy to the required IAM group.

</td></tr><tr><td>

Detach Inline Policy from Group

</td><td>

Deletes the specified inline policy from the specified AWS IAM group

</td></tr><tr><td>

Detach Policy from Group

</td><td>

Detaches the specified managed policy from the required IAM group.

</td></tr><tr><td>

Look up Attached Group Policies

</td><td>

Retrieves the list of all policies attached to the IAM group.

</td></tr><tr><td>

Look up Group Policies

</td><td>

Retrieves all the inline policies of the specified group. If none exists, the operation returns an empty list

</td></tr><tr><td rowspan="4">

Policy Management

</td><td>

Create Policy

</td><td>

Creates managed policy in the specified IAM group.

</td></tr><tr><td>

Delete Policy

</td><td>

Deletes specified Policy from AWS IAM.

</td></tr><tr><td>

Detach Policy from Roles

</td><td>

Detaches the specified managed policy from the specified IAM Role.

</td></tr><tr><td>

Look up Entities for Policy

</td><td>

Lists all entities \(Users, Group, and Roles\) attached to this policy.

</td></tr><tr><td rowspan="18">

User Management

</td><td>

Create User

</td><td>

Creates a user in AWS IAM.

</td></tr><tr><td>

Deactivate MFA Device

</td><td>

Deactivates the required MFA device attached to a user.

</td></tr><tr><td>

Delete Access Key for User

</td><td>

Deletes the access key of the AWS IAM user.

</td></tr><tr><td>

Delete Login Profile

</td><td>

Deletes the password for the specified IAM user, which terminates the user's ability to access AWS services through the AWS Management Console.

</td></tr><tr><td>

Delete Service Specific Credential

</td><td>

Deletes the required service-specific credential.

</td></tr><tr><td>

Delete Signing Certificate

</td><td>

Deletes a signing certificate associated with the specified IAM user.

</td></tr><tr><td>

Delete SSH Public Key

</td><td>

Deletes the specified SSH public key.

</td></tr><tr><td>

Delete User

</td><td>

Deletes the required IAM User.

</td></tr><tr><td>

Delete Virtual MFA Device by User

</td><td>

Deletes the specified Virtual MFA device.

</td></tr><tr><td>

Detach Policy from User

</td><td>

Detaches the specified managed policy from the specified IAM role.

</td></tr><tr><td>

Look up User

</td><td>

Searches for the required user in the AWS IAM.

</td></tr><tr><td>

Look up Access Keys by User

</td><td>

Lists the access key of the AWS IAM user.

</td></tr><tr><td>

Look up Groups for User

</td><td>

Retrieves the list of all the groups, a particular user belongs to.

</td></tr><tr><td>

Look up Inline User Policies

</td><td>

Retrieves all the inline policies of the specified IAM user. If none exists, the operation returns an empty list.

</td></tr><tr><td>

Look up MFA Devices by User

</td><td>

Retrieves information about the MFA services associated with the specified IAM user. If none exists, the operation returns an empty list.

</td></tr><tr><td>

Look up Service Specific Credentials

</td><td>

Retrieves information about the service-specific credentials associated with the specified IAM user.

</td></tr><tr><td>

Look up Signing Certificates by User

</td><td>

Retrieves information about the signing certificates associated with the specified IAM user. If none exists, the operation returns an empty list.

</td></tr><tr><td>

Look up SSH Public Keys by User

</td><td>

Retrieves information about the SSH public keys associated with the specified IAM user. If none exists, the operation returns an empty list.

</td></tr><tr><td>

User Policy Management

</td><td>

Attach Policy to User

</td><td>

Attaches the specified managed policy to the specified user.

</td></tr><tr><td>

 

</td><td>

Delete Inline User Policy

</td><td>

Deletes an inline policy attached to the user.

</td></tr><tr><td>

 

</td><td>

Look up Attached User Policies

</td><td>

Retrieves all the attached policies of the user.

</td></tr><tr><td>

Role Management

</td><td>

Look up Roles

</td><td>

Retrieves list of all roles.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the AWS IAM spoke](../task/setup-aws-iam.md#).

