---
title: Configure the list page in Service Operations Workspace for ITSM
description: Configure the fuzzyCount property to modify how the number of records is displayed on the SOW list page thus improving system performance.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Service Operations Workspace for ITSM to improve your experience, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the list page in Service Operations Workspace for ITSM

Configure the **fuzzyCount** property to modify how the number of records is displayed on the SOW list page thus improving system performance.

## About this task

The input of the **fuzzyCount** property is JSON key value pair.

**Note:** The property applies to any new list component used across SOW pages where record count limit input for the component isn't defined.

On the SOW list page, right-click on a record to use the following options:

-   Copy URL: Copy the URL of the record to a clipboard and share the record URL with other stakeholders.
-   Copy sys ID: Copy the sys ID of the record to a clipboard and share the sys ID of the record with other stakeholders

**Note:** You can resize the modal in the SRP and list pages in SOW.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

2.  From the list of UX applications, select **Service Operations Workspace**.

3.  On the UX Application form, from the UX Page Properties related list, select the **fuzzyCount** property.

4.  On the UX Page Property page, edit the **Value** field.

<table id="table_pgs_wcw_cdc"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{"default":-1\}.

</td><td>

Displays the count of the total number of records in a list.![Count of incidents](../image/fuzzycount.png)

</td></tr><tr><td>

\{"default":&lt;integer&gt;\}.

</td><td>

Displays the count of the number of records in a list as &lt;integer+&gt;.For example, if the incident has 124 records, if you configure the value of the property as 10, the system displays the count of incidents as 10+.

![Count after updating the value of fuzzyCount property](../image/fuzzycount-2.png)

</td></tr><tr><td>

\{"default":&lt;integer&gt;, "incident": &lt;integer1&gt;\}.

</td><td>

Displays the count of the number of records in a list as &lt;integer+&gt;.For example, if the incident has 14 records, if you configure the incident value in the property as 10, the system displays the count of incidents as 10 and for the non incident list, the count will be based on the default value defined in the property.

</td></tr></tbody>
</table>5.  Select **Update**.


**Parent Topic:**[Configuring Service Operations Workspace for ITSM to improve your experience](../concept/configuring-sow-to-improve-experience.md)

