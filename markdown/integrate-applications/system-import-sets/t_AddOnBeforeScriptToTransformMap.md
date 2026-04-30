---
title: Add onBefore scripts to the transform map
description: Create one onBefore transform map script to copy the sys\_id of new records from the source to the target instance. Create a second onBefore transform map script to identify records on the target instance that have the same unique values but different sys\_id values.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using XML import sets, Importing from another ServiceNow instance, Import sets, Imports, Workflow Data Fabric]
---

# Add onBefore scripts to the transform map

Create one onBefore transform map script to copy the sys\_id of new records from the source to the target instance. Create a second onBefore transform map script to identify records on the target instance that have the same unique values but different sys\_id values.

## Before you begin

Role required: admin.

## Procedure

1.  Open the table transform map record you created.

2.  In the **Transform Scripts** related list, click **New**.

3.  In the **When** field, select **onBefore**.

4.  Enter the following script:

    ```
    if (action == "insert") {target.setNewGuidValue(source.u_sys_id); }
    ```

5.  Click **Submit**.

6.  In the **Transform Scripts** related list, click **New**.

7.  In the **When** field, select **onBefore**.

8.  Enter the following **Script**:

    ```
    /** 
    * This script queries for a uniquely identifying value of the referenced record and then 
    * updates the target reference field with the sys_id of the matching target record.
    * This sample assumes:
    * 1) The target table contains an assigned_to field which is a reference field.
    * 2) The reference field references the User [sys_user] table.
    * 3) You can use the email field to uniquely identify users. Alternatively you
    *    could use the user_name field.
    */
    var ref = new GlideRecord("sys_user"); //Replace sys_user with any reference table
    ref.addQuery("email", source.email); //Replace email with any unique field
    ref.query();
    if(ref.next()){
       target.assigned_to = ref.sys_id; //Replace assigned_to with any reference field
    }
    ```

9.  Click **Submit**.


**Parent Topic:**[Using XML import sets](../concept/c_XMLImportSets.md)

**Previous topic:**[Create a transform map](t_CreateATransformMap.md)

**Next topic:**[Retrieving data from a CSV formatted file](t_RetrieveDataFromACSVFormatFile.md)

