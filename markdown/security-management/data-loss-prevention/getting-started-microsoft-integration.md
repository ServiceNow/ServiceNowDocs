---
title: Getting started with Microsoft DLP IR integration for data loss prevention
description: Review the following information before you start setting up your Microsoft DLP IR integration for data loss prevention.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Data Loss Prevention Incident Response with Microsoft, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Getting started with Microsoft DLP IR integration for data loss prevention

Review the following information before you start setting up your Microsoft DLP IR integration for data loss prevention.

<table id="table_yvc_gb3_1nc"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Get the Microsoft Purview credentials to fetch the event data and AWS/Azure Storage account credentials to store the match content

 Register an application with the Microsoft identity platform

</td><td>

Register an application on the Microsoft Azure platform from [here](https://learn.microsoft.com/en-us/office/office-365-management-api/get-started-with-office-365-management-apis#register-your-application-in-azure-ad) to get the Client ID, Client Secret, and Tenant ID. For information on the Roles required for creating an application, see [Prerequisites](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app#prerequisites).For information on the API Permissions/Roles required on a Microsoft Azure application to configure it on ServiceNow Microsoft DLP integration, refer to the following table.

</td></tr><tr><td>

Permissions required for Azure user to get the access of read/write/delete blob on Azure Storage

</td><td>

1.  Assign the **Storage Blob Data Contributor** role to an existing Azure user to read, write, and delete blobs on Azure Storage. For information about the role, see [Azure built-in roles: Storage Blob Data Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor). Alternatively, create a custom role and specify the actions. For information about creating custom roles, see [Azure custom roles](https://learn.microsoft.com/en-us/azure/role-based-access-control/custom-roles).
2.  Assign a shared access key to the user that has the role privileges. For information about account access keys, see [View account access keys](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-keys-manage?tabs=azure-portal#view-account-access-keys).

</td></tr><tr><td>

Permissions required for AWS user to get the access of read/write/delete object on AWS Storage

</td><td>

Create a policy that gives list, read, write, and delete access for the object in AWS S3 Storage.1.  Create and configure an Amazon S3 bucket. For information about creating an S3 bucket, see [Create an S3 bucket](https://docs.aws.amazon.com/AmazonS3/latest/userguide/creating-bucket.html).
2.  Provide read and write access to Amazon S3 bucket objects. For information about the object accesses, see the [example policy](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_examples_s3_rw-bucket.html). For information about creating policies, see [Create IAM policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_create-console.html).
3.  Provide the access key and the secret key to the user. For information about authentication, see [Authenticating the AWS tools](https://docs.aws.amazon.com/powershell/latest/userguide/creds-idc.html).

</td></tr><tr><td>

Assign and verify if you have the required roles for ServiceNow AI Platform and Data Loss Administration roles.

</td><td>

The following roles are required for configuration and verification of the expected results:-   The admin role installs the integration from the ServiceNow Store and assigns the sn\_dlir.admin role.
-   The sn\_dlir.admin role performs the following tasks:
    -   Configures the integration.
    -   Sets up the incident profiles.

</td></tr><tr><td>

Verify that the ServiceNow core applications required to support the Microsoft DLP IR integration are installed and activated before you configure this integration.

</td><td>

Verify that the following DLP IR applications and security support common applications are installed and activated from the ServiceNow Store. If not installed, then install and activate on the application. -   Security Support Common
-   Data Loss Prevention Incident Response

</td></tr></tbody>
</table><table id="table_u52_yyl_vwb"><thead><tr><th>

API

</th><th>

Permission name

</th><th>

Type

</th><th>

Description

</th><th>

Required for which ServiceNow functionality?

</th><th>

Is Admin consent required?

</th></tr></thead><tbody><tr><td>

Office 365 Management API

</td><td>

ActivityFeed.ReadDlp

</td><td>

Application

</td><td>

Read DLP policy events including detected sensitive data.

</td><td>

To ingest the DLP events from MSFT Purview to ServiceNow.**Note:** This permission is a must to get the MSFT data into ServiceNow.

</td><td align="center">

Yes

</td></tr><tr><td rowspan="3">

Microsoft Graph API

</td><td>

Files.Read.All

</td><td>

Application

</td><td>

Read files in all site collections that you can access.

</td><td>

Download File: To download the attachment on the ServiceNow instance that caused the DLP event from OneDrive or SharePoint **Note:** This is optional. You can skip this API permission if you don't want to allow the analysts to download the attachment that caused the DLP event.

</td><td align="center">

Yes

</td></tr><tr><td>

Mail.Read

</td><td>

Application

</td><td>

Read mail in all mailboxes.

</td><td>

Download File: To download the email content \(body and attachment\) on the ServiceNow instance that caused the DLP event from Exchange.**Note:** Optional. You can skip this API permission if you don't want to allow the analysts to download the email content \(body, attachment\) that caused the DLP event.

</td><td align="center">

Yes

</td></tr><tr><td>

User.Read

</td><td>

Delegated

</td><td>

Sign in and read user profile.

</td><td>

Default permission available for all new applications.

</td><td align="center">

No

</td></tr></tbody>
</table>## Detected Sensitive Information \(Optional\)

The match content is stored externally in Azure Blob Storage or Amazon S3 bucket and will be pulled from external storage when the user views an incident.

Any one of the following permissions are required if the users would like to view Match Content/Detected Sensitive Information in the DLP Core application:

1.  If you’re a Microsoft Azure user, you must have the role Storage Blob Data Contributor to read, write, and delete blobs on Azure Storage.
2.  If you’re an Amazon S3 user, you must create a policy that gives list, read, write, and delete access for the object in Amazon S3 Storage.

**Parent Topic:**[Data Loss Prevention Incident Response with Microsoft](../concept/dlp-integration-microsoft.md)

