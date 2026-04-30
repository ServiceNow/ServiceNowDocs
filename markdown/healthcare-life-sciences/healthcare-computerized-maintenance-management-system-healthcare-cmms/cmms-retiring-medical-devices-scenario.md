---
title: Healthcare Computerized Maintenance Management System - Medical devices out-of-service scenario
description: Use the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application for setting medical devices to out-of-service and creating disposal work orders for them.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Healthcare CMMS, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Healthcare Computerized Maintenance Management System - Medical devices out-of-service scenario

Use the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application for setting medical devices to out-of-service and creating disposal work orders for them.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

Scenario: A hospital needs to discontinue or replace an old medical device with new model. Due to a fault leading it to be beyond repair, the medical device being replaced needs to be set to out-of-service. A device organization contributor who acts as requester with the sn\_hcls\_cmms.device\_service\_org\_contributor role works at the hospital location submits the out-of-service request form from a customer service portal of the hospital. In the out-of-service request form, the contributor enters the medical device model and medical device details such as requested by, requested organization, device model, device, requester comments for out-of-service medical device, short description. After submitting the out-of-service request form, a medical device out-of-service case is created in the ServiceNow instance associated with the customer service portal of the hospital. To resolve the case, the Healthcare CMMS workflow initiates a playbook configured for the medical device out-of-service cases. The case gets assigned to a clinical engineer who acts as a fulfiller with the sn\_hcls\_cmms.clinical\_engineer role.

The following workflow elaborates how the clinical engineers with the sn\_hcls\_cmms.clinical\_engineer role use the application to out-of-service medical devices:

![Workflow for setting medical devices to out-of-service using the Healthcare CMMS application. For the text description, refer to the workflow steps that follow.](../image/cmms-out-of-service-medical-device.png "Using the Healthcare CMMS application for medical device out-of-service")

1.  Uses the Workspace to view the medical device out-of-service case.
2.  In Workspace, views the complete information about the medical device and its model from the **Details** tab.
3.  Selects the **Playbook** tab to view all the necessary case-related information.

    The layout of a playbook enables clinical engineers to focus on the steps they’re responsible for, while providing full visibility into the end-to-end process life cycle.

4.  Reviews the medical device details.
5.  Reviews and cancel all the work orders for the related medical device.
6.  Ensures that all the work orders are canceled.
7.  Sets the medical device to out-of-service.
8.  Creates the disposal work order for the out-of-service device.
9.  Ensures that all out-of-service tasks are set to complete in the playbook and closes the medical device out-of-service case.

