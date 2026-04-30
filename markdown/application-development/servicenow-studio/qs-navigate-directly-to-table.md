---
title: Navigate directly to a table in ServiceNow Studio
description: Navigate directly to the list view of a table in ServiceNow Studio by using the Open list feature in the Navigator panel or search shortcuts in the main search.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ServiceNow Studio quick start, Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Navigate directly to a table in ServiceNow Studio

Navigate directly to the list view of a table in ServiceNow Studio by using the **Open list** feature in the Navigator panel or search shortcuts in the main search.

## Before you begin

Role required: admin or delegated\_developer

You can also watch a short video on how to navigate directly to a table.

Video on how to navigate directly to a table in ServiceNow Studio 

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Open a table directly in one of two ways.

    -   In the Navigator panel, with any application or file category selected, select **Open list**.

        The list opens in a new integrated tab. In the example below, this is a list of all apps on the Custom Applications table \[sys\_app\].![Open any list on the platform by opening it in the Navigator and selecting Open list.](../image/sn-studio-open-list.png)

    -   In the Search bar on the home page, enter one of the following inputs and press **Enter**.

        **Important:** The table name must match the name in the dictionary entry for the table. For more information about the primary table associated with each metadata type, see [ServiceNow Studio Navigator panel taxonomy](../reference/servicenow-studio-file-navigator-taxonomy.md).

        When you enter an input, the table view opens in a new integrated tab.

        |Input|Behavior|
        |-----|--------|
        |`<table name>.list`|Opens the list view of the table in the same window or tab.|
        |`<table name>.form` or `<table name>.do`|Opens the form view of the table in the same window or tab.|
        |`<table name>.config`|Opens the configuration view \[personalize\_all.do\] of the table in the same window or tab.|
        |`<table name>.filter`|Opens an empty list view of the table in the same window or tab, so that you can apply filters without loading the list. This is helpful for large lists that take a long time to load.|

        For example, if you want to open the list of all users in your organization, you could search for the Users table \[sys\_user\] using the search input `sys_user.list`. To add a new user quickly, search for `sys_user.do` to open a new form view of the Users table. To change the Users table configurations, search for `sys_user.config`. To open the Users table without loading any of the records, search for `sys_user.filter`.

        **Note:** You can use upper and lower case to change how the list view of a table opens.

        -   &lt;table\_name&gt;.lower case: Opens the table in the content pane.
        -   &lt;table\_name&gt;.UPPER case: Opens the table record or list in a new tab.

