---
title: Document access in a legal matter
description: Documents attached to legal matters are uploaded to the configured external storage system when the external storage option is enabled on an intake form with All or matter type selected. The access permission of these documents to various personas is controlled in real time, via a scheduled job, or on-demand.
locale: en-US
release: australia
product: Legal Matter Management
classification: legal-matter-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create an artifact for a legal matter, Work on a legal matter, Use, Legal Matter Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Document access in a legal matter

Documents attached to legal matters are uploaded to the configured external storage system when the external storage option is enabled on an intake form with All or matter type selected. The access permission of these documents to various personas is controlled in real time, via a scheduled job, or on-demand.

## Document access in legal matters for various personas

The following table shows the type of access to documents and when it is granted to various personas.

|Persona|Access type|Access level|When|
|-------|-----------|------------|----|
|Requester, requested for|Read only|Document|Legal matter is submitted|
|Group manager|Read, Write, Delete|Legal matter|Legal matter is submitted or promoted from legal request|
|Matter owner \(Assigned to\)|Read, Write, Delete|Legal matter|Legal matter is assigned|
|Collaborators|Read, Write, Delete|Legal matter|Added to the **Collaborators** list|
|Ad hoc approvers|Read only, No delete|Legal matter, artifact, or document based on approval requested|Ad hoc approval is initiated|
|Matter task owner|Read only, No delete|Artifact|Artifact is associated to a matter task or when a task is assigned to a user|
|Matter task owner|Read only, No delete|Document in artifact associated with the matter task|Artifact is associated to a matter task or when a task is assigned to a user|
|Members of assignment group|Depends on the **Assignment group permission** field|Document|Job is run as scheduled, or on-demand|
|Watch list users|Read only, No delete|Legal matter|Added to the **Watch list**|
|Delegates|Read only, No delete|Legal matter, artifact, or document based on duties delegated|**Resolve platform delegation permissions for legal matter** job is run as scheduled, or on-demand|
|Delegates through granular delegation|Read only, No delete|Legal matter, artifact, or document based on duties delegated|User is delegated|

The scheduled job **Process External Storage Permissions** runs at the defined intervals to sync access for all unprocessed permissions on documents for legal matters stored in the external storage.

**Note:**

-   Requesters can access documents attached to their legal requests from the **Documents** tab on the Standard Ticket page.

    **Note:** Requesters can delete only those documents from the request that they've attached.

-   The matter owner assigned to the legal matter can access documents from the **Documents** tab of the Artifacts record in the Legal Counsel Center.
-   Users added to the matter can request on-demand access to documents if they need access before the scheduled job is run.
-   The legal admin can revoke a user's access to documents of a legal matter and legal requests.
-   Ad hoc approvers lose document access after they approve or reject the requested item.
-   Delegates lose access after the delegation period expires.

-   **[Request document access for a legal matter](../task/request-doc-access-legal-matter.md)**  
Request access to documents attached to a legal matter that you do not currently have access to.
-   **[Remove document access of users in a legal matter](../task/remove-doc-access-legal-matter.md)**  
Remove existing users' access to documents attached to a legal matter's artifact when they are no longer required to view those documents.

**Parent Topic:**[Create an artifact for a legal matter](../task/add-artifact-to-legal-matter.md)

