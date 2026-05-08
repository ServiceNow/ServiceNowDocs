---
title: Personal authentication
description: Personal authentication enables individual users to authenticate with their personal accounts within ServiceNow using a secure connection between the user's identity and their corresponding Microsoft OneDrive or Google Drive account, allowing users to access, view, and manage their personal files directly from ServiceNow.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate with Document Services, Multi Provider Document Services Framework, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Personal authentication

Personal authentication enables individual users to authenticate with their personal accounts within ServiceNow using a secure connection between the user's identity and their corresponding Microsoft OneDrive or Google Drive account, allowing users to access, view, and manage their personal files directly from ServiceNow.

## Personal authentication for Microsoft OneDrive

Personal authentication allows users to securely connect their individual Microsoft OneDrive accounts to Document Management. This enables user-specific access to files stored in Microsoft OneDrive, supporting personalized document handling such as attaching, viewing, or managing files directly within ServiceNow records.

This authentication method uses OAuth 2.0 to authorize each user, ensuring that file access and operations are performed under their unique identity. Each user connects to their own Microsoft OneDrive account, ensuring privacy and personalized access.

For more information, see Personal Authentication.

## Personal authentication for Google Drive

Personal authentication for Google Drive enables users to securely link their individual Google accounts with Document Management. This integration allows users to access, upload, and manage files from their personal Google Drive within ServiceNow, ensuring that all document interactions are authenticated under the user’s unique identity.

For more information, see Personal Authentication.

## Personal Authentication dashboard

Use your personal credentials to connect to third-party integrations. View, authenticate, revoke, and renew your personal authentications through a simplified, consolidated interface. For more information, see Using the Personal Authentication dashboard.

**Note:** The personal authentication dashboard can be accessed by users with `sn_personal_auth.personal_auth_user` role.

-   **[Configure personal authentication for Multi Provider Document Services Framework](../task/configure-personal-authentication-mp.md)**  
Configure and enable personal authentication for Microsoft OneDrive and Google Drive accounts in Multi Provider Document Services Framework.
-   **[Authenticate Microsoft OneDrive account](../task/authenticate-onedrive-account.md)**  
Enable personal authentication for Microsoft OneDrive for Multi Provider Document Services Framework.
-   **[Authenticate Google Drive account](../task/authenticate-google-drive-account.md)**  
Enable personal authentication for Google Drive for Multi Provider Document Services Framework.

**Parent Topic:**[Integrate with Document Services](../reference/integrate-with-document-services-mp.md)

