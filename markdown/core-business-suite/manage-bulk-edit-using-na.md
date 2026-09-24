---
title: Bulk edit
description: Edit records in bulk for Core Business Suite business units through the Now Assist conversational experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/core-business-suite/manage-bulk-edit-using-na.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for Core Business Suite \(CBS\), Configure Core Business Suite using Otto, Configure, Core Business Suite]
---

# Bulk edit

Edit records in bulk for Core Business Suite business units through the Now Assist conversational experience.

## Before you begin

Ensure that Now Assist in Virtual Agent is installed. For more information, see .

Role required: admin, sn\_cbs.admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  On the Core Business Suite card, select **View product overview**.

3.  In the Configuration insights section, select **Configure**.

    The Configure Core Business Suite page opens in the Configuration Console.

4.  Select **Workplace locations** under Workplace Services.

5.  Select **Configure with Now Assist**.

    Now Assist opens the conversational panel, detects the current page context, and invokes the CBS Bulk Upload Agent.

    **Note:** The CBS Bulk Upload Agent supports Workplace Locations for bulk edit.

6.  Select **Bulk edit** or enter a natural‑language prompt.

    Example prompts:

    -   `Bulk edit workplace locations`.
    -   `Upload edit workplace locations using a template`.
    -   `Bulk edit records for workplace locations`.
    Now Assist processes your request, identifies the relevant template based on the selection, and provides it for download.

7.  Download the template.

    The template downloads as a .csv file.

8.  Open the file in excel \(.xlsx or .xls\), make the required changes, and save it.

9.  Upload the updated template when prompted.

    Now Assist analyzes the uploaded file and validates the data.

10. Review the validation results.

11. If errors are reported, open the provided import link and correct the issues.

12. If validation is successful, select **Process all rows**.

    Now Assist processes the updates and provides access to the import set.

13. Select **Import Set** to review the updated records.

14. Confirm that the changes are reflected.

15. Select **Mark as configured** when prompted.

    Now Assist confirms the bulk edit is completed with a success message.

16. Refresh the CBS Configuration Console to verify that the records were updated successfully.


**Parent Topic:**[ServiceNow Otto for Core Business Suite \(CBS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/now-assist-cbs.md)

