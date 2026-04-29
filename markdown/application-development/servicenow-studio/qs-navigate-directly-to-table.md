---
title: Navigate directly to a table in ServiceNow Studio
description: Open any table view directly in ServiceNow Studio using the Open list feature in the Navigator panel or search shortcuts in the Search bar.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Studio quick start, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Navigate directly to a table in ServiceNow Studio

Open any table view directly in ServiceNow Studio using the **Open list** feature in the Navigator panel or search shortcuts in the Search bar.

## Before you begin

Role required: admin or delegated\_developer

Watch a short video on how to navigate directly to a table.

Video on how to navigate directly to a table in ServiceNow Studio 

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Open a table directly using one of the following options.

    -   In the Navigator panel, with any application or file category selected, select **Open list**.

        The list opens in a new tab. In the example below, this is a list of all apps on the Custom Applications table \[sys\_app\].![Open any list on the platform by opening it in the Navigator and selecting Open list.](../image/sn-studio-open-list.png)

    -   In the Search bar, enter one of the inputs in the table below and press **Enter**. The table view opens in a new tab.

        **Important:** The table name must match the name in the dictionary entry for the table. For more information about the primary table associated with each metadata type, see [ServiceNow Studio Navigator panel taxonomy](../reference/servicenow-studio-file-navigator-taxonomy.md).

        To find the primary table name for a metadata type, select the metadata type in the Navigator panel. The primary table name appears below it. In the following example, **sys\_hub\_action\_type\_definition** is the table name for the **Action** metadata type.

        ![View the table name for a metadata type under the name.](../image/sn-studio-table-name.png)

        When you enter an input, the table view opens in a new tab.

        |Input|Result|
        |-----|------|
        |`<table name>.list`|Opens the list view of the table.|
        |`<table name>.form` or `<table name>.do`|Opens the form view of the table.|
        |`<table name>.config`|Opens the configuration view \[personalize\_all.do\] of the table.|
        |`<table name>.filter`|Opens an empty list view of the table so you can apply filters without loading all records. Use this shortcut for large tables that take a long time to load.|

        For example, to open the list of all users, search for the Users table \[sys\_user\] using `sys_user.list`. To open a new form view of the Users table, search for `sys_user.do`. To open the Users table configuration, search for `sys_user.config`. To open the Users table without loading any records, search for `sys_user.filter`.

        **Note:** Use upper or lower case to control how the table opens.

        -   &lt;table\_name&gt;.lower case: Opens the table in the content pane.
        -   &lt;table\_name&gt;.UPPER case: Opens the table record or list in a new tab.

