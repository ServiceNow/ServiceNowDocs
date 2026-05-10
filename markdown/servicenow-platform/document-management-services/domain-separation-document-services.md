---
title: Domain separation and Document Management
description: Domain separation is supported for Document Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [References, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Document Management

Domain separation is supported for Document Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Overview

Document Management provides an access level approach to controlling the document access and providing security to the users.

## How domain separation works in Document Management

When domains are separated in Document Management, users can see and manage documents and give access privileges only in their own \(tenant\) domain.

A user in the parent domain has access to documents in the child domain.

When a user creates a document, document list or document entries, then their domain is the same as the user's domain.

When the owner of the document changes then the related versions, references, and permission record's domain is updated with the domain of the parent document.

## Use cases

-   **Documents**

    Documents can be edited or accessed only within their domain. Access to a document can become void if a user belongs to a different domain from the document's domain.

    -   Users in the global domain can access documents in all domains when the read access is granted to the user.
    -   Users in a non-global domain can access documents only in the same domain and global domain when document access is granted to the user.
-   **Versions, References and Permissions table**
    -   Users can access the versions, references, and, permissions table records only if they have access to the parent document.
    -   If a user has access to the target record in the references table, access to the parent document is granted only if inherited access is enabled for the document and the user is in the same domain as the parent document.
-   **List and List Entries**

    List and List Entries have domain pointing to the current user domain and can be accessed by the users with document admin rights.


## Known issues

If a document contains references and if the owner of the document is changed and does not have access to the target record of one of the references, then the reference record might not be visible to the new owner.

For example, if the document owner, User A \(Domain: D1\) is changed to User B \(Domain: D2\) and User B does not have access to the target record of the reference table, User B might not be able to see the reference record.

**Parent Topic:**[References](reference-document-management.md)

**Related topics**  


[Components installed with Document Management](../reference/installed-with-doc-mgmt.md)

[Document Management roles](../reference/document-management-roles.md#)

[Granular admin roles in Document Management](../reference/granular-admin-roles-dms.md)

[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

