---
title: Post case reviews
description: Use a post case review to capture details about a resolved case, including a summary of the issue, affected assets, root cause, resolution, and any preventive measures.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-08-06"
reading_time_minutes: 3
breadcrumb: [Customer Service case digests, Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Post case reviews

Use a post case review to capture details about a resolved case, including a summary of the issue, affected assets, root cause, resolution, and any preventive measures.

## Creating a post case review

Customer service agents can create post case reviews for cases that are in the **Resolved** state.

Agents can select the **Create Post Case Review** UI action to create a post case review document. This action creates a case action summary record and adds the record to the Related Records section on the Case form in the **Post Case Review** field.

## Publishing a post case review

Agents can preview a post case review document before publishing and, if necessary, have the document reviewed and approved.

Agents can add an approval group or approval users to the Post Case Review record and then request approval. The system sends an email notification to the approvers with a link to the post case review document. The approvers can either approve the document or suggest changes by adding them to the **Work notes** field on the Post Case Review record.

When an agent publishes a post case review document, the system adds a link to a PDF of the document in the **Additional comments** field on the Case form. The system also adds the record to the Related Records section on the Case form in the **Post Case Review** field. If the document is available to customers, the link is visible from the Customer and Consumer Service Portals.

## Post case review configuration records

The configuration selected for post case review documents identifies the information from the case that is captured and populated in post case review record. The configuration also specifies the template that the system uses to create the post case review document.

## Closing a case while a post case review is in progress

If a case is closed while the post case review document is in progress, agents can still update the **Additional comments** on the Case form with the post case review document link. Once a case is closed, the Post Case Review form displays a message that the associated case has been closed.

## Post case review actions by role

Customer service roles can perform the following actions for post case review documents.

<table id="table_ctm_t15_d3b"><thead><tr><th>

Role

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Customer service agent

</td><td>

-   Create and preview one post case review document for a resolved case.
-   Request approval using an optional approval workflow.
-   Publish a post case review document to a case.
-   Reopen and edit a published post case review document.

</td></tr><tr><td>

Customer service manager

</td><td>

Review, approve, and suggest changes to post case review documents.

</td></tr><tr><td>

Major issue manager

</td><td>

-   Create and publish post case review documents for resolved major cases.
-   Copy the documents to the associated child cases.

</td></tr><tr><td>

Customer

</td><td>

View post case review documents from the Customer and Consumer Service Portals.

</td></tr></tbody>
</table>## Post case reviews for major cases

Customer service managers and major issue managers can create and publish post case review documents for resolved major cases. These documents capture the case data specified in the configuration but do not include account-specific information. The customer service manager can also copy a post case review document to the associated child cases. The system adds the account-specific information when it generates the document for each child case.

The system administrator can enable post case review documents for major cases by setting the **sn\_customerservice.parent\_child\_case\_sync** system property to true.

**Note:** Setting this property to true disables the **Create Post Case Review** UI action for child cases.

**Related topics**  


[Create a post case review](../task/create-case-review-document.md)

[Create a post case review for a major case](../task/create-case-review-document-mim.md)

