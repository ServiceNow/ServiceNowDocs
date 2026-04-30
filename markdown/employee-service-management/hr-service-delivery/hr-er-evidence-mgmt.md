---
title: Evidence Management for Employee Relations
description: Use Evidence Management to capture and categorize evidence for Employee Relations or related cases.Set up HR Service Delivery Management so your agents can collect evidence and information related to Employee Relation \(ER\) cases.Create evidence types to catalog and organize employee relation evidence in an efficient and logical way to enhance your business processes.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Evidence Management for Employee Relations

Use Evidence Management to capture and categorize evidence for Employee Relations or related cases.

Evidence is defined as any digital artifacts gathered as part of an investigation, like files that are either uploaded to Evidence Management or reside in another system.

## Setting up Evidence Management

Set up HR Service Delivery Management so your agents can collect evidence and information related to Employee Relation \(ER\) cases.

You can activate Evidence Management \[com.sn\_evidence\_management\] plugin if you have the admin role. This plugin activates when the Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_realtions\] plugin is activated. For more information, see [Activate Employee Relations](../task/activate-hr-employee-relations.md#).

### Roles

The following roles are installed with the Evidence Management \[com.sn\_evidence\_management\] plugin:

<table id="table_v2h_p2t_lbc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Evidence admin \[sn\_em.admin\]

</td><td>

Can access and configure all areas within Evidence Management.

</td><td>

-   sn\_em.evidence\_config\_manager
-   sn\_em.evidence\_reader
-   sn\_em.evidence\_writer

</td></tr><tr><td>

Evidence Configuration manager \[sn\_em.evidence\_config\_manager\]

</td><td>

Can access, create, and manage evidence type records.**Note:** requires the evidence reader and writer roles to manage the evidence type records.

</td><td>

 

</td></tr><tr><td>

Evidence reader \[sn\_em.evidence\_reader\]

</td><td>

Can view evidence if the ER case is accessible.

</td><td>

 

</td></tr><tr><td>

Evidence writer \[sn\_em.evidence\_writer\]

</td><td>

Can create and manage evidence records.

</td><td>

sn\_em.evidence\_reader

</td></tr></tbody>
</table>Employee Relations roles include Evidence Management roles.

Users are unable to read evidence when impersonating.

When an Employee Relations case is restricted, users can only view the evidence record if they can view the ER case.

### Evidence types

Before you can add evidence to an ER case, you must set up evidence types. Evidence types help you categorize and organize the evidence you collect related to ER cases. The base system provides:

-   Audio
-   Chat logs
-   Email
-   Photos
-   Screenshots
-   SMS
-   Video

You can create additional evidence types. For more information, see [Create evidence types](hr-er-evidence-mgmt.md#).

### Create evidence types

Create evidence types to catalog and organize employee relation evidence in an efficient and logical way to enhance your business processes.

#### Before you begin

Role required: sn\_em.evidence\_config\_manager

**Note:** The base system provides preconfigured evidence types.

#### Procedure

1.  Navigate to **All** &gt; **Evidence Management** &gt; **Evidence Types**.

2.  Select **New**.

3.  Fill in the form or edit the fields.

    |Field|Value|
    |-----|-----|
    |**Name**|The name that identifies and describes the evidence type.|
    |**Active**|Indicates if the evidence type is active and available for use.|

4.  Select **Submit**.


