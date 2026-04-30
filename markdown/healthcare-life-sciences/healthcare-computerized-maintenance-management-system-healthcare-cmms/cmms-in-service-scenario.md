---
title: Healthcare Computerized Maintenance Management System - medical devices in-service scenario
description: Use the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application for setting medical devices in-service and associating them with maintenance plans.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Healthcare CMMS, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Healthcare Computerized Maintenance Management System - medical devices in-service scenario

Use the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application for setting medical devices in-service and associating them with maintenance plans.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

Scenario: A hospital purchases a new infusion pump that needs to be set to in-service and scheduled for planned maintenance. A device organization contributor, who acts as a requester with the sn\_hcls\_cmms.device\_service\_org\_contributor role, works at the hospital location and submits the medical device in-service request form from the hospital's customer service portal. In the medical device in-service request form, the contributor enters the medical device model and medical device details such as model name, model number, manufacturer, short description, serial number, organization, and cost center. When the new medical device model is set to in-service, select **Allow alternate maintenance** in the medical device in-service request form in order to be able to enter a request for the AEM. After submitting the medical device in-service request form, a medical device in-service case is created in the ServiceNow instance associated with the customer service portal of the hospital. To resolve the case, the Healthcare CMMS workflow initiates a playbook configured for the medical device in-service cases. The case gets assigned to a clinical engineer who acts as a fulfiller with the sn\_hcls\_cmms.clinical\_engineer role.

The following graphic shows how the Healthcare CMMS application is used for medical devices in-service scenario.

![Workflow to set the medical device in-service using the Healthcare CMMS application. For the text description, refer to the workflow steps.](../image/cmms-cd-onboarding-scenario.png "Using the Healthcare CMMS application for medical devices in-service")

The following workflow steps elaborate how the clinical engineers with the sn\_hcls\_cmms.clinical\_engineer role use the Healthcare CMMS application to enable the medical device in-service:

1.  Uses the Workspace to view the medical device in-service case.
2.  In Workspace, views the complete information about the medical device and its model from the **Details** tab.
3.  Selects the **Playbook** tab to view all the necessary case-related information.

    The layout of a playbook enables clinical engineers to focus on the steps they are responsible for, while providing full visibility into the end-to-end process life cycle.

4.  Reviews the medical device model.
5.  Reviews the devices that are included in the case and assesses the risks for each medical device.
6.  Reviews the work orders for the initial inspection of each medical device.
7.  After the inspection of a medical device is completed, adds a maintenance plan for a new model/ medical device and reviews the maintenance plan.
8.  Ensures that all medical device in-service tasks are set to complete in the playbook and closes the medical device in-service case.

