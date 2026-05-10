---
title: Create a UI macro for a formatter
description: Create a UI macro to define the content that the formatter displays.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Formatters, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a UI macro for a formatter

Create a UI macro to define the content that the formatter displays.

## Before you begin

This functionality requires knowledge of Jelly script.

Role required: ui\_macro\_admin

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Macros**.

2.  Click **New**.

3.  Complete the form.

4.  In the **XML** script field, enter Jelly script to define the content to be displayed by the formatter.

    **Note:** The UI Macro for the formatter represents a row in the UI. It must begin and end with `<TR></TR>` tags.

    ![Formatter UI macro](../image/FormatterUIMacro.png)

    This Jelly script is reproduced below in plain text that you can copy into the Macro form as a basis for your macro script.

    ```
    <?xml version="1.0" encoding="utf-8" ?>
    <j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
    <button style="background: #C0C0C0; border-color: darkgrey; color: #3f464f; height:30; width:70"
    onclick="saveCustomAttachment();return false">
    <b>Attach file</b>
    </button>
    <script>
    function saveCustomAttachment(){
    var tableName = g_form.getTableName();
    var sys_id_input = gel('sysparm_item_guid') ? gel('sysparm_item_guid').value : g_form.getUniqueValue();
    if(tableName === "ni"){
    saveCatAttachment(sys_id_input, 'sc_cart_item');
    }else{
    saveAttachment('sc_req_item', sys_id_input);
    }
    }
    </script>
    </j:jelly>
    ```

5.  Click **Submit**.


**Parent Topic:**[Using formatters](../concept/c_Formatters.md)

**Related topics**  


[Activity formatter](../concept/c_ActivityFormatter.md#)

[Create a formatter and add it to a form](t_CreateAFormatter.md)

[Process flow formatter](../reference/r_ProcessFlowFormatter.md#)

[Parent breadcrumbs formatter](t_TaskParentBreadcrumbsFormatter.md#)

[Approval summarizer formatter](../../service-administration/reference/r_ApprovalSummarizerFormatter.md)

[Limit the number of activity stream entries](limit-activity-stream-entries.md)

[Override a formatter with macros](t_UIMacroOverride.md)

