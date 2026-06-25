---
title: Privacy content accelerator
description: The privacy content accelerator provides prebuilt privacy content that you can activate directly from the Privacy Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/privacy-content-accelerator.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-10"
reading_time_minutes: 5
breadcrumb: [Privacy Management, Governance, Risk, and Compliance]
---

# Privacy content accelerator

The privacy content accelerator provides prebuilt privacy content that you can activate directly from the Privacy Workspace.

## Disclaimer

**Important:**

The ServiceNow Risk products help customers address regulatory requirements under various jurisdictions. However, we do not guarantee compliance and customers are ultimately responsible for their own compliance with applicable regulations.

ServiceNow aims to provide software updates for new or updated major regulations and requirements within twelve to eighteen months of the regulation's publication. For regulations for which ServiceNow provides a level of support in the base system, ServiceNow aims to provide software updates for minor regulatory changes within 12 months and for major regulatory changes within up to 18 months depending on scope and impact. We differentiate between typical regulatory content updates, which do not require software updates or enhancements, and regulatory updates, which do require software updates or enhancements. Content updates are generally delivered on a shorter cadence than if software update or enhancement is required for the regulatory update or change.

## Accessing the privacy content accelerator

Privacy Management Content provides prebuilt authority documents, citations, control objectives, and risk statements. These are aligned with major privacy frameworks, such as GDPR, CCPA, LGPD, NIST Privacy Framework 1.0, Virginia Consumer Data Protection Act \(CDPA\), Colorado Privacy Act, and DPDPA.

A dedicated icon in the Privacy Workspace provides navigation to the privacy content accelerator. Only users with the privacy manager or privacy admin roles can access this icon.

## Content tab

The privacy content accelerator page contains two tabs:

-   **Privacy Frameworks**

    Displays the available authority documents. Each authority document card shows the count of related citations and control objectives.

-   **Risk Statements**

    Displays risk statement categories. Each category card shows the version and provides an option to activate or update the associated risk statements.


**Note:** The cards also show the current status, and the version number when an active version exists.

Both tabs organize content into two sub-tabs by installation state:

-   **Inactive**

    Lists the authority documents and risk statement versions that aren't installed in your library. Cards on this sub-tab show the **Activate** button. To install content from this sub-tab, see [Activate privacy content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/update-privacy-content.md).

-   **Active**

    Lists the authority documents and risk statement versions currently installed in your library. Cards on this sub-tab show the active version number and the **Update** button. To update the activated content in your library, see [Update privacy content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/update-privacy-mgmt-content.md).


## Content status

Each authority document and risk statement card shows one of the following statuses:

-   **New**

    The authority document or the risk statement version hasn't been installed. The card displays an **Activate** button.

-   **Active**

    The authority document or the risk statement version is installed. The card displays the active version number and an **Update** button.


## Installing content

When you activate or update an authority document or a privacy risk statement version, the installation wizard opens. The wizard displays the list of citations and control objectives associated with the authority document, and risk statements available for the selected version.

**Important:** Control objectives and risk statements are AI-generated. Although AI models are exposed to major privacy regulations, they aren't trained on the risk and compliance methodologies that your teams may use to derive a complete, consistent set of control objectives and risk statements from a regulation. Review each record for accuracy, scope, and fit with your internal taxonomy before you map it to processing activities or assessment questions.

<table id="table_rs_columns"><thead><tr><th>

Column name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Name of the citation, control objective, or risk statement.

</td></tr><tr><td>

**Description**

</td><td>

Description of the citation, control objective, or risk statement.**Note:** All descriptions are AI-generated. Check AI-generated content for accuracy.

</td></tr><tr><td>

**Installation state**

</td><td>

Current installation state of the record. After you activate or update privacy content, selected citations, control objectives, or risk statements transition from **Ready** to **Installed**.-   **Ready**: Records that haven't yet been installed.
-   **Installed**: Records that are installed and active in your library.

**Important:** When you update to a new version of privacy risk statements, previously installed risk statements also appear as **Ready** by default. While this doesn't mean that existing records are removed from the library, reinstalling them may overwrite certain fields.

</td></tr><tr><td>

**Parent**

</td><td>

The parent record of the selected citations, control objectives, or risk statements. **Note:** If a parent citation has not been installed, the parent field on child citation records displays an empty value. The parent citation value is populated after the parent citation is installed. The same behavior applies to related control objectives.

</td></tr><tr><td>

**Supplemental guidance**

</td><td>

Source regulatory text related to the citations.**Note:** Supplemental guidance is formatted by AI. Review all content for accuracy.

If you don’t see this column, add it using the **Personalize fields** option.

</td></tr></tbody>
</table>## Content reference records

When an authority document is activated, a content reference record is created in your library. This record stores the active version and links to all citations installed for that authority document. Each citation record, in turn, lists its associated control objectives.

## Risk statement versioning

Privacy risk statements are shipped in versioned sets. Each new version includes the risk statements from the previous version and adds new ones. To activate a new version, see [Activate privacy content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/update-privacy-content.md).

When you activate a new risk statement version, all risk statements appear as **Ready**, even those installed in a previous version. Reinstalling existing records from a new version can overwrite certain fields if they share the same name.

## Overwrite behavior for existing records

-   **Citations**

    If a citation with the same name already exists in the instance and it belongs to the same authority document, installing the content pack version overwrites the existing record.

-   **Risk statements**

    If a risk statement with the same name already exists in your instance, reinstalling it overwrites the existing record.

    \[Omitted image "prm-content-overwrite-ver.png"\] Alt text: Flowchart showing risk statement overwrite behavior based on name matching and field changes.

    When you select the risk statements to install, they are matched against the ones already in your library by their name and category. The category is the same for all privacy risk statements. Each privacy risk statement is therefore uniquely identified by its name. Unique records are installed as new. Matching records are overwritten.

    On each matched risk statement, all edits to the following fields are overwritten with values from the incoming record:

    -   Description
    -   Expected ALE
    -   Level
    -   Tolerance status
    -   Active
    -   Leaf
    -   License
    -   Order
    -   State
    All changes to the related lists and fields outside the ones listed above are preserved.

    Before updating, review your library for risk statements changed since the last activation or update. If updating would overwrite a change you must retain, rename the record before updating. This creates a separate record of the reinstalled risk statement, preserving all changes in the old record.


