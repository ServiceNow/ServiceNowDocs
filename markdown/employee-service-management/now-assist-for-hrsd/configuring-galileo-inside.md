---
title: Configure Now Assist AI Helper – Galileo Inside
description: Enable users to access functionality and benefits of the Now Assist AI Helper – Galileo Inside \[sn\_hr\_na\_galileo\] plugin by completing a short installation and configuration process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/now-assist-for-hrsd/configuring-galileo-inside.html
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-04-28"
reading_time_minutes: 3
breadcrumb: [Configure, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure Now Assist AI Helper – Galileo Inside

Enable users to access functionality and benefits of the Now Assist AI Helper – Galileo Inside \[sn\_hr\_na\_galileo\] plugin by completing a short installation and configuration process.

## Before you begin

Obtain the API key from The Josh Bersin Company.

Role required: admin

## Procedure

1.  Install the Now Assist AI Helper – Galileo Inside plugin \(sn\_hr\_na\_galileo\).

    For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

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

Next, assign the `sn_hr_na_galileo.read` role to users to enable them to interact with Now Assist AI Helper – Galileo Inside.

**Parent Topic:**[Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

**Related topics**  


[Skill inputs and triggers for ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[RCA approvals for ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Restrict Now Assist capabilities for employee relations cases]()

[Customize the ServiceNow Otto for HRSD skills]()

[Configure attachment summary]()

[Configure resolution notes generation for ServiceNow Otto for HRSD]()

[Configure sensitivity detection]()

[Configure Gen AI Virtual Agent for HRSD]()

[Configure the ServiceNow Otto for HRSD Virtual Agent topics]()

[Configure HCM agents for HR Service Delivery AI Agent Collection]()

[Use Galileo Inside to answer HR-related questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/use-galileo-inside.md)

