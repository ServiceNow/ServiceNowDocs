---
title: Defining Document Parameters
description: Before using the Managed Documents application, the user with the document\_management\_admin role needs to set the parameters that define the kinds of documents to be managed through the application. Managed Documents provides both base and custom parameter options.
locale: en-US
release: xanadu
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Features, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Defining Document Parameters

Before using the Managed Documents application, the user with the `document_management_admin` role needs to set the parameters that define the kinds of documents to be managed through the application. Managed Documents provides both base and custom parameter options.

## Defining Document Parameters

The following document parameters should be defined:

-   **Type:** identifies the purpose of the document. The type also determines the default document format and name format.
-   **Classification:** indicates the security level assigned to the document and determines who can view or edit the document.
-   **Audience:** specifies the intended readers of the document.
-   **Name format:** specifies the name format to use when a document revision is added.
-   **Name components:** are individual identifiers used inside a name format. Name components define a reference path \(often by dot-walking\) that holds the value specific to the document.
-   **Approval rules:** determine which approvers are added to documents \(in addition to the **Reviewers** specified on the document record\).

## Defining Types

To define a new type, navigate to **Managed Documents** &gt; **Administration** &gt; **Type** and click **New**.

|Field|Description|
|-----|-----------|
|Name|A unique name for the type.|
|Code|A short code for the type. Referenced as a name component for the name format.|
|Label|A label to display in the **Type** choice list.|
|Name Format|The name format that documents of this type will use.|
|Order|A number indicating the type's sequence in the choice list.|

The following types are available in the base system.

|Name|Code|Label|Name format|Order|
|----|----|-----|-----------|-----|
|-- None --|null|-- None --|null|1|
|policy|POL|Policy|Default Policy|2|
|guideline|GUI|Guideline|Default|3|
|procedure|PROC|Procedure|Default|4|
|contract|CON|Contract|Default|5|

**Note:** For documents with a **Type** of **Contract**, a **Contracts** related list appears on the document record, listing any contracts the document is associated with.

-   **[Defining Approval Rules](r_DefiningApprovalRules.md)**  
To define a new approval rule, navigate to **Managed Documents** &gt; **Administration** &gt; **Approval Rules** and click **New**.
-   **[Defining Audiences](r_DefiningAudiences.md)**  
To define a new audience, navigate to **Managed Documents** &gt; **Administration** &gt; **Audience** and click **New**.
-   **[Defining Classifications](r_DefiningClassifications.md)**  
Define a new classification on the Classification form.
-   **[Defining Name Components](r_DefiningNameComponents.md)**  
Name components define the document values used in the name format.
-   **[Defining Name Formats](r_DefiningNameFormats.md)**  
The name format automatically generates a name for a document revision by arranging name components in a standard code to match naming conventions.

**Parent Topic:**[Managed Document features](r_ManagedDocumentFeatures.md)

