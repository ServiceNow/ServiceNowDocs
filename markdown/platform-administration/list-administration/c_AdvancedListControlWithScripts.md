---
title: Advanced list control with scripts
description: You can write scripts to specify which list elements, such as links, filters, and buttons, are present.You can create a UI action that opens the slushbucket interface to customize lists in the list view.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [List configuration, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Advanced list control with scripts

You can write scripts to specify which list elements, such as links, filters, and buttons, are present.

These scripts can react to the record that is being displayed. For related list controls, the global variable **parent** identifies the parent record. For primary lists, there is no parent record.

[Configure](../../form-administration/concept/configure-form-layout.md#) the List Control form and add the script field that you need:

-   **Omit Columns Condition:** If there are no conditions, omit column headings.
-   **Omit Edit Condition:** Omit the **Edit** button.
-   **Omit Empty Condition:** If there are no conditions, omit the list header.
-   **Omit Filter Condition:** Omit the list filter.
-   **Omit Links Condition:** Omit related links.
-   **Omit New Condition:** Omit the **New** button.

In these script fields, if the script evaluates to **true**, the item is omitted. The following script is an example that you can use on the **Affected CIs** related list to show only the **Edit** button if the parent task is active. This script is placed in the **Omit Edit Condition** script field.

```
var answer;
 if (parent.active == true ) {
 //Do not remove the 'Edit' button
  answer = false; 
} 
else {
 //Remove the 'Edit' button
  answer = true;
}
answer;
```

**Parent Topic:**[List configuration](c_ListConfiguration.md)

## Configure a list UI action

You can create a UI action that opens the slushbucket interface to customize lists in the list view.

### Before you begin

Role required: ui\_action\_admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **UI Actions**.

2.  Click **New**.

3.  In the **Table** field, select the **List \[sys\_ui\_list\]** table.

4.  Select the **List context menu** check box.

5.  Ensure the **Active** check box is selected.

6.  Paste the following script in the **Script** field:

    ```
    var url  = "slushbucket.do?sysparm_form=list&sysparm_list=" + current. name + "&sysparm_view=" + current. view. name ;
    url  += "&sysparm_collection=" + current. parent + "&sysparm_collection_relationship=" + current. relationship ; 
    url  += "&sysparm_referring_url=sys_ui_view.do?sys_id=" + current. view. toString ( ) ;
    action. setRedirectURL (url ) ;
    ```

7.  Click **Submit**.


