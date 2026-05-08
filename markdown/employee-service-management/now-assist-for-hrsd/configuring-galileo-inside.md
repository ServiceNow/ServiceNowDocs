---
title: Configure Now Assist for HR - Galileo Inside
description: Enable users to access functionality and benefits of the Now Assist for HR - Galileo Inside \[sn\_hr\_na\_galileo\] plugin by completing a short installation and configuration process.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure Now Assist for HR - Galileo Inside

Enable users to access functionality and benefits of the Now Assist for HR - Galileo Inside \[sn\_hr\_na\_galileo\] plugin by completing a short installation and configuration process.

## Before you begin

Obtain the API key from The Josh Bersin Company.

Role required: admin

## Procedure

1.  Install the Now Assist for HR - Galileo Inside \(sn\_hr\_na\_galileo\).

    For information about the installation process, see Install Now Assist plugins.

2.  Input your Josh Bersin credentials into your ServiceNow instance.

    1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Credentials**.

    2.  Select **Galileo Inside API Key**.

    3.  In the **API Key** field, delete the placeholder value and enter the API key you received from the Josh Bersin company.

    4.  Select **Update**.

3.  Load Galileo data into your ServiceNow instance.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Select **Fetch and Index Galileo data**.

    3.  Select **Execute Now**.

        The process to fetch and index the Galileo data takes between two to four hours. After four hours, check the sn\_hr\_gen\_ai\_external\_content\_connector\_metadata table for a record to confirm the indexing result.

    When the scheduled job is done, the Galileo data is available to users with the `n_hr_na_galileo.read` or `n_hr_na_galileo.admin` roles.


## What to do next

Next, assign the `sn_hr_na_galileo.read` role to users to enable them to interact with Now Assist for HR - Galileo Inside.

**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md)

**Related topics**  


[Use Now Assist for HR - Galileo Inside to answer HR-related questions](use-galileo-inside.md)

