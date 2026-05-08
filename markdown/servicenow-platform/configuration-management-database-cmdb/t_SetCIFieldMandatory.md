---
title: Set a CI attribute to be mandatory
description: Configure a CI attribute as mandatory so it is included in the CMDB Health tests for the required metric if enabled. Required is a metric of the CMDB Health completeness KPI.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set a CI attribute to be mandatory

Configure a CI attribute as mandatory so it is included in the CMDB Health tests for the **required** metric if enabled. **Required** is a metric of the CMDB Health **completeness** KPI.

## Before you begin

Role required:

-   sn\_cmdb\_admin or Itil\_admin, and personalize\_dictionary: For editing the dictionary table
-   sn\_cmdb\_editor and itil have read access

## About this task

When a field is configured as mandatory, then if the **required** metric is enabled, the CMDB health tests check whether that field is populated or not. The CMDB Health Dashboard shows the aggregated report of the percentage of CIs for which one or more required fields is empty.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to display the CI Classes list. Then select the class with the field that needs to be set as mandatory.

3.  In the class navigation bar, expand **Class Info** and then select **Attributes**. In the Attributes view, click **Added**.

4.  Locate the attribute that you want to set as mandatory, and then double-click its **Mandatory** value and set it to true.

    The next time the form is opened, a field status indicator appears next to the field label, indicating that a value is mandatory.

    **Note:** Mandatory fields are global. The field is marked as mandatory everywhere it appears on a form. Also, mandatory fields do not appear correctly when using Service Mapping tag-based discovery. For more information, see Tag-based discovery in Service Mapping.


**Related topics**  


[CMDB Health Dashboard for Helsinki \| Overview](https://youtu.be/CvMRT3NExIo)

[bundle-platadm.t_MakingAFieldMandatory]

