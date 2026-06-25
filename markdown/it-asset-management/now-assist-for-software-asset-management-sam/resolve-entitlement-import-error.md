---
title: Resolve entitlement import errors by using Now Assist for SAM
description: Reduce manual effort when reviewing entitlement import errors in the Software Asset Workspace using Now Assist for SAM AI skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/now-assist-for-software-asset-management-sam/resolve-entitlement-import-error.html
release: australia
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 3
keywords: [Software Normalization skill, Product Match Reviewer skill, resolve entitlement import errors,]
breadcrumb: [Use generative AI skills, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Resolve entitlement import errors by using Now Assist for SAM

Reduce manual effort when reviewing entitlement import errors in the Software Asset Workspace using Now Assist for SAM AI skills.

## Before you begin

The following plugins and store applications must be installed from [ServiceNow Store](https://store.servicenow.com/store) to use the AI skills:

-   Now Assist for Software Asset Management \(SAM\) \(sn-now-assist-sam\)
-   Software Asset Management AI Advance \(sn-ai-sam-advance\)
-   Content library portal \(sn-itam-contlookup\)

Role required: sam\_user or sam\_admin

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

When you import software entitlements using the [Import bulk entitlements in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/import-entitlements-workspace.md) feature, some rows may contain publisher or product data that standard content matching can't resolve. Unresolved publisher or product data prevents the entitlement import from completing successfully.

To resolve this issue, Now Assist for SAM provides the following AI-powered skills that normalize publisher and product values:

-   Software normalization
-   Product match reviewer

After the file import completes, if any publisher or product names in the import file are misspelled, incomplete, or unrecognized, the skills run automatically to identify the correct values and provide corrections.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Software Asset Workspace**.

2.  Select **Create entitlement**.

3.  In the Create new entitlement dialog box, select **Import multiple entitlements from an Excel file**.

4.  Select **Next**.

5.  Upload a Microsoft Excel file.

    For more information about importing multiple entitlements, see [Import bulk entitlements in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/import-entitlements-workspace.md).

    **Note:** The error resolution for the **Product** and **Publisher** fields applies only when the **Import Type** field value is selected as **Standard Import document**.

    After the file import completes, the following two skills run in sequence to provide correction suggestions for unresolved publisher or product data.

<table id="table_pqq_vnc_mjc"><thead><tr><th>

Skill

</th><th>

Details

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Software normalization

</td><td>

Identifies canonical publisher and product names from discovered software data in the Content Library. This skill uses LLM \(large language model\)-driven knowledge to standardize raw, incomplete, or unrecognized publisher and product values submitted during entitlement import.

</td><td>

Canonical publisher and product names based on discovered software value in the Content Library are displayed in the **Product** and **Publisher** fields of the imported entitlement record.

</td></tr><tr><td>

Product match reviewer

</td><td>

The Product match reviewer skill runs after the Software normalization skill completes successfully. **Note:** It runs only when the Software normalization skill is unable to find the correct product match from the Content Library.

The Product match reviewer skill performs an AI-powered search and selects the correct product match. If no reliable match is found, the skill returns an empty result.

</td><td>

-   The confirmed product match from the AI-based content search result is displayed for the entitlement record **Product** field.
-   If no reliable match is found for the **Product** field, the skill returns an empty result.


</td></tr></tbody>
</table>6.  Select the **Errors** tab.

    The **Errors** tab displays all entitlement import error records that require human attention. These records fall into the following categories:

    -   Records where the AI skills have provided a suggested correction that requires your review. In the Error status column, the sparkle icon \[Omitted image "ai-sparkle-icon.png"\] Alt text: indicates that the record contains an AI suggestion.
    -   Records where the AI skills were unable to resolve the import error and provide a correction. Review these records and manually update the publisher or product values to resolve the error.
7.  Select the number link to open the import error record.

    If the import error record contains an AI-suggested value, an AI sparkle icon \[Omitted image "field-ai-sparkel-icon.png"\] Alt text: is displayed on the field, showing both the AI-corrected value and the original value from the import file.

8.  Review the AI-corrected value for each field.

9.  Select **Import** to save and import the reviewed record.


## Result

-   After the import is complete, an entitlement record is created and displayed on the **Entitlements** tab.
-   The import error record is removed from the **Errors** tab.
-   The Entitlement creation widget in the AI activity section of the Software Asset overview page is updated. The widget displays the number of entitlement import errors requiring review. Select the link to view the Entitlement Import Error list.

    \[Omitted image "import-errors-require-review.png"\] Alt text: Import errors to review


**Parent Topic:**[Using generative AI skills in Now Assist for SAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/using-now-assist-sam.md)

**Related topics**  


[Import bulk entitlements in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/import-entitlements-workspace.md)

