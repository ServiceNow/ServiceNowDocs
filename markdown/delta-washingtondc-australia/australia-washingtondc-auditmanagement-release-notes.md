---
title: Combined Audit Management release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Audit Management from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-auditmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Audit Management release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Audit Management from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Audit Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Audit Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Audit Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Manage your documents and work papers with Audit Management as cloud files](https://www.servicenow.com/docs/access?context=manage-cloud-docs-using-onedrive-int&family=washingtondc&ft:locale=en-US)**

Manage your documents and work papers with Audit Management as cloud files. This capability addresses specific use cases for the engagement and audit task records in the Audit Workspace. Link the cloud files to any GRC record and share a single cloud file with multiple records.

-   **[Create a Cloud file configuration on engagements and audit tasks](https://www.servicenow.com/docs/access?context=document-access-configuration&family=washingtondc&ft:locale=en-US)**

Manage access permissions on the cloud files. Use the Cloud file configuration module to assign the read and write permissions to the users of the cloud files.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Generate an audit report for an engagement using Microsoft Word template](https://www.servicenow.com/docs/access?context=generate-audit-report&family=xanadu&ft:locale=en-US)**

Use the Audit Workspace to generate audit reports for an engagement using Microsoft Word template to collaborate with your auditors in an effortless and user-friendly manner. You can manage the generated report as a cloud file either on cloud \(Microsoft SharePoint\) or as a sys\_attachment that is attached to the engagement record.

-   **[Cloud document management](https://www.servicenow.com/docs/access?context=manage-cloud-docs-using-onedrive-int&family=xanadu&ft:locale=en-US)**

Upload documents from your local computer as cloud files and link them to any record in ServiceNow. You can upload files to a predefined folder path and location.

-   **[User role enhancements in Audit Management](https://www.servicenow.com/docs/access?context=r_RolesInstallWAudit&family=xanadu&ft:locale=en-US)**

The following roles have been added:

    -   Use the Audit approver \(sn\_audit.approver\) role to approve an engagement and audit plan. Anyone with this role can be a part of an approver list. This role is also classified as a lite operator role.
    -   Use the Audit reader \(sn\_audit.reader\) role to view the audit-related entities, such as engagements, plans, observations, and audit tasks. Anyone with this role has exclusive read access to all the entities in the Audit Management application. This role is also classified as a lite operator role.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Matrix report in the Audit Workspace](https://www.servicenow.com/docs/access?context=matrix-report-audit-ws&family=yokohama&ft:locale=en-US)**

Analyze relationships between different variables by using a Matrix report that presents data in a structured format. Assess and document risks and the internal controls designed to mitigate those risks through the Risk and Controls Matrix.

-   **[Entity Based Access for Audit Management](https://www.servicenow.com/docs/access?context=c_Engagements&family=yokohama&ft:locale=en-US)**

Entity-based access enables you to create configurations for entities, entity classes, and entity types. When a user is qualified based on these configurations and has the minimum required roles, they can access to the following tables:

    -   Engagement
    -   Test Plan
    -   Control Test
    -   Observation
    -   Control to Engagement
    -   Test Plan to Engagement
    -   Risk to Engagement
    -   Issue to Engagement
    -   Entity to Engagement

</td></tr><tr><td>

Zurich

</td><td>

-   **Audit Period Start and End Dates [\[Placeholder link text to key t\_CreateEngagement\]](https://www.servicenow.com/docs/access?context=t_CreateEngagement&family=zurich&ft:locale=en-US)**

Set audit period start and end dates directly on Engagement records to focus audits on specific time-frames. The system displays only indicator results that fall within your defined audit period, keeping the audit time-frame separate from the overall engagement time-frame. This helps you audit past or future periods without affecting the broader engagement timeline.

-   **[\[Placeholder link text to key unified-content-management\_0\]](https://www.servicenow.com/docs/access?context=unified-content-management_0&family=zurich&ft:locale=en-US)**

Simplify the installation of pre-configured content packs with the new Unified content management icon in the Audit Workspace. Content Accelerator includes the Digital Operational Resilience Act \(DORA\) content pack, offering citations and authority documents for DORA compliance. Audit shared manager and Audit WS supervisor roles can access Content Accelerator.

-   **[Enhancement to evidence request](https://www.servicenow.com/docs/access?context=evidence-request&family=zurich&ft:locale=en-US)**

Create evidence response directly in one step. This bypasses the step involved in creation of evidence request and collection details. Evidence response is enhanced with additional data of source and context. To leverage evidence capabilities, feature roles have been introduced:

    -   sn\_grc\_advanced.evidence\_reader
    -   sn\_grc\_advanced.evidence\_requester
    -   sn\_grc\_advanced.evidence\_responder
    -   sn\_grc\_advanced.evidence\_admin
-   **[Integration with ITAM](https://www.servicenow.com/docs/access?context=solutions-gallery&family=zurich&ft:locale=en-US)**

Leverage Audit Management support as an ITAM customer through dedicated feature roles. A lightweight version of the Audit Management workspace is available, which includes the following features:

    -   On the Audit Management home page, you can track **Timeline**, **Engagements**, **Tracking**, **Create evidence request**, and **.**
    -   The lightweight Audit Management also includes the key capabilities, such as Engagement, Entity Scoping, Activities, and Evidence when Advanced Core is installed.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Audit Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Analytics and Reporting Solutions for Audit Management in Next Experience UI Framework](https://www.servicenow.com/docs/access?context=grc-audit-mgmt-content-pack&family=washingtondc&ft:locale=en-US)**

Starting with version 18.1.0 of the Audit Management application, the Analytics and Reporting solutions for Audit Management such as the Audit Engagement Overview dashboard and Audit Manager dashboard are available in the Next Experience UI Framework.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Domain separation and Audit Management](https://www.servicenow.com/docs/access?context=audit-management-domain-separation&family=xanadu&ft:locale=en-US)**

Changes are made to the domain assignment process to manage data segregation by the Managed Service Providers related to the objects in Audit Management and Advanced Audit.

-   **[Role change for users approving workflows](https://www.servicenow.com/docs/access?context=r_RolesInstallWAudit&family=xanadu&ft:locale=en-US)**

Approvers for an engagement and audit plan can also use the Audit approver \(sn\_audit.approver\) role as a lite operator role to approve audit workflows.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US)**

The Audit Management configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Audit Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Audit Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Audit Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install Audit Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Audit Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Audit Management by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Audit Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Audit Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Audit Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Audit Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Audit Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Manage your documents and work papers with Audit Management as cloud files.
-   Link the cloud files to any GRC record and share a single cloud file with multiple records.
-   Manage access permissions on the cloud files.

 See [Audit Management](https://www.servicenow.com/docs/access?context=c_GRCAudits&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Manage your documents and work papers in Audit Management as cloud files.
-   Link cloud files to any GRC record and share a single cloud file with multiple records.
-   Upload documents from your local computer as cloud files and link them to any record in ServiceNow.
-   Use the lite roles introduced in Audit Management for lighter business operations.

 See [Audit Management](https://www.servicenow.com/docs/access?context=c_GRCAudits&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Analyze relationships between different variables, such as assessing risks and controls, by using the Matrix report in Audit Workspace.
-   Manage your documents and work papers in Audit Management as cloud files.
-   Upload documents from your local computer as cloud files and link them to any record in your ServiceNow instance.
-   Share a single cloud file with multiple records by linking it to any GRC record.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

 See [Audit Management](https://www.servicenow.com/docs/access?context=c_GRCAudits&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Set audit time frames within engagements using new audit date fields. Filter indicator results by specific periods, independent of the overall engagement time frame.
-   Access pre-configured content packs through the new Content Accelerator icon in the Audit Workspace. This includes the Digital Operational Resilience Act \(DORA\) pack with citations and authority documents.
-   Create evidence responses quickly with a simplified process.
-   Access engagements, add existing entities to an engagement, and create activities in the Lite Audit workspace, which is a simplified version of the Audit Management workspace. If the advance core store app is installed, evidences can also be associated with the engagement.

 See [Audit Management](https://www.servicenow.com/docs/access?context=c_GRCAudits&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

