---
title: Healthcare Computerized Maintenance Management System - Reviewing AEM request scenario
description: Use the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application for reviewing the existing maintenance plan related to a medical device model.
locale: en-US
release: zurich
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Healthcare Computerized Maintenance Management System, Clinical Device Management, Healthcare and Life Sciences]
---

# Healthcare Computerized Maintenance Management System - Reviewing AEM request scenario

Use the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application for reviewing the existing maintenance plan related to a medical device model.

**Important:** Healthcare Computerized Maintenance Management System is now deprecated and no longer supported or available for new activation. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

Scenario: A hospital needs to review the existing maintenance plan for all the MRI devices associated with a medical device model. A device organization contributor who works at the hospital location submits the request form for the alternative equipment maintenance \(AEM\) from the customer service portal of the hospital. The AEM request form shows the medical device models that have been selected to allow alternate maintenance in the form. In the AEM request form, the contributor enters the requester organization, medical device model, and other details, and suggests making changes to the maintenance plan schedule. When a medical device AEM case is created in the ServiceNow instance, the Healthcare CMMS workflow initiates a playbook configured for the medical device AEM cases. The case gets assigned to a clinical engineer who acts as a fulfiller with the sn\_hcls\_cmms.clinical\_engineer role.

1.  Uses the Workspace to view the medical device AEM case.
2.  In Workspace, views the complete information about the medical device model and AEM request details from the **Details** tab.
3.  Selects the **Playbook** tab to view all the necessary case-related information.

    The layout of a playbook enables clinical engineers to focus on the steps they’re responsible for, while providing full visibility into the end-to-end process life cycle.

4.  Reviews the AEM request details and submits the AEM request for approval.
5.  After the changes to the AEM request are approved, removes the medical device model from the existing maintenance plan.
6.  Adds a new plan with the updated maintenance schedule.
7.  Ensures that all AEM request tasks are set to complete in the playbook and closes the medical device AEM case.

