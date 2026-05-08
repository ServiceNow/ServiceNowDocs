---
title: Review AI-extracted metadata and contract reminder date in the Software Asset Workspace
description: Use the contract playbook to review and update the AI-extracted metadata and contract reminder date.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use manage contract repository agentic workflow, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Review AI-extracted metadata and contract reminder date in the Software Asset Workspace

Use the contract playbook to review and update the AI-extracted metadata and contract reminder date.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller, sam\_admin/sam\_user, sn\_cm\_gen\_ai.ai\_contract\_config, and now\_assist\_panel\_user

## About this task

The Manage contract repository agentic workflow uses AI agents to extract key metadata from signed contracts and calculate contract reminder date. The metadata is extracted based on the applicable use case in the Contract metadata extraction skill. After the extraction process is complete, a message appears on the contract record and an email notification is sent with a link to review the extracted metadata. Once you have reviewed and submitted the extracted metadata, the contract reminder date is calculated. The reminder date is calculated based on the contract end date, auto-renewal clause, and notice period for contract renewal or termination.

To receive notifications when AI agents complete metadata extraction, verify that notifications are enabled by the administrator. For more information, see Enable notifications for AI extracted metadata and obligations.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Contracts** &gt; **Software contracts**.

2.  Open a Contract record for which you want to review the extracted metadata.

3.  Select the **Playbook** tab.

4.  In the Extracted metadata section, select **Review metadata**.

    The uploaded signed contract document and extracted fields are displayed on the **Record** tab. In the Document Q&amp;A section, review all extracted information to verify that it’s accurate.

5.  Enter the value in the extracted fields that are empty.

6.  Update the extracted information for the fields with incorrect information.

    1.  Next to the appropriate field, select the Edit icon ![](../image/now-assist-sam-contract-metadata-extraction-edit-icon.png).

    2.  Make your updates as needed.

    3.  Save your changes.

7.  Select **Submit** and select one of these options in the confirmation message:

    -   To mark your confirmation and proceed with contract metadata extraction, select **Confirm and Submit**.
    -   To verify the extracted field values, select **Review**, and then select **Submit** to proceed with contract metadata extraction.
    After you confirm and submit the reviewed fields, a confirmation message appears for successful submission of the reviewed contract metadata. In the **Playbook** tab, in the Extracted metadata section, the status for metadata extraction is displayed as Complete. On the **Details** tab, the extracted field value from the signed contract document is populated.

8.  Select the **Details** tab and review the field values extracted and populated on the contract form.

9.  Select the **Playbook** tab.

    If the contract end date is available, the playbook opens on the **Review contract reminders** step, where you can review the AI calculated reminder date.

10. In the **Reminder date** field, modify the date if needed.

11. Select **Mark as complete**.

    The Contract reminder recipients page opens, displaying the list of users who are already configured as recipients for the contract reminder.

12. Configure the recipient list.

    -   To add a user, select **Add** and then enter the user name in the Add recipients window.
    -   To remove a user, select the check box corresponding to the user name and then select remove.

        **Note:** You must add at least one user as a recipient.

13. Select **Mark as complete**.


## Result

-   The extracted and reviewed metadata is added to the mapped fields in the software contract.
-   The contract reminder date is saved, and the configured recipient receives a notification on the specified date to remind them of upcoming contract renewal or termination actions.

**Parent Topic:**[Use manage contract repository agentic workflow in the Software Asset Workspace](../concept/manage-contract-repository-workflow.md)

