---
title: Reference field icon
description: On forms, the reference icon \( Core UI reference icon \) appears by populated reference fields. Clicking the icon opens a read-only preview of the referenced record.Use a table's sys\_popup form view to configure the fields in the pop-up form that appear when pointing to a reference icon. If the table has no sys\_popup view, the pop-up uses the default view.Reference pop-ups and click-throughs are hidden by default when a client script, UI policy, variable, or ACL makes the field read-only. The ability to see or click through to the target record does not depend on whether the reference field is writable. You can change the read-only setting.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Decorations, Reference field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Reference field icon

On forms, the reference icon \(![Core UI reference icon](../image/IconReferenceUI15.png)\) appears by populated reference fields. Clicking the icon opens a read-only preview of the referenced record.

![Pointing to the reference icon, which looks like the letter I in a circle, opens a preview of the record over the form](../image/ReferencedRecordUI15.png "Referenced record preview on a form")

The preview remains open until you click somewhere else on the form.

Click **Open Record** to navigate to the referenced record.

**Note:** When using a reference icon in Service Portal, a form opens using the default view of the form rather than a popup view. Write permissions to this form are the same as opening the form in the default view in the standard UI.

## Configure the reference icon view of fields

Use a table's sys\_popup form view to configure the fields in the pop-up form that appear when pointing to a reference icon. If the table has no sys\_popup view, the pop-up uses the default view.

### Before you begin

Role required: personalize\_form

### About this task

The pop-up form displays in the top form section only.

### Procedure

1.  To configure a reference field popup form for a table using the default sys\_popup view, navigate to the following URL format, substituting the instance name and table name:

    ```
    <your instance name>.service-now.com/<table name>.do?sysparm_view=sys_popup
    ```

    **Note:** This URL format only shows a table and default sys\_popup view. It does not work for records that use a different view.

    An example of an instance for Acme, the sys\_user table, and the sys\_popup default view:

    ```
    acme.service-now.com/sys_user.do?sysparm_view=sys_popup
    ```

2.  To configure a reference field popup form for a table using a non-default sys\_popup view, navigate to the following URL format, substituting the instance name, table name, and name of view:

    ```
    <your instance name>.service-now.com/<table name>.do?sysparm_view=sys_popup,<name_of_view>
    ```

    An example of an instance for Acme, the sys\_user table, and the sys\_popup ESS view:

    ```
    acme.service-now.com/sys_user.do?sysparm_view=sys_popup,ess
    ```

3.  Configure the form to add or remove fields as appropriate.


## Configure pop-ups on read-only fields

Reference pop-ups and click-throughs are hidden by default when a client script, UI policy, variable, or ACL makes the field read-only. The ability to see or click through to the target record does not depend on whether the reference field is writable. You can change the read-only setting.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Change the value of the **Enable click-through of a reference field when the reference field is read-only.** \(**glide.ui.reference.readonly.clickthrough**\) property.

    If set to true, the pop-up appears for read-only fields and for variables.


### What to do next

If this system value is set to **false**, you can override the setting for a specific read-only reference field. Configure the dictionary entry and add the **readonly\_clickthrough=true** attribute.

![Read-only clickthrough attribute in dictionary entry](../image/ClickThroughAttribute.png "Dictionary entry showing the clickthrough attribute")

