---
title: Unique record identifier \(sys\_id\)
description: A unique 32-character GUID \(Globally Unique ID\), called a Sys ID \(sys\_id\) identifies each record in an instance.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Unique record identifier \(sys\_id\)

A unique 32-character GUID \(Globally Unique ID\), called a Sys ID \(sys\_id\) identifies each record in an instance.

When created within the application, sys\_id values are unique. The ServiceNow AI Platform and database should manage all operations on sys\_id values. The same sys\_id value is never generated twice, which ensures that every record created in every table in every instance in the world has a unique identifier. If two records have the same sys\_id value, it occurs as a result of the following situations:

-   If a record with the sys\_id was copied to the other at the database level outside of the ServiceNow AI Platform.
-   If a record with the sys\_id was copied using an Update Set or via XML, its sys\_id is the same.


**Note:** A new record has a sys\_id of -1, and once inserted, it is assigned a new sys\_id. The sys\_id is not meant to show as a field on a form or as a column in a list. To learn more, see the [Users are unable to add the sys\_id field to a form or list view](https://support.servicenow.com/kb_view.do?sysparm_article=KB0690876) \[KB0690876\] article in the Now Support Knowledge Base.

You can access the sys\_id from a record URL or by using a script.

-   To access the sys\_id from the URL, navigate to any record, right-click the header bar, and select **Copy URL**. The sys\_id is inside of the URL, after the parameter sys\_id=.
-   To access the sys\_id using a script, use one of the following options.
    -   Find the sys\_id of a record in a business rule \(or any other server-side JavaScript\) by dot-walking from the GlideRecord.

        ```
        var id = current.sys_id;
        ```

    -   Find the sys\_id of a record in client-side JavaScript using g\_form.getUniqueValue\(\).

        ```
        function onLoad() {
            var incSysid = g_form.getUniqueValue();
            alert(incSysid);
        }
        ```


**Parent Topic:**[Data Management reference](../../managing-data/reference/data-management-reference.md)

