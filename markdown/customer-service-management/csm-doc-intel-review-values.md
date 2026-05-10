---
title: Review and submit values predicted by Document Intelligence
description: Agents can extract, validate, and update the key values from valid attachments in the case using the Document Intelligence interface.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Task Intelligence, Automate and optimize, Use, Customer Service Management]
---

# Review and submit values predicted by Document Intelligence

Agents can extract, validate, and update the key values from valid attachments in the case using the Document Intelligence interface.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, sn\_csm\_ml\_task.ti\_admin

## About this task

The task definition includes an extraction mode that determines how the system handles the extracted values: straight through processing, auto-fill, or recommendations. Regardless of the extraction mode, agents can view valid attachments in the Document Intelligence interface and confirm or correct the values.

## Procedure

1.  Open a case in CSM Configurable Workspace.

2.  Select **Review in DocIntel** to open the [Document Intelligence workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/doc-intel-workspace.md) in a separate tab and view the attachments and extracted values.

    In this tab:

    -   Attachments appear in the list of attachments on the left side of the tab.
    -   An image of the selected attachment appears in the center of the tab.
    -   Extracted fields appear in a list on the right side of the tab.
3.  Select an attachment to view an image of that attachment in the center of the tab.

4.  Review the extracted fields and confirm or correct the values.

    1.  If a value for a field is correct, select in the field and press Enter to confirm.

        Confirmed values have a blue check mark.

    2.  If a value for a field isn’t correct, select in the field, select the correct value from the drop-down list, and press Enter.

    3.  If a value for a field isn’t correct and the correct value doesn’t appear in the drop-down list, select the more actions button next to the field and select **Missing in this document**.

5.  Select **Submit** to add these values to the fields on the Case form.


