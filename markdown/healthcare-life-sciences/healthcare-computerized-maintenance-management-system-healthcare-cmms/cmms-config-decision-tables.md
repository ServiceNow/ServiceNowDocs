---
title: Configuring the approval process of AEM requests
description: You can define the conditions for approval of changes to the current maintenance plan for a medical device model associated with a medical device AEM case.
locale: en-US
release: zurich
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure AEM request review, Configure, Healthcare Computerized Maintenance Management System, Clinical Device Management, Healthcare and Life Sciences]
---

# Configuring the approval process of AEM requests

You can define the conditions for approval of changes to the current maintenance plan for a medical device model associated with a medical device AEM case.

**Important:** Healthcare Computerized Maintenance Management System is now deprecated and no longer supported or available for new activation. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

As a user with the admin role, you can configure decision tables to initiate the approval workflow for an alternative equipment maintenance \(AEM\) request when the decision condition is satisfied for a medical device AEM case. For example, as part of the maintenance plan scheduling process, you can define conditions to send the AEM request for approval to specific users for reviewing and approving the plan when the state of the medical device AEM is set to **Review in progress**.

You configure decision tables for medical device AEM cases by navigating to **All** &gt; **System Definition** &gt; **Decision Tables**. When configuring decision tables for medical device AEM cases, associate the column in the Medical device case \[sn\_hcls\_cmms\_case\] table as a decision input. By default, the Medical device AEM approval decision table is available within the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application to configure the decision conditions for the approval of AEM requests.

The **Trigger medical device AEM approval** business rule runs when a clinical engineer selects **Request approval** during the review of an AEM request in the playbook. The business rule triggers the approval workflow, if available, for the AEM review. When the decision conditions are satisfied, the approval request is sent to all the approvers. If no approval workflow is available, the AEM request is automatically approved.

**Note:** When configuring the decision approval flow using the Workflow Studio feature, make sure that the **Approval** field configured for the Medical device case \[sn\_hcls\_cmms\_case\] table is set to **Approval** for the last level of the approval action only. For more information, see [Ask for Approval step](https://www.servicenow.com/docs/access?context=ask-approval-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

To learn more, see [Decision Tables](https://www.servicenow.com/docs/access?context=decision-table&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

