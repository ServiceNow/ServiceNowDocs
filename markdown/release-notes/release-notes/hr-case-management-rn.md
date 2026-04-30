---
title: Case and Knowledge Management release notes
description: The ServiceNow Case and Knowledge Management application enables you to standardize the documentation, interaction, and fulfillment of employee inquiries and requests, which helps to improve HR efficiency and services over time. Case and Knowledge Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Case and Knowledge Management release notes

The ServiceNow® Case and Knowledge Management application enables you to standardize the documentation, interaction, and fulfillment of employee inquiries and requests, which helps to improve HR efficiency and services over time. Case and Knowledge Management was enhanced and updated in the Xanadu release.

## Case and Knowledge Management highlights for the Xanadu release

-   Use the new HR guided setup that supports domain separation at the global and at the parent or child levels.
-   HR Document Templates is being deprecated and is no longer available for use. You can use the ServiceNow Document Templates application instead of HR Document Templates.

See [Case and Knowledge Management](https://www.servicenow.com/docs/access?context=case-knowledge-management-landing-page&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Guided setup for HR Service Delivery](https://www.servicenow.com/docs/access?context=guided-set-up-hr&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    Run the guided setup for each domain within HR Service Delivery. Prior to the Xanadu release, you could run the guided setup at the global domain only.

-   **Workflow to Workflow Studio migration**

    Because of the enhanced features in Workflow Studio, the HR Service Activities, HR Case User Acceptance, HR Case Approval subflows have been migrated from Workflow to Workflow Studio. As an HR administrator, you can configure the **sn\_hr\_core.deprecated\_workflows** system property to decide whether to run a legacy workflow or corresponding flow in Workflow Studio.

-   **Zero Trust Access \(ZTA\) for HR Service Delivery**

    Enable an administrator to configure in-time access with the dynamic role relegation feature. Based on different criteria such as the IP address, location, device, or time, the administrator can craft policies to permit only a certain subset of the user's original roles in the session.


## Deprecations

Starting with the Xanadu release, HR Document Templates is being prepared for deprecation. HR Document Templates is hidden and is no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. You can use the ServiceNow Document Templates application instead of HR Document templates.

## Activation information

Case and Knowledge Management is a ServiceNow AI Platform feature that is available with activation of the Human Resources Scoped App: Core \[com.sn\_hr\_core\].

## Related ServiceNow applications and features

-   **[Agent Workspace for HR Case Management \(Configurable\)](https://www.servicenow.com/docs/access?context=agent-ws-hr-case-mgmt-landing-page&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    The ServiceNow® Agent Workspace for HR Case Management application enables you to interact with employees, respond to inquiries, and resolve issues quickly.


**Parent Topic:**[HR Service Delivery release notes](hr-service-delivery-landing.md)

