---
title: Change the maximum image size
description: Adjust the maximum size that is accepted for images used for playbook generation.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-10-08"
reading_time_minutes: 1
breadcrumb: [Configuring Playbook Assist, Playbook Assist, Exploring playbooks, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Change the maximum image size

Adjust the maximum size that is accepted for images used for playbook generation.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties** for the \[sys\_properties.list\] table.

2.  Search for and open the **com.glide.attachment.max\_get\_size** property.

3.  If the property doesn't exist yet, create the **com.glide.attachment.max\_get\_size** property.

    1.  Select **New** in the upper right corner.

    2.  Enter values for the following fields:

<table id="table_tg1_mnt_51b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name the property **com.glide.attachment.max\_get\_size**.

</td></tr><tr><td>

Type

</td><td>

Select **integer** from the drop-down.

</td></tr><tr><td>

Value

</td><td>

Enter the maximum bytes allowed for an uploaded image. The default value is 5242880 bytes \(5 MB\), but you can increase this up to 10485760 bytes \(10 MB\) or down to 102400 bytes \(100 KB\).-   **Megabytes \(MB\)**

If the equivalent MB value has a decimal and is between 1 MB and 10 MB, the value is rounded down to the next whole MB. For example, if you enter 4980736 bytes \(4.75 MB\), the maximum size will be 4194304 \(4 MB\).

-   **Kilobytes \(KB\)**

If the value is less than 1 MB, the equivalent KB value is rounded down to the next whole KB. For example, if the value is 580608 bytes \(567 KB\), the maximum size limit is rounded down to 512000 bytes \(500 KB\).

-   **Less or greater than 5 MB**

Images smaller than 5242880 bytes \(5 MB\) are scaled down. Images that are larger than 5 MB are not scaled and the system creates a link instead.

-   **Greater than 10 MB**

If the value is more than 10 MB, such as 12582912 bytes \(12 MB\), the maximum size defaults to 10485760 bytes \(10 MB\).

-   **100 KB minimum**

If the value is less than 102400 bytes \(100 KB\), such as 91136 bytes \(89 KB\), the maximum size defaults to 102400 bytes \(100 KB\).

</td></tr></tbody>
</table>4.  Select **Submit** in the upper right corner.


## Result

The maximum size for an image upload is set or changed.

**Parent Topic:**[Configuring Playbook Assist](../concept/configuring-playbook-assist.md)

**Related topics**  


[Generate a playbook](generate-a-playbook-outline.md)

[Administering attachments](https://www.servicenow.com/docs/access?context=r_AdministeringAttachments&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

[General Guidelines for Building Playbooks with Now Assist](../reference/general-guidelines-playbook-assist.md)

