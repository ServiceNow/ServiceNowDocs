---
title: Review and submit values predicted by Document Intelligence
description: Agents can extract, validate, and update the key values from valid attachments in the case using the Document Intelligence interface.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use Task Intelligence for Customer Service, Automate and optimize, Using Customer Service Management, Customer Service Management]
---

# Review and submit values predicted by Document Intelligence

Agents can extract, validate, and update the key values from valid attachments in the case using the Document Intelligence interface.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, sn\_csm\_ml\_task.ti\_admin, admin

## About this task

The task definition includes an extraction mode that determines how the system handles the extracted values: straight through processing, autofill, or recommendations. Regardless of the extraction mode, agents can view valid attachments in Document Intelligence interface and confirm or correct the values.

## Procedure

1.  Open a case in CSM Configurable Workspace.

2.  Click **Review in DocIntel** to open the [Document Intelligence workspace](https://www.servicenow.com/docs/access?context=doc-intel-workspace&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) in a separate tab and view the attachments and extracted values.

    In this tab:

    -   Attachments appear in the list of attachments on the left side of the tab.
    -   An image of the selected attachment appears in the center of the tab.
    -   Extracted fields appear in a list on the right side of the tab.
3.  Select an attachment to view an image of that attachment in the center of the tab.

4.  Review the extracted fields and confirm or correct the values.

    1.  If a value for a field is correct, click in the field and press Enter to confirm.

        Confirmed values have a blue check mark.

    2.  If a value for a field is not correct, click in the field, select the correct value from the dropdown list, and press Enter.

    3.  If a value for a field is not correct and the correct value does not appear in the dropdown list, select the more actions button next to the field and select **Missing in this document**.

5.  Click **Submit** to add these values to fields on the Case form.


