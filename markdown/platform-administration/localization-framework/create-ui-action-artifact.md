---
title: Create a UI action for the custom artifact
description: Create a UI action to request translations for the custom artifact.
locale: en-US
release: yokohama
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Artifact configurations, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a UI action for the custom artifact

Create a UI action to request translations for the custom artifact.

## Before you begin

Role required: localization\_admin

## Procedure

1.  Navigate to the custom artifact table.

    Find the table using its table name. For example, **\[sys\_cs\_topic\]** is the table name for Virtual Agent topics.

2.  Click the hamburger icon \(![Hamburger icon](../../search-administration/image/hamburger-icon.png)\) at any of the columns and navigate to **Configure** **UI Actions**.

3.  Click **New**.

4.  In the UI Actions form, fill in the fields.

<table id="table_if2_jvj_xnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the UI action.For example, **Request Translations**.

</td></tr><tr><td>

Client

</td><td>

Option to execute the script in the user's browser. When enabled, the **Onclick** field appears above the Condition field.

</td></tr><tr><td>

Condition

</td><td>

Condition to decide when to show this UI action.

</td></tr><tr><td>

Onclick

</td><td>

Provide the JavaScript function name as:```
renderLanguagePickerModal();
```

</td></tr><tr><td>

Script

</td><td>

Option to execute the script to run the request translations function. The script varies for **Form button** and **List choice**.

-   Form Button

    ```
function renderLanguagePickerModal() {

    var dlg = new GlideModal("sn_lf_language_picker");
    dlg.setTitle(getMessage("Request Translations"));
    dlg.setPreference("sys_id", g_form.getUniqueValue());
    dlg.setPreference("artifact_config_internal_name", "catalog_item");
    dlg.setPreference("request_type", "form");
    dlg.setPreference("focusTrap", true);
    dlg.render();
}
    ```

-   List choice

    ```
function renderLanguagePickerModal() {
    var sys_ids = g_list.getChecked();
    if (!sys_ids || sys_ids.length == 0)
        return;
    var dlg = new GlideModal("sn_lf_language_picker");
    dlg.setTitle(getMessage("Request Translations"));
    dlg.setPreference("sys_id", sys_ids);
    dlg.setPreference("artifact_config_internal_name", "catalog_item");
    dlg.setPreference("request_type", "list");
    dlg.setPreference("focusTrap", true);
    dlg.render();
}
    ```

</td></tr><tr><td>

Form button

</td><td>

Option to enable the UI action as a form button.

</td></tr><tr><td>

List choice

</td><td>

Option to enable the UI action in the choice list.

</td></tr></tbody>
</table>    **Note:** Configure the form to see all the fields. For more information, see [Create a UI action](../../list-administration/task/t_EditingAUIAction.md).

5.  Click **Submit**.


**Parent Topic:**[Artifact configurations](../concept/framework-configuration.md)

