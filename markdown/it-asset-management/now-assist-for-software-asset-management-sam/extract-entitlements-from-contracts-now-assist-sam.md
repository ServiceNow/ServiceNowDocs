---
title: Extract entitlements from software contracts using ServiceNow Otto for Software Asset Management \(SAM\)
description: Reduce manual effort by using generative AI to create entitlements by extracting information from software contracts.Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to extract contract entitlement data. A trigger initiates an action, such as when the system generates an entitlement from a contract.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/now-assist-for-software-asset-management-sam/extract-entitlements-from-contracts-now-assist-sam.html
release: zurich
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [Contract entitlement data extraction skill]
breadcrumb: [Use generative AI skills, ServiceNow Otto for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Extract entitlements from software contracts using ServiceNow Otto for Software Asset Management \(SAM\)

Reduce manual effort by using generative AI to create entitlements by extracting information from software contracts.

## Before you begin

Before you use the Contract entitlement data extraction skill, install the following plugin and the store apps that match your platform release version.

<table id="table_contract_ent_plugins"><thead><tr><th>

Platform release

</th><th>

Plugin

</th><th>

Store apps

</th></tr></thead><tbody><tr><td>

Zurich Patch 8 or later patches

</td><td>

Software Asset Management Professional \[com.snc.samp\]

</td><td>

-   ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 7.0.0 or later
-   Software Asset Workspace \[sn\_sam\_workspace\] - 10.0.8 or later

</td></tr></tbody>
</table>Role required: sam\_user

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

**Note:** The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

Starting with the Australia Patch 4 release, Azure OpenAI is the default model provider for the Contract entitlement data extraction generative AI skill.

With the Contract entitlement data extraction skill being activated by default, you can upload software contracts in the Software Asset Workspace to automatically generate entitlements.

You can extract data related to entitlements from an existing or a new contract and only from contracts where the contract model is a software license.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Contracts** &gt; **Software contracts**.

2.  Open an existing software contract that is in an active state and where the contract model is a software license, and select **New**.

    **Note:** Only the sam\_admin role can create a contract.

3.  Select **Import contract document**.

4.  Select a publisher from the **Publisher** list.

5.  Select **Add file** to attach a PDF or image of a contract.

    **Note:** The file format should be PDF, JPG, JPEG, or PNG and the file size per attachment must not exceed 4 MB. The maximum page count is 10 pages for images and 25 pages for PDFs.

6.  Select **Upload**.

7.  Select **Next** to go to the Extract entitlements page.

    A message appears informing you that the extracting process is in progress.

8.  Select **Next** after the extraction process is complete.

    \[Omitted image "extractentitlements.png"\] Alt text: Extract entitlements page

9.  Select the expand arrow next to **Tables**.

10. Select **Entitlements**.

    Correct inaccurate predictions or add values that DocIntel missed on this page. Use the **Draw mode** in DocIntel to move or reorder the columns, or make edits directly in the table.

11. Select **Submit** after you review all the predictions on the page.

    The Confirm field predictions message box opens.

12. Select **Confirm and submit**.

    The status changes from **Review** to **Done**. Every time you make changes and select **Submit**, the data extracted from DocIntel changes.

13. Select **Next** to lock in the data and go to the Review entitlements page.

    \[Omitted image "reviewentitlements.png"\] Alt text: Review entitlements page

    The Review entitlements page opens with the entitlement import error records. For each entitlement extracted from the contract document, an entitlement import record is created. The page also shows the PDF or images you uploaded.

    If you selected a publisher in step 4, the best matches for that publisher appear.

    You can perform inline editing in the list view for all records that are in the **Needs review** status.

14. Select one of the following options:

    -   **Mark as reviewed** for records that have no errors. Additionally, if a record has errors that you don't want to ignore, open that record, rectify the errors, and then select **Mark as reviewed**. If you select **Mark as reviewed**, the status changes to **Reviewed**.
    -   **Ignore** to ignore the errors for a record. After you ignore a record, the record becomes read only and the status changes to **Ignored**. You can select **Edit** on the record form to change the status of the record to **Needs review** or **Reviewed**. **Edit** appears only for records that are in the **Ignored** or **Reviewed** status.

        **Warning:** If a record is marked as **Ignored**, an entitlement doesn't get created.

15. Select **Submit** after you review and correct the errors in all the records.

    The entitlements are successfully created.


**Parent Topic:**[Using generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/now-assist-for-software-asset-management-sam/using-now-assist-sam.md)

## Contract entitlement data extraction skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to extract contract entitlement data. A trigger initiates an action, such as when the system generates an entitlement from a contract.

### Triggers for contract entitlement data extraction skill

The following table lists the triggers for the contract entitlement data extraction skill.

|Trigger|Description|
|-------|-----------|
|User-triggered|An entitlement is automatically generated from a contract when the user manually triggers the skill by selecting **Import contract document** in the software contract page.|

### Input for the Contract entitlement data extraction skill

The following table lists the inputs for the Contract entitlement data extraction skill.

|Input|Description|
|-----|-----------|
|The contract document|The contract document that the user uploads that is used for extracting the entitlement information.|

