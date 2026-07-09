---
title: Update content in the privacy library
description: Update an installed authority document or risk statement version to add newer citations, control objectives, and risk statements to your privacy library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/update-privacy-mgmt-content.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 2
keywords: [activate risk statements, privacy risk statements, risk statement category, privacy content]
breadcrumb: [Privacy content accelerator, Privacy Management, Governance, Risk, and Compliance]
---

# Update content in the privacy library

Update an installed authority document or risk statement version to add newer citations, control objectives, and risk statements to your privacy library.

## Disclaimer

**Important:**

The ServiceNow Risk products help customers address regulatory requirements under various jurisdictions. However, we do not guarantee compliance and customers are ultimately responsible for their own compliance with applicable regulations.

ServiceNow aims to provide software updates for new or updated major regulations and requirements within twelve to eighteen months of the regulation's publication. For regulations for which ServiceNow provides a level of support in the base system, ServiceNow aims to provide software updates for minor regulatory changes within 12 months and for major regulatory changes within up to 18 months depending on scope and impact. We differentiate between typical regulatory content updates, which do not require software updates or enhancements, and regulatory updates, which do require software updates or enhancements. Content updates are generally delivered on a shorter cadence than if software update or enhancement is required for the regulatory update or change.

## Before you begin

Role required: sn\_privacy.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace**.

2.  Select the Privacy content icon \[Omitted image "unified-content-mgmt-icon.png"\].

3.  Depending on the scope for the content you want to update, select either the **Privacy Frameworks** tab or the **Risk Statements** tab.

4.  Select **Active**.

5.  In the authority document or risk statement entry, select **Update**.

6.  In the Disclaimer message, select **Agree**.

    The installation wizard shows records associated with the selected authority document or risk statement version. Records not yet added to your library have the installation state Ready. Records already installed from this version have the installation state Installed.

    **Note:** Control objectives and risk statements are AI-generated. Although AI models are exposed to major privacy regulations, they aren't trained on the risk and compliance methodologies that your teams might use to derive a complete, consistent set of control objectives and risk statements from a regulation. Review each record for accuracy, scope, and fit with your internal taxonomy before you map it to processing activities or assessment questions.

7.  Review the records available to install.

    -   The Authority Document page lists the following document types:
        -   Citations associated with the selected authority document. To view the source regulatory text related to the citations, add **Supplemental guidance** as a column using the **Personalize fields** option of the **More Actions** menu.

            **Note:** Citation descriptions are AI-generated. The source regulatory text in supplemental guidance is formatted using AI. Review all content for accuracy.

        -   Control objectives mapped to the selected citations.
    -   The Risk Statement page lists the privacy risk statements available with the selection version.
8.  Select the records to install.

9.  Select **Next**.

10. Review the number of selected records and select **Submit**.

    The status changes to Updating while installation is in progress.

11. Refresh the page to verify that installation is complete.


## Result

The installed records are available in the List view of the Privacy Workspace.

