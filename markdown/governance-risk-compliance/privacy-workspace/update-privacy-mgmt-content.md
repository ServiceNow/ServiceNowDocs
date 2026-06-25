---
title: Update privacy content
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

# Update privacy content

Update an installed authority document or risk statement version to add newer citations, control objectives, and risk statements to your privacy library.

## Disclaimer

**Important:**

The ServiceNow Risk products help customers address regulatory requirements under various jurisdictions. However, we do not guarantee compliance and customers are ultimately responsible for their own compliance with applicable regulations.

ServiceNow aims to provide software updates for new or updated major regulations and requirements within twelve to eighteen months of the regulation's publication. For regulations for which ServiceNow provides a level of support in the base system, ServiceNow aims to provide software updates for minor regulatory changes within 12 months and for major regulatory changes within up to 18 months depending on scope and impact. We differentiate between typical regulatory content updates, which do not require software updates or enhancements, and regulatory updates, which do require software updates or enhancements. Content updates are generally delivered on a shorter cadence than if software update or enhancement is required for the regulatory update or change.

## Before you begin

Role required: sn\_privacy.manager

## Procedure

1.  In the Privacy Workspace, select the Privacy content icon.

2.  Select the **Privacy Frameworks** tab or the **Risk Statements** tab depending on the content you want to update.

3.  On the **Active** sub-tab, locate the activated authority document or risk statement version update, and select **Update**.

4.  Review the disclaimer, and select **Agree**.

    The installation wizard opens, showing records associated with the selected authority document or risk statement version.

    **Important:** Control objectives and risk statements are AI-generated. Although AI models are exposed to major privacy regulations, they aren't trained on the risk and compliance methodologies that your teams may use to derive a complete, consistent set of control objectives and risk statements from a regulation. Review each record for accuracy, scope, and fit with your internal taxonomy before you map it to processing activities or assessment questions.

5.  Select the records to install, and select **Next**.

    Records not yet added to your library appear as **Ready**. Records already installed from this version appear as **Installed**.

<table id="table_cbp_2fn_kjc"><thead><tr><th>

Record type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Citation**

</td><td>

Citations associated with the selected authority document. To view the source regulatory text related to the citations, add **Supplemental guidance** as a column using the **Personalize fields** option.**Note:** Citation descriptions are AI-generated. Supplemental guidance is formatted by AI. Review all content for accuracy.

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

The installed records are available in the List view of the Privacy Workspace.

**Related topics**  


[Privacy content accelerator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/privacy-content-accelerator.md)

[Activate privacy content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/update-privacy-content.md)

