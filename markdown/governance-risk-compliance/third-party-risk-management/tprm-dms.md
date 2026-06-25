---
title: Document Management system in Third-party Risk Management
description: Learn how the enhanced Document Management system supports third-party collaboration and internal workflows in Third-party Risk Management \(TPRM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-dms.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 6
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Document Management system in Third-party Risk Management

Learn how the enhanced Document Management system supports third-party collaboration and internal workflows in Third-party Risk Management \(TPRM\).

## Document Management Overview

Starting with version 21.1.x, the Document Management System \(DMS\) in Third-party Risk Management \(TPRM\) provides a centralized repository for storing, organizing, and managing third-party documents throughout the vendor life cycle. DMS streamlines evidence tracking, reduces duplication, and improves audit readiness by enabling document reuse across assessments, contracts, issues, and tasks. Access DMS in the Vendor Management Workspace or third-party portal to create, manage, and reference documents. Primary contacts manage permissions in the portal. TPR assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\], TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], and TPR administrators have write access, while third-party assessment reviewers \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] have read-only access. DMS supports metadata, version control, search, reporting, and audit tracking for all document actions.

The DMS is accessible for internal users through the Documents module in the Vendor Management Workspace as shown in the following example.

\[Omitted image "tprm-new-doc-dms.png"\] Alt text: Documents module in the Vendor Management Workspace.

The DMS is accessible for external users through the Third-party portal as shown in the following example.

\[Omitted image "tprm-dms-portal.png"\] Alt text: DMS in the third-party portal. For detailed descriptions refer to the paragraphs preceding and following this image.

## Key capabilities

-   Third-party contacts can upload and manage documents using the third-party portal.

    For more information, see [Upload and manage documents in the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-add-document-portal.md).

-   Internal users can create and access document records through the Documents module in the Vendor Management Workspace.

    For more information, see [Create a document record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-document.md).

-   Users can manage document versions, download attachments, and track their metadata.

    For more information, see [Create a document version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-document-version.md).

-   Documents can be linked to multiple TPRM record types with auto-rollup:

    -   Tasks
    -   Issues
    -   Engagements
    -   Assessments
    For more information, see [Link documents to a TPRM record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-link-document.md).

-   Internal users can manage role-based permissions for primary contacts and other internal users.

    For more information, see [Define document sharing permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-doc-share-permissions.md).

-   Each document version supports download options, advanced search and reporting for metadata and relationships, and complete audit tracking of actions and version history.

## Document life cycle and traceability

Each document captures metadata including creation date, type, description, version, and status. Metadata is used for classification, reporting, and workflow routing.

Each document supports multiple versions. TPR assessors, managers, and administrators can upload new versions, view version history, and download attachments for any version. Versions are sorted by creation date in descending order.

Documents can be linked to assessments, engagements, issues, and tasks. These references automatically roll up to related third-party records. Duplicate references aren’t allowed.

**Note:** A linked document is a document record associated with another record \(assessment, engagement, issue, or task\) for traceability and reporting. Linking creates a formal relationship that supports life-cycle tracking. A reference is the entry that represents this link, shown in the document’s References tab and the related record’s Documents list. Each reference includes metadata like record type and ID. The key difference is that linking is the action and a reference is the result. Multiple references to one document are possible, but duplicate references to the same record aren’t allowed.

All document actions including uploads and version updates are tracked for audit purposes. Audit logs are accessible to authorized users.

## Collaboration and insights

All actions, including approvals and rejections, are tracked in the audit log for transparency and reporting. You can search documents by metadata fields and generate reports on document usage, status, and relationships. Filters include document type, risk category, expiration date, and third-party association. You can generate reports on document usage, version history, and linked records using the Reports module or Performance Analytics.

Report types can include:

-   Document inventory report with metadata and version details.
-   Linkage report showing documents associated with assessments, engagements, and tasks.
-   Audit report for document actions and life-cycle events.

## DMS and Smart assessment

If you have the third‑party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can access and use third‑party and engagement documentation during assessment activities. The Document Management System \(DMS\) works with SAE to make documents available during assessments. When a document is uploaded or updated in DMS, the system retrieves the file and associated metadata so the information can be made available during assessment activities.

This capability reduces manual effort by ensuring that essential vendor documentation remains accessible throughout the assessment process, while still allowing users to review, edit, and finalize their responses.

For more information, see [AI-assisted questionnaire pre-fill using the Document Management System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae.md).

## Now Assist document skills

If your organization uses DMS and Now Assist for TPRM, you can leverage AI-driven skills to streamline document-heavy workflows. These capabilities reduce manual effort, improve accuracy, and accelerate risk tasks. Now Assist for Document Management and Now Assist for TPRM offer the following key skills:

-   TPRM issue summarization– Condenses complex third-party risk issues into actionable summaries, helping risk analysts review and respond faster.

    For more information, see [TPRM issue summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/issue-summarization-tprm.md).

-   Smart documents – Summarizes risk management documents and provides quick Q&amp;A, reducing manual review and speeding up due diligence.

    For more information, see [Smart Documents Skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-smart-documents.md).

-   Extract information from documents – Uses AI to pull specific data points \(such as risk indicators, compliance clauses, or contract terms\) from large documents, reducing manual review time and improving accuracy.

    For more information, see [Now Assist extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-extract-information-from-documents.md).


For more information on Now Assist for Document Management skills, see [Explore Now Assist in Document Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/explore-now-assist-in-document-management.md).

## Limitations

-   External users can’t preview documents due to restrictions; they must download documents from the portal to view them.
-   The third-party field is optional when creating a document. However, if the document is associated with a third party, this field is required. For internal documents with no third-party association, the field can remain empty.
-   Document creation and versioning currently require separate steps.

**Related topics**  


[Create a document record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-document.md)

[Create a document version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-document-version.md)

[Link documents to a TPRM record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-link-document.md)

[Define document sharing permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-doc-share-permissions.md)

[Upload and manage documents in the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-add-document-portal.md)

[Document approval and publish process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/document-review-approval.md)

[Exploring Document Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/explore-doc-management.md)

[Explore Now Assist in Document Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/explore-now-assist-in-document-management.md)

[Exploring Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-docintel.md)

