---
title: Configure the list page in Service Operations Workspace for ITSM
description: Configure the fuzzyCount property to modify how the number of records is displayed on the Service Operations Workspace \(SOW\) list page. Configuring the fuzzyCount property helps improve the system performance.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Service Operations Workspace for ITSM to improve your experience, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the list page in Service Operations Workspace for ITSM

Configure the **fuzzyCount** property to modify how the number of records is displayed on the Service Operations Workspace \(SOW\) list page. Configuring the **fuzzyCount** property helps improve the system performance.

## About this task

The input of the **fuzzyCount** property is JSON key value pair. The property applies to any new list component used across SOW pages where record count limit input for the component isn't defined.

The **fuzzyCount** property applies to all SOW list including related list and Multi Record Associator \(MRA\) list in the SOW records pages.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  On the SOW Admin Center page, navigate to **Initial setup** &gt; **SOW properties**.

3.  On the SOW properties page, in the **Improve page load speed for list view pages in SOW** tile, select **Configure**.

    The **fuzzyCount** UX property page opens on a separate tab.

    Alternatively, you can also access the **fuzzyCount** UX property page by navigating to **All** &gt; **Now Experience Framework** &gt; **Experiences**. From the list of UX applications, select **Service Operations Workspace** and then from the UX Page Properties related list, select the **fuzzyCount** property.

4.  On the UX Page Property page, edit the **Value** field.

<table id="table_pgs_wcw_cdc"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{"default":-1\}.

</td><td>

Displays the count of the total number of records in a list. The fuzzyCount UX property is not applied to the SOW list page.![Count of incidents](../image/fuzzycount.png)

</td></tr><tr><td>

\{"default":&lt;integer&gt;\}.

</td><td>

Displays the count of the number of records in a list as &lt;integer+&gt;.For example, if the incident has 124 records, if you configure the value of the property as 10, the system displays the count of incidents as 10+.

![Count after updating the value of fuzzyCount property](../image/fuzzycount-2.png)

</td></tr><tr><td>

\{"default":&lt;integer&gt;, "incident": &lt;integer1&gt;\}.

</td><td>

Displays the count of the number of records in a list as &lt;integer+&gt;. You can also set the count of the records to be displayed for a specific table or record type such as incident.For example, if the incident has 14 records, if you configure the incident value in the property as 10 and default value as 20, the system displays the count of incident records as 10+ and for the non incident list, the count is displayed based on the default value defined in the property which is 20+.

</td></tr></tbody>
</table>5.  Select **Update**.


**Parent Topic:**[Configuring Service Operations Workspace for ITSM to improve your experience](../concept/configuring-sow-to-improve-experience.md)

