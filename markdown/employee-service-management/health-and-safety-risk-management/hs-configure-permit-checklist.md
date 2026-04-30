---
title: Configure a permit checklist
description: Create a permit checklist and link it to the permit type of a permit-to-work request.
locale: en-US
release: zurich
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure permit-to-work, Configure, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Configure a permit checklist

Create a permit checklist and link it to the permit type of a permit-to-work request.

## Before you begin

Role required: admin and sn\_hs\_rm.permit\_coordinator

## Procedure

1.  Navigate to **All** &gt; **Service catalog** &gt; **Catalog definitions** &gt; **Record producers**.

2.  Search for and select **Permit checklist** record.

3.  Select the Variable sets related list and select **New**.

4.  Create a variable set with grouped variables by selecting **single row variable set** .

5.  On the Variable set new record form, fill in the fields.

    For a description of the field values, see [Variable set new record form](../reference/hs-variable-set-new-record-form.md).

6.  Select **Submit**.

    The new variable set is created.

7.  Open the new variable set and on the form fill in the fields.

    For more information on the field description, see [Variable new record form](../reference/hs-variable-new-record.md).

8.  Select **Submit**.

9.  Create a checklist type.

    1.  Navigate to **All** &gt; **System definition** &gt; **Tables**.

    2.  Search in the **Label** column for `Permit checklist` and select the table.

    3.  Select **Checklist type** in the **Column label** related list.

    4.  If the request form displays a message about the application scope, select **here** to be able to edit the record.

    5.  Select the Choices related list and select **New**.

    6.  On the form, fill in the fields.

        For more information on the field description, see [Choice new record form](../reference/hs-choice-new-record-form.md).

    7.  Select **Submit**.

10. Associate the checklist to a permit type.

    1.  Navigate to **All** &gt; **System definition** &gt; **Decision tables** and select **Permit checklist configuration**.

    2.  Select **Draft** and select **Add new decision row**.

    3.  Select the empty cell in the **permit type** column and select the permit type in the **Choice input** field in the **permit type**, then select **OK**.

    4.  Select the empty cell in the **checklist type** column and select the checklist type in the **Choice input** field, then select **OK**.

    5.  Select the empty cell in the **variable set** column and select the variable set in the **Choice input** field, then select **OK**.

    6.  Select **Save**.

    7.  Select **Publish** and then select **Publish** in the modal dialogue.

11. Create a flow for the checklist type.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    2.  Select the **Flows** tab and then select the **Create permit checklist when permit created** flow.

    3.  Select **Duplicate action** for the existing **Create permit checklist record** action.

        The flows are built using ServiceNow Workflow Studio, so make sure you’re familiar with the [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer-home-landing-page&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) basics.

        For information on how to create or modify flows, see [Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

    4.  Select the new checklist type in the **Checklist type** field.

    5.  Select **Save** and then select **Activate**.


## Result

The checklist is configured and displayed in the checklist tab of the permit-to-work request form when the permit type is selected.

**Parent Topic:**[Configure permit-to-work](../concept/hs-configure-permit-to-work.md)

