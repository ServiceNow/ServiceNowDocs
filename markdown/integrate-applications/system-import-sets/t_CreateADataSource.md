---
title: Create an XML data source to another instance
description: Data sources are used to create an import set so that data can be processed, if necessary, prior to being mapped onto a production table.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using XML import sets, Importing from another ServiceNow instance, Import sets, Imports, Workflow Data Fabric]
---

# Create an XML data source to another instance

Data sources are used to create an import set so that data can be processed, if necessary, prior to being mapped onto a production table.

## Before you begin

Role required: admin.

## About this task

**Note:** To import using XML with High Security Settings enabled, you must possess elevated privileges.

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Data Sources**.

2.  Click **New**.

3.  Complete the form using the following values:

    | | |
    |---|---|
    |Import set table label|&lt;`import_set_table_label`&gt;|
    |Type|File|
    |Format|XML|
    |Xpath for each row|/xml/&lt;`source_table_name`&gt;|
    |Expand node children|true|
    |File retrieval method|HTTPS|
    |File path|/&lt;`source_table_name`&gt;.do?XML|
    |Server|&lt;instance name&gt;.service-now.com|
    |Port|Port to use to connect to the specified server.|
    |User name|A user account on the remote instance. The username used cannot be an email address.|
    |Password|The password for the same remote account.|

4.  Click **Submit**.

5.  Click **Test Load 20 Records** to create the import set table and to ensure that your data source is functional.

    **Note:** The 20 loaded records can't be transformed and are for testing purposes only.


**Parent Topic:**[Using XML import sets](../concept/c_XMLImportSets.md)

**Previous topic:**[Using XML import sets](../concept/c_XMLImportSets.md)

**Next topic:**[Create a transform map](t_CreateATransformMap.md)

