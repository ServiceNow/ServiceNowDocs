---
title: Review AI-extracted metadata and contract reminder date
description: Use the contract playbook to review and update the AI-extracted metadata and contract reminder date.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-08-10"
reading_time_minutes: 3
keywords: [Manage contract repository, Agentic workflow in Contract Management Pro, Review AI extracted information, Playbook in Contract Management Pro, Review AI results in Contract Management Pro]
breadcrumb: [Review AI results, Use agentic workflows, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Review AI-extracted metadata and contract reminder date

Use the contract playbook to review and update the AI-extracted metadata and contract reminder date.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

## About this task

The Manage contract repository agentic workflow uses AI agents to extract key metadata from signed contracts and calculate contract reminder date. The metadata is extracted based on the applicable use case in the Contract metadata extraction skill. After the extraction process is complete, a message appears on the contract record and an email notification is sent with a link to review the extracted metadata. Once you have reviewed and submitted the extracted metadata, the contract reminder date is calculated based on the contract end date, auto-renewal clause, and notice period for contract renewal or termination.

To receive notifications when AI agents complete metadata extraction, ensure that notifications are enabled by the system administrator. For more information, see [Enable notifications for AI extracted metadata and obligations](cmpro-na-me-agentic-ntf.md).

## Procedure

1.  Open a contract repository record where you want to review the extract information.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d396638e90">

Method

</th><th align="left" id="d396638e93">

Steps

</th></tr></thead><tbody><tr><td id="d396638e99">

**Contract Workspace**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon \(![List icon.](../../legal-request-management/image/lsd-lcc-list-icon.png)\).
3.  Select **Executed contracts**.
4.  Select **All**.
5.  Select the contract repository record.


</td></tr><tr><td id="d396638e147">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open a contract request that is in the Closed complete or Contract signed state.
3.  Select the **Contract repository** tab.
4.  Select the contract repository record.


</td></tr><tr><td id="d396638e174">

**Email notification**

</td><td>

Select **Open playbook** in the email notification that you receive after the metadata extraction is complete.

</td></tr></tbody>
</table>2.  Select the **Playbook** tab.

    The playbook opens displaying a step-by-step interface to review the extracted metadata.

    ![Contract playbook with step-by-step interface to review AI extracted results.](../image/cmpro-na-ai-playbook.png "Contract playbook")

3.  Select **Review metadata**.

    The Document Intelligence workspace opens on a different tab displaying the extracted information.

    ![Document Intelligence displaying extracted metadata for a contract.](../image/cmpro-na-di-me.png "Document Intelligence workspace")

4.  Review and update the extracted metadata.

    For more information, see [Work with extracted metadata](cncore-review-metatdata.md).

5.  Select **Submit**.

    The reviewed metadata is added to the contract repository fields and the **Extracted results** tab opens on the contract repository record. For more information, see [Metadata extraction results](../reference/cncore-metadata-ext-results.md).

6.  Select the **Playbook** tab.

    The playbook opens on the **Review contract reminders** step where you can review the AI calculated reminder date.

    ![Contract playbook displaying the Contract reminder date page.](../image/cmpro-na-me-completed.png "Contract reminder date")

7.  In the **Reminder date** field, modify the date, if necessary.

8.  Select **Mark as complete**.

    The Contract reminder recipients page opens displaying the list of users who are already configured as recipients for the contract reminder.

    ![Contract playbook displaying the Contract reminder recipients page.](../image/cmpro-na-reminder-rec.png "Contract reminder recipients")

9.  Configure the recipient list.

    -   To add a user, select **Add** and then enter the user name in the Add recipients window.
    -   To remove a user, select the check box corresponding to the user name and then select remove.

        **Note:** At least one user is required in the recipient list.

10. Select **Mark as complete**.


## Result

The contract reminder date is saved, and configured users will receive a notification on the specified date to remind them of upcoming contract renewal or termination actions.

**Related topics**  


[Manage contract repository agentic workflow](../concept/cmpro-na-reminder-agentic-wf.md)

[Reviewing AI-extracted results in the playbook](../concept/cmpro-na-review-ai.md)

[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

