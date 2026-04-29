---
title: Create a multi-table processor
description: Create a multi-table processor that reports the number of rows in any table on your instance. This feature is deprecated.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Processors, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Create a multi-table processor

Create a multi-table processor that reports the number of rows in any table on your instance. This feature is deprecated.

## Before you begin

Role required: admin

## About this task

**Note:** This feature is deprecated. While legacy, existing custom processors continue to be supported, creating new custom processors has been deprecated. Instead, use the [Scripted REST APIs](../../../../integrate/custom-web-services/concept/c_CustomWebServices.md)

The multi-table processor protects itself from performance and security violations by confirming that the user is authorized to read the table. It does not report on certain tables that are too large to query safely.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Processors**.

    The list of processors appears.

2.  Select**New**.

3.  Enter the following information.

<table id="table_jxj_zbf_hq"><tbody><tr><td>

**Name**

</td><td>

TableSize

</td></tr><tr><td>

**Type**

</td><td>

Choose **Javascript**

</td></tr><tr><td>

**Description**

</td><td>

Return number of records in a table

</td></tr><tr><td>

**Parameters**

</td><td>

**SIZE**

</td></tr><tr><td>

**Path**

</td><td>

&lt;leave empty&gt;

</td></tr></tbody>
</table>    Script:

    ```
    g_response.setContentType('text/html;charset=UTF-8');
    if(g_target === 'sys_email' || g_target === 'sys_log' ) 
    {
      g_processor.writeOutput(g_target + ' table is too large to quickly count');
      } else {   
        var count = new GlideAggregate(g_target);
        if( count.canRead() ) {
          count.addAggregate('COUNT');
          count.query();
          var records = 0;
          if (count.next()) {
            records = count.getAggregate('COUNT');
           }
           g_processor.writeOutput('table ' + g_target + ' has ' + records + ' records');
          } else {
           g_processor.writeOutput('You do not have access to table ' + g_target);
      }
    }            
    ```

4.  Select **Save**.

5.  Test the new processor by entering the following URLs:

    `https://<instancename>.service-now.com/incident.do?SIZE` and `https://<instancename>.service-now.com/sys_user.do?SIZE`

    Your instance reports the number of records in the table. For example, `table incident has 82 records`.


**Parent Topic:**[Processors](../../../../script/processors/concept/c_Processors.md)

