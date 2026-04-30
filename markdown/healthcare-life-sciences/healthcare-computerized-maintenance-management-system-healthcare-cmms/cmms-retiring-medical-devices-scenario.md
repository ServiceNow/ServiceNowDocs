---
title: Healthcare Computerized Maintenance Management System - Medical devices out-of-service scenario
description: Use the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application for setting medical devices to out-of-service and creating disposal work orders for them.
locale: en-US
release: zurich
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Healthcare Computerized Maintenance Management System, Clinical Device Management, Healthcare and Life Sciences]
---

# Healthcare Computerized Maintenance Management System - Medical devices out-of-service scenario

Use the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application for setting medical devices to out-of-service and creating disposal work orders for them.

**Important:** Healthcare Computerized Maintenance Management System is now deprecated and no longer supported or available for new activation. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

Scenario: A hospital needs to discontinue or replace an old medical device with new model. Due to a fault leading it to be beyond repair, the medical device being replaced needs to be set to out-of-service. A device organization contributor who acts as requester with the sn\_hcls\_cmms.device\_service\_org\_contributor role works at the hospital location submits the out-of-service request form from a customer service portal of the hospital. In the out-of-service request form, the contributor enters the medical device model and medical device details such as requested by, requested organization, device model, device, requester comments for out-of-service medical device, short description. After submitting the out-of-service request form, a medical device out-of-service case is created in the ServiceNow instance associated with the customer service portal of the hospital. To resolve the case, the Healthcare CMMS workflow initiates a playbook configured for the medical device out-of-service cases. The case gets assigned to a clinical engineer who acts as a fulfiller with the sn\_hcls\_cmms.clinical\_engineer role.

