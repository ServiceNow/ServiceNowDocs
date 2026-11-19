---
title: Unified Content Management \(UCM\)
description: Unified Content Management \(UCM\) is the shared foundation that your risk and compliance applications use to organize, version, and deliver regulatory content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-common-functions/ucm-shared-architecture.html
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 6
keywords: [Unified Content Management, UCM, Content Library, content pack, Content Delivery Service, CDS, version management]
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Unified Content Management \(UCM\)

Unified Content Management \(UCM\) is the shared foundation that your risk and compliance applications use to organize, version, and deliver regulatory content.

## UCM overview

Risk and compliance programs are only as reliable as the regulatory content behind them. When a law or framework changes, your frameworks, citations, and control mappings need to change with it. Previously, updated content reached you only through a new application release, so staying current meant waiting for a release, upgrading, and reconciling versions yourself. UCM now delivers content separately from application releases, so updates reach your instance as they become available.

The following applications use or build on UCM.

<table id="table_a4x_t5d_tkc"><thead><tr><th>

Application

</th><th>

Content delivery

</th><th>

Content provided

</th><th>

Related topics

</th></tr></thead><tbody><tr><td>

Policy and Compliance Management

</td><td>

UCM \(sn\_esg\_content\)

</td><td>

Authority documents, citations, control objectives

</td><td>

[UCM in Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/unified-content-management.md)

</td></tr><tr><td>

Operational Sustainability Management

</td><td>

UCM \(sn\_esg\_content\)

</td><td>

Frameworks, citations, metric definitions, emission factors

</td><td>

[ESG content accelerator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/environmental-social-governance/esg-content-accelerator.md)

</td></tr><tr><td>

Privacy ManagementPrivacy Management

</td><td>

Privacy Management Content \(sn\_privacy\_content\) with a dependency on UCM

</td><td>

Authority documents, citations, control objectives, risk statements

</td><td>

[Privacy content accelerator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/privacy-content-accelerator.md)

</td></tr><tr><td>

AI Risk and Compliance

</td><td>

AI Risk and Compliance Content \(sn\_grc\_ai\_gov\_cont\) with a dependency on UCM

</td><td>

Agencies, authority documents, citations, control objectives, risk statements

</td><td>

[AI Risk and Compliance Content Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/ai-risk-management/airc-content-pack.md)

</td></tr><tr><td>

Third-party Risk Management

</td><td>

UCM \(sn\_esg\_content\)

</td><td>

Smart assessment templates

</td><td>

-   [Managing TPRM SAE templates with Unified Content Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/third-party-risk-management/tprm-integrating-ucm.md)
-   [Activate or update Smart Assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/third-party-risk-management/activate_sae_ucm.md)

</td></tr><tr><td>

Audit Management

</td><td>

UCM \(sn\_esg\_content\)

</td><td>

Frameworks, citations

</td><td>

[UCM in Audit Management](https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/audit-management/unified-content-management_0.html)

</td></tr></tbody>
</table>While each application provides its own content, UCM handles how that content is organized, versioned, and delivered.

## Benefits of UCM

-   Multiple frameworks are available to choose from based on your organization's requirements.
-   Citations within a framework can be installed selectively, so you install only the ones you need.
-   Activating a framework enables you to install associated citations, control objectives, metric definitions and other content already mapped to each other.
-   Control objectives can link to citations from more than one framework, so one control can address overlapping requirements. For example, the AI Risk and Compliance content pack maps about 300 control objectives across the EU AI Act, NIST AI RMF, California AI Act, and Colorado AI Act.
-   New frameworks and newer versions of existing frameworks appear in the content library as they're released, and you choose when to activate or update them.

## Content library and content packs

All UCM content comes from the content library, a repository of content curated from authoritative sources such as regulators and standards bodies. The library organizes content into the following types.

-   **Agencies**

    Regulatory bodies and standards organizations, such as the European Commission or ISO, that issue content.

-   **Authority documents**

    Source regulations, frameworks, or standards, such as GDPR or the EU AI Act.

-   **Citations**

    Individual clauses, articles, or sections within an authority document.

-   **Control objectives**

    Goals a control is meant to achieve, each linked to the citations it addresses.

-   **Risk statements**

    Standardized descriptions of risks associated with a framework or domain.

-   **Assessment templates**

    Reusable questionnaires and evaluation formats, such as impact assessments, built from the library's content.


Content in the library is grouped into content packs by business domain, such as privacy or third-party risk. The packs available to you depend on the applications you've installed.

## Content delivery

UCM delivers content through the Continuance Delivery System \(CDS\), a platform service that sends content to your instance separately from application releases. UCM checks CDS for new content on a schedule and adds it to the content library on your instance, where you can activate or update it. When you activate a content pack, UCM copies its content into your installed application's records. You can then use the content as provided or edit it to fit your organization's requirements. To fetch new UCM content from the CDS manually, see [Fetch UCM content updates manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/fetch-ucm-update-manual.md).

## Installing UCM

Depending on the application you use, install the respective plugin from the ServiceNow Store.

-   For Policy and Compliance Management, Operational Sustainability Management, Audit Management, or Third-party Risk Management, install UCM \(sn\_esg\_content\).
-   For Privacy Management, install Privacy Management Content \(sn\_privacy\_content\), which installs UCM as a dependency.
-   For AI Risk and Compliance, install AI Risk and Compliance Content \(sn\_grc\_ai\_gov\_cont\), which installs UCM as a dependency.

After installation, open UCM by selecting the UCM icon \[Omitted image "unified-content-mgmt-icon.png"\] Alt text: in your application's workspace.

## UCM home page

The UCM home page shows the available content in your library, grouped into tabs by content type, such as Frameworks &amp; Regulations, Risk Statements, and Emission Factors. Each item appears as a card that shows its name, a short description, and its state, such as New, Active, or Error. You can activate or update content from its respective card.

\[Omitted image "ucm-landing.png"\] Alt text: UCM landing page in the compliance workspace showing the available content packs to be activated or updated.

Each tab organizes content into two sub-tabs by their installation state.

-   **Inactive**

    Content that you haven't activated yet. Each card shows the New status and an **Activate** button.

-   **Active**

    Content that you have activated. Each card shows the currently active version and an **Update** button.


When you activate or update a framework, you select which of its associated content, such as citations, control objectives, or metric definitions, applies to your organization. The content you select is added to your instance already mapped to the framework and to each other, so you don't have to create those mappings yourself.

## Content versioning

When regulations change, updated content is released in numbered versions. Each version is stored as its own record, so when a new version is released, it arrives as an additional record. You control which version is in use. Selecting **Activate** installs a version you haven't used before. Selecting **Update** enables you to apply a new version's content to the record you have already installed.

**Note:** Updating applies the newer content to your installed records, which can overwrite changes you made to them. To keep your changes, rename the customized record before you update. The update then creates a new record and leaves your renamed record unchanged.

-   **[Fetch UCM content updates manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/fetch-ucm-update-manual.md)**  
Manually fetch the latest Unified Content Management \(UCM\) content from the Continuance Delivery System \(CDS\) to bring new content and updates to your content library.

**Parent Topic:**[Common Governance, Risk, and Compliance features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/common-grc-features.md)

