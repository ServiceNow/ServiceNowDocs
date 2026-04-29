---
title: Bulk upload
description: Upload records in bulk for Core Business Suite business units through the Now Assist conversational experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 2
breadcrumb: [Now Assist for Core Business Suite, Configure Core Business Suite using Now Assist, Configure, Core Business Suite]
---

# Bulk upload

Upload records in bulk for Core Business Suite business units through the Now Assist conversational experience.

## Before you begin

Ensure that the following are activated:

-   AI search \([Activate AI Search](activate-ai-search.md)\)
-   Now Assist panel \([Activate Now Assist panel](enable-now-assist-panel.md)\)

Role required: admin, sn\_cbs.admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  On the Core Business Suite Foundation card, select **View product overview**.

3.  In the Configuration insights section, select **Configure**.

    The Configure Core Business Suite page opens in the Configuration Console.

4.  From the navigation menu, select the section to which you want to bulk upload the details:

    -   **Workplace locations** under Workplace Services
    -   **Supplier management** or **Supplier contacts** under Source-to-Pay
5.  Select **Configure with Now Assist**.

    Now Assist opens the conversational panel, detects the current page context, and invokes the CBS Bulk Upload agent.

    **Note:** Now Assist guides you through follow‑up questions and requests confirmation before completing the bulk upload.

6.  Select **Bulk upload** or enter a natural‑language prompt:

    Example prompts:

    -   `Bulk upload workplace locations`.
    -   `Upload multiple workplace locations using a template`.
    -   `Bulk upload records for workplace locations`.
    Now Assist processes your request, identifies the relevant template based on the selection, and provides it for download.

7.  Download the bulk upload template.

8.  Enter the required data in the template and save the file.

9.  Upload the updated template when prompted.

    Now Assist analyzes the uploaded file and validates the data.

10. Review the validation results.

11. If errors are reported, review and update the template file as needed, and re-upload it.

12. If validation is successful, select **Process all rows**.

    Now Assist processes the import and provides access to the import set.

13. Select **Import Set** to review the imported records.

14. Confirm that the updates are reflected.

15. Select **Mark as configured** when prompted.

    Now Assist confirms that the bulk upload is complete with a success message.

16. Refresh the Core Business Suite Configuration Console to verify that the records are created successfully.


**Parent Topic:**[Now Assist for Core Business Suite](../concept/now-assist-cbs.md)

