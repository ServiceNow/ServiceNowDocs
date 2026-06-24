---
title: Configuring playbooks to set medical devices out-of-service
description: You can configure a playbook to provide step-by-step guidance to set medical devices out-of-service in the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/cmms-config-playbook-retiring-medical-device.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure medical device out-of-service, Configure, Healthcare Computerized Maintenance Management System, Clinical Device Management, Healthcare and Life Sciences]
---

# Configuring playbooks to set medical devices out-of-service

You can configure a playbook to provide step-by-step guidance to set medical devices out-of-service in the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application.

**Important:** Healthcare Computerized Maintenance Management System is now deprecated and no longer supported or available for new activation. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/clinical-device-mgmt-overview.md).

As a user with the admin role, you can create a playbook by using Playbooks, a ServiceNow AI Platform® feature. For more information, see [Process Automation Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio/process-automation-designer.md).

The playbooks in the Healthcare CMMS application use the CSM Configurable Workspace playbook experience. By default, the Healthcare CMMS application includes the playbook for medical device out-of-service to assist clinical engineers to resolve medical device out-of-service cases.

Configure a playbook by navigating to **All** &gt; **Process Automation** &gt; **Process Automation Designer**. You can either select an existing process definition or create a new process definition for the playbook associated with the medical device cases. For more information, see [Process definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio/process-definitions.md).

**Note:** When configuring a process definition for the playbook associated with medical device out-of-service cases, ensure that the application scope is set to Healthcare Computerized Maintenance Management System using the application picker. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/building-applications/c_ApplicationPicker.md).

