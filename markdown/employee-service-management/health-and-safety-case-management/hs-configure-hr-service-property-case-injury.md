---
title: Configure HR service for creating an HR case for an injury
description: Configure the HR service that you want to use for creating HR cases for injuries and illnesses.
locale: en-US
release: australia
product: Health and Safety Case Management
classification: health-and-safety-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Health and Safety Case Management, Health and Safety, Employee Service Management]
---

# Configure HR service for creating an HR case for an injury

Configure the HR service that you want to use for creating HR cases for injuries and illnesses.

## Before you begin

Ensure that the following conditions are met:

-   The Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is installed on your ServiceNow instance. For more information on activating it, see [Activate Case and Knowledge Management](../../human-resources/task/activate-case-and-knowledge-management-scoped.md).
-   The application scope is selected as Health and Safety Case Management. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: sn\_hs\_cm.case\_manager and sn\_hr\_core.admin

## About this task

For information on HR services and what you can configure, see [HR services](../../human-resources/concept/hr-service-administration.md).

## Procedure

1.  Copy the sys\_id of the HR service.

    1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

    2.  In the list, select the HR service that you want to use for creating HR cases from injury and illness records.

    3.  Right-click the HR service and select **Copy sys\_id**.

2.  Update the sys\_id of the HR service in the system property.

    1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety administration** &gt; **Properties**.

    2.  In the **HR Service sys\_id** \(**sn\_hs\_cm.hr\_service\_sys\_id**\) property, update the sys\_id that you copied in step 1.

    3.  Select **Save**.


**Parent Topic:**[Configuring Health and Safety Case Management](../concept/hs-setting-up-case-management.md)

**Previous topic:**[Install Health and Safety Case Management](install-hs-case-management.md)

**Next topic:**[Submitting Health and Safety cases](../concept/hs-submitting-health-safety-cases.md)

