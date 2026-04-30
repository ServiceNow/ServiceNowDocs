---
title: Create a source for failure and resolution codes
description: Create a source to be associated with any failure or resolution code. The source for a code could be internal, external, or even from a manufacturer.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage failure and resolution codes, Configure, Enterprise Asset Management, IT Asset Management]
---

# Create a source for failure and resolution codes

Create a source to be associated with any failure or resolution code. The source for a code could be internal, external, or even from a manufacturer.

## Before you begin

Role required: sn\_eam.enterprise\_admin or inventory\_admin

## About this task

You should have at least one source before creating failure or resolution codes.

**Note:** Sources of the codes are stored in the Asset service source \[sn\_ent\_asset\_service\_source\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Workspace** &gt; **Admin center** &gt; **Failure and resolution**.

2.  In the Failure and resolution list, select **Sources**.

    Any existing sources are shown in the sources list.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_ims_flr_mfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Name of the source. For example, `External` or `Internal`.

</td></tr><tr><td>

Description

</td><td>

Brief description of the source.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

The source that you created is shown in the Sources list.

