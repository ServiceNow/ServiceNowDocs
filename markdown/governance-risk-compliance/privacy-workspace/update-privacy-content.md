---
title: Activate privacy content
description: Activate an authority document or risk statement version to install the associated citations, control objectives, or risk statements into your privacy library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/update-privacy-content.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-10"
reading_time_minutes: 3
breadcrumb: [Privacy content accelerator, Privacy Management, Governance, Risk, and Compliance]
---

# Activate privacy content

Activate an authority document or risk statement version to install the associated citations, control objectives, or risk statements into your privacy library.

## Disclaimer

**Important:**

The ServiceNow Risk products help customers address regulatory requirements under various jurisdictions. However, we do not guarantee compliance and customers are ultimately responsible for their own compliance with applicable regulations.

ServiceNow aims to provide software updates for new or updated major regulations and requirements within twelve to eighteen months of the regulation's publication. For regulations for which ServiceNow provides a level of support in the base system, ServiceNow aims to provide software updates for minor regulatory changes within 12 months and for major regulatory changes within up to 18 months depending on scope and impact. We differentiate between typical regulatory content updates, which do not require software updates or enhancements, and regulatory updates, which do require software updates or enhancements. Content updates are generally delivered on a shorter cadence than if software update or enhancement is required for the regulatory update or change.

## Before you begin

Role required: sn\_privacy.manager

## Procedure

1.  In the Privacy Workspace, select the Privacy content icon.

2.  Select the **Privacy Frameworks** tab or the **Risk Statements** tab depending on the content you want to activate.

3.  On the **Inactive** sub-tab, locate the new authority document or risk statement version to install, and select **Activate**.

    The **Activate** button appears only when the authority document status or the risk statement version is **New**.

4.  Review the disclaimer, and select **Agree**.

    The installation wizard opens, showing records associated with the selected authority document or risk statement version.

    **Important:** Control objectives and risk statements are AI-generated. Although AI models are exposed to major privacy regulations, they aren't trained on the risk and compliance methodologies that your teams may use to derive a complete, consistent set of control objectives and risk statements from a regulation. Review each record for accuracy, scope, and fit with your internal taxonomy before you map it to processing activities or assessment questions.

5.  Select the records to install, and then select **Next**.

    Records that are ready to be installed show **Ready**, and those that are already installed in your library show **Installed**.

    **Note:** When you activate a new risk statement version, all risk statements appear as **Ready**, even those installed in the previous version. Reinstalling existing records from a new version can overwrite certain fields if they share the same name. To understand overwriting behavior, see [Overwrite behavior for existing records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/privacy-content-accelerator.md).

<table><thead><tr><th>

Record type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Citation**

</td><td>

Citations associated with the selected authority document. To view the source regulatory text related to citations, add **Supplemental guidance** as a column using the **Personalize fields** option.**Note:** Citation descriptions are AI-generated. Supplemental guidance is formatted by AI. Review all content for accuracy.

</td></tr><tr><td>

**Control objective**

</td><td>

Control objectives mapped to the selected citations. If no control objectives are mapped to the selected citations, proceed to the next step.

</td></tr></tbody>
</table>    |Record type|Description|
    |-----------|-----------|
    |**Risk statement**|Privacy risk statements available with the selected version.|

6.  Review the number of selected records, and select **Submit**.

    The status changes to **Updating** while installation is in progress.

7.  Refresh the page to verify that installation is complete.


## Result

-   The activated content moves to the **Active** sub-tab.
-   The content card displays the active version number.
-   The button label on the activated content changes to **Update**.
-   Access the installed authority document, citations, control objectives, and risk statements from the List view of the Privacy Workspace.

## What to do next

Update the activated authority documents to add more citations and control objectives.

Update the version of the privacy risk statements to add new statements to your library. See [Update privacy content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/update-privacy-mgmt-content.md).

