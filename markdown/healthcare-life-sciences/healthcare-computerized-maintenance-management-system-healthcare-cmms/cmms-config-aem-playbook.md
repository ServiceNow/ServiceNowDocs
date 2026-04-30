---
title: Configuring playbooks for reviewing AEM requests for medical devices
description: Configure a playbook to provide step-by-step guidance for resolving medical device cases for reviewing alternative equipment maintenance \(AEM\) requests in the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application.
locale: en-US
release: yokohama
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Healthcare CMMS for the review of AEM requests, Configuring Healthcare CMMS, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Configuring playbooks for reviewing AEM requests for medical devices

Configure a playbook to provide step-by-step guidance for resolving medical device cases for reviewing alternative equipment maintenance \(AEM\) requests in the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

As a user with the admin role, you can create a playbook by using Playbooks, a ServiceNow AI Platform® feature. For more information, see [Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

The playbooks in the Healthcare CMMS application use the CSM Configurable Workspace playbook experience. By default, the Healthcare CMMS application includes the playbook for reviewing AEM requests for medical device models and its devices to assist clinical engineers to resolve medical device AEM cases.

Configure a playbook by navigating to **All** &gt; **Process Automation** &gt; **Process Automation Designer**. You can either select an existing process definition or create a new process definition for the playbook associated with the medical device cases. For more information, see [Process definitions](https://www.servicenow.com/docs/access?context=process-definitions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Note:** When configuring a process definition for the playbook associated with medical device AEM cases, ensure that the application scope is set to Healthcare Computerized Maintenance Management System using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

