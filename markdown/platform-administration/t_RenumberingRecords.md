---
title: Configure left padding of a system number in a table
description: You can configure the left padding of the system numbers on a table. For example, pad the Number field on an Incident, Problem, or Change Request.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Prepare to left-pad number fields in custom tables, Record numbering, Customize, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Configure left padding of a system number in a table

You can configure the left padding of the system numbers on a table. For example, pad the **Number** field on an Incident, Problem, or Change Request.

## Before you begin

If you are configuring numbers on a custom table or a table that does not extend the task table, then, before performing the following procedure, you must prepare business rules and script includes. For more information, see [Prepare to left-pad number fields in custom tables](t_PrepToLeftPadNumFldsInCustmTbls.md).

Role required: admin

## Procedure

1.  Navigate to the form, then right-click the **Number** field and select **Configure Dictionary**.

2.  Enter the following script in the **Default value** field and click **Update**.

    ```
    javascript:getNextObjNumberPadded();
    ```

3.  Navigate to **System Definition** &gt; **Number Maintenance**.

4.  Open the table record.

5.  Enter a value in the **Number of digits** field.

6.  Click **Update**.

    Number padding is applied to both existing and new records.

    ![Sys number padded](../image/SysNumberPadded.png)

    The result of the configuration in the image is an Incident number that is left padded.

    ![Padded incident number](../image/PaddedIncidentnumber.png)


**Parent Topic:**[Prepare to left-pad number fields in custom tables](t_PrepToLeftPadNumFldsInCustmTbls.md)

