---
title: Pre-requisites to enable policy redlining feature
description: Certain configurations are required to be set up for policy collaborators to use the policy redlining feature in the Compliance Workspace.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Policy authoring and redlining, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Pre-requisites to enable policy redlining feature

Certain configurations are required to be set up for policy collaborators to use the policy redlining feature in the Compliance Workspace.

**Important:**

Currently, the policy authoring and redlining feature is available exclusively to ServiceNow cloud-based customers.

## Spoke support for cloud hosting services

-   **Spokes required for Policy authoring – integration with Microsoft Office 365**
    -   Microsoft OneDrive Spoke – 2.1.1
    -   Microsoft OneDrive Spoke for Document Service Framework – 1.0.5
-   **Spokes required for Policy authoring – integration with Microsoft SharePoint**
    -   Microsoft OneDrive spoke 2.3.1
    -   Document services framework for OneDrive – 2.0.0
-   **Spokes required for Policy authoring – integration with Google Drive**
    -   Document Service Framework for Google Drive Spoke – 1.0.1
    -   Google Drive Spoke – 1.4.1

**Note:** Integration Hub entitlements included in the Compliance Workspace are for Policy authoring – integration with O365 and integration with Google Drive. Using Microsoft integration or Google Drive integration requires Integration Hub transactions not included in the Compliance Workspace product but requires an Automation Engine or Integration Hub entitlement.

## Connecting to cloud hosting services

If you’re a policy collaborator wanting to use the policy redlining feature in the Compliance Workspace, then you must set up the following configurations.

**Note:** You can establish a connection with only one of the following cloud hosting services: either Microsoft or Google Drive.

Microsoft implies both Microsoft OneDrive and Microsoft SharePoint.

-   **Establish a connection with cloud hosting services**
    -   **Connection with Microsoft OneDrive**

        You must first set up the Microsoft OneDrive to perform actions in Microsoft OneDrive from ServiceNow. For more information, see [Setup Microsoft OneDrive for Document Services](https://www.servicenow.com/docs/access?context=configure-ms-onedrive-doc-services&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

        **Note:** To set up connection you require Microsoft Azure App permissions such as email, openid, profile, Files.ReadWrite, offline\_access, User.Read, User.ReadBasic.All, Sites.ReadWrite.All.

    -   **Connection with Microsoft SharePoint**

        You must first set up the Microsoft SharePoint to perform actions in Microsoft SharePoint site from ServiceNow. For more information, see [Setup Microsoft OneDrive for Document Services](https://www.servicenow.com/docs/access?context=configure-ms-onedrive-doc-services&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

        The Microsoft OneDrive setup configured in ServiceNow is the same as that is done for Microsoft SharePoint as well. However, the Microsoft Azure App permissions are required for Microsoft SharePoint.

        **Note:** To set up connection you require Microsoft Azure App permissions such as email, openid, profile, Files.ReadWrite, offline\_access, User.Read, User.ReadBasic.All, Sites.ReadWrite.All.

    -   **Connection with Google Drive**

        To set up Google Drive as a cloud hosting service and to create or update the policy text document that resides in Google Drive, you must:

        1.  [Set up Google Drive spoke](https://www.servicenow.com/docs/access?context=setup-gdrive&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) account.
        2.  Integrate the Document Services with Google Drive. For more information, see [Document Services Framework for Google Drive](https://www.servicenow.com/docs/access?context=google-drive-spoke-document-services&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
        3.  To manage documents in Google Docs from your ServiceNow instance, you must integrate the ServiceNow instance with Google docs. For more information, see [Set up the Google Docs](https://www.servicenow.com/docs/access?context=setup-gdocs&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

## Setting up system properties to connect with cloud hosting services

-   **Enable system properties to use policy redlining in Compliance Workspace**
    1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **GRC properties**.
        1.  To opt Microsoft OneDrive as your cloud hosting service, select **One drive** in the **Select a file sharing service to host documents and attachments** system property list.

            If you select **None** in the **Select a file sharing service to host documents and attachments** system property list, then you can import the policy text. For more information, see [Import policy text for redlining](../task/import-policy-text-redlining.md).

        2.  To opt Google Drive as your cloud hosting service, select **Google drive** in the **Select a file sharing service to host documents and attachments** system property list.
        3.  To opt Microsoft SharePoint, select **SharePoint** in the **Select a file sharing service to host documents and attachments** system property list.
    2.  Set the folder path that is to be created in Microsoft OneDrive in the **Default folder path where documents and attachments will be located. You can organize files in sub-folders within this path** system property list.
-   **Provide mp\_document\_user role**

    The mp\_document\_user role is required to access policy redlining document-related tables. This role is required for users using the policy redlining feature to create, update, and delete the related documents.


As a sys admin you can establish the cloud hosting connection, enable system properties, and provide the mp\_document\_user role and compliance user \(sn\_compliance.user\) role for the policy redlining users.

