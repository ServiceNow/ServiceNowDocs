---
title: Review AI-extracted metadata and contract reminder date in the Hardware Asset Workspace
description: Use the contract playbook to review and update the AI-extracted metadata and contract reminder date.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/review-ai-extracted-metadata-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 3
breadcrumb: [Manage contract repository agentic workflow, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Review AI-extracted metadata and contract reminder date in the Hardware Asset Workspace

Use the contract playbook to review and update the AI-extracted metadata and contract reminder date.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller, ham\_admin/ham\_user, sn\_cm\_gen\_ai.ai\_contract\_config, and now\_assist\_panel\_user

## About this task

The Manage contract repository agentic workflow uses AI agents to extract key metadata from signed contracts and calculate contract reminder date. The metadata is extracted based on the applicable use case in the Contract metadata extraction skill. After the extraction process is complete, a message appears on the contract record and an email notification is sent with a link to review the extracted metadata. Once you have reviewed and submitted the extracted metadata, the contract reminder date is calculated. The reminder date is calculated based on the contract end date, auto-renewal clause, and notice period for contract renewal or termination.

To receive notifications when AI agents complete metadata extraction, verify that notifications are enabled by the administrator. For more information, see [Enable notifications for AI extracted metadata and obligations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-na-me-agentic-ntf.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Contract management**.

2.  Select the **All contracts** tab.

3.  Select a contract record for which you want to review the extracted metadata.

4.  Select the **Playbook** tab.

5.  In the playbook, under the AI extracted metadata section, select **Extracted metadata**.

    The playbook displays the Extracted metadata section with a review overview showing the number of fields yet to review and reviewed.

6.  Select **Review metadata**.

    The **Review Metadata** page opens, displaying the signed contract document on the left and the **Extracted data** panel on the right. Fields that could not be extracted are tagged **Missing in the document**.

7.  Review each field in the Extracted data panel and mark it as reviewed using one of the following methods:

    -   To update a field value:
        1.  Select the Edit icon \[Omitted image "now-assist-sam-contract-metadata-extraction-edit-icon.png"\] Alt text: next to the field to open it for editing.
        2.  Enter the correct value in the field.

            If the value is not available in the contract document, select the **Answer is missing in the document** check box.

        3.  Select **Save**.

            A tick appears on the button, indicating the field is reviewed.

    -   To accept the extracted value without editing:

        Select the **Click to mark as reviewed** button next to the field.

        A tick appears on the button, indicating the field is reviewed. Use the **To review** tab to track fields that still require review. The count updates as you mark each field.

8.  After reviewing all fields, select **Submit**.

    The **Confirm field predictions** dialog box appears, prompting you to confirm that you have reviewed all fields for accuracy before submitting.

9.  In the dialog box, select one of the following options:

    -   To go back and review remaining fields, select **Review**.
    -   To confirm and submit the reviewed metadata, select **Confirm and Submit**.
    -   The extracted and reviewed metadata is added to the mapped fields in the hardware contract.
    -   In the Playbook tab, the status of the Extracted metadata section updates to Complete.
10. Select the **Playbook** tab.

11. Under Review contract reminders, select **Contract reminder date**.

12. Review the **Reminder date** field.

    -   If the signed contract contains the contract end date, auto-renewal clause, and notice period, the AI agent calculates and populates the reminder date. To understand how the date was calculated, select **Show AI reasoning** to view the breakdown. Modify the date if needed.
    -   If any of these values are missing from the signed contract, the reminder date can't be calculated automatically. Enter the reminder date manually in the **Reminder date** field.
13. Select **Mark as complete**.

    The Contract reminder recipients page opens, displaying the list of users who are already configured as recipients for the contract reminder.

14. Configure the recipient list.

    -   To add a recipient, select **Add**. In the **Add recipients** dialog box, select a user and then select **Add**.

    -   To remove a recipient, select the check box next to the user name and select **Remove**.

        **Note:** You must add at least one user as a recipient.

15. Select **Mark as complete**.

    The contract reminder date is saved, and the configured recipient receives a notification on the specified date to remind them of upcoming contract renewal or termination actions.


**Parent Topic:**[Manage contract repository agentic workflow in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/manage-contract-repo-agent-flow-ham.md)

