---
title: Work with extracted metadata
description: Review the metadata extracted from a contract and add it to the contract repository.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Metadata Extraction]
breadcrumb: [Contract metadata extraction, Use generative AI skills, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Work with extracted metadata

Review the metadata extracted from a contract and add it to the contract repository.

## About this task

After the metadata extraction process is completed, you can review and modify the values of the extracted fields in the Document Intelligence workspace before submitting it to update mapped fields in the contract repository.

## Before you begin

The metadata extraction process must be completed.

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

## Procedure

1.  Open a contract repository record where you want to review extracted information.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d594847e69">

Method

</th><th align="left" id="d594847e72">

Steps

</th></tr></thead><tbody><tr><td id="d594847e78">

**Contract Workspace**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon \(![List icon.](../../legal-request-management/image/lsd-lcc-list-icon.png)\).
3.  Select **Executed contracts**.
4.  Select **All**.
5.  Select the contract repository record.


</td></tr><tr><td id="d594847e126">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open a contract request that is in the Closed complete or Contract signed state.
3.  Select the **Contract repository** tab.
4.  Select the contract repository record.


</td></tr></tbody>
</table>2.  Select **Review extracted metadata**.

    The Document Intelligence workspace opens on a different tab displaying the extracted information.

    ![Document intelligence workspace to update the extracted metadata.](../image/cmpro-na-di-me.png "Document Intelligence workspace")

3.  Review the extracted information.

4.  Enter the value in the extracted fields that are empty.

5.  Update the extracted information for the fields with incorrect information.

    1.  Select the field.

    2.  For text fields, enter the correct value.

        The value is automatically saved.

    3.  For reference fields, select **Edit**, search for the correct value in the **Matched to** field, and then select **Save**.

    4.  For date fields, select **Edit**, select the date, and then select **Save**.

    5.  Enter a new value or select a value from the list of available options.

    6.  Select **Save**.

6.  Select **Submit**.


## Result

The information is submitted to be added to the mapped fields in the contract repository.

When the extraction process is completed, you can view the status of the extracted fields in the **Extraction results** related list in the contract repository record. For more information on the status of the fields, see [Metadata extraction results](../reference/cncore-metadata-ext-results.md).

**Parent Topic:**[Contract metadata extraction using Now Assist in Contract Management](../concept/cncore-metadata-extract-land.md)

