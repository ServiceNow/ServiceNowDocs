---
title: Set up Customer Service Management integration with Safe Workplace applications
description: Enable the integration with Safe Workplace applications to help contacts or consumers safely enter locations and comply with health and safety policies.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating with Safe Workplace applications, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Set up Customer Service Management integration with Safe Workplace applications

Enable the integration with Safe Workplace applications to help contacts or consumers safely enter locations and comply with health and safety policies.

## Before you begin

Ensure that the Customer Service plugin \(com.sn\_customerservice\) is installed.

If you are supporting business-to-consumer \(B2C\) customers, ensure that the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) is installed.

Role required: admin

## Procedure

1.  [Install Employee Health Screening](https://www.servicenow.com/docs/access?context=install-emp-health-screening&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

2.  Give external users access to the Health Verification form.

    For more information, see the [Allow external users access to "Health Verification" catalog item \[KB0856301\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0856301) article in the HI Knowledge Base.

3.  Assign the sn\_imt\_monitoring.monitoring\_user role to a customer or consumer service agent.

4.  [Configure the health screening form](configure-record-producer-csm-safe-workplace.md).

5.  Create relationships to show health screening information on Agent Workspace.

6.  [Customize the Consumer or Customer Service Portal](customize-csp-csm-portals.md) to display a link to the Health Verification form in the portal header menu.


