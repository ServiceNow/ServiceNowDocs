---
title: Business roles
description: Business roles enable you to automatically provision applications to employees through licensed identity provider \(IDP\) services. If you are subscribed to HR Service Delivery, preconfigured integrations for select systems may be available to use.
locale: en-US
release: australia
product: Employee Journey Management
classification: employee-journey-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Lifecyle events for enterprise, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Business roles

Business roles enable you to automatically provision applications to employees through licensed identity provider \(IDP\) services. If you are subscribed to HR Service Delivery, preconfigured integrations for select systems may be available to use.

## Preconfigured integrations for new hire onboarding

The following integrations are available to use with new hire onboarding. These integrations require subscriptions to the relevant spoke in IntegrationHub, as well as the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

**Note:** The lifecycle event for new hire onboarding is included as demo data with the Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

-   [Okta integration for new hire onboarding](integrating-with-okta-service.md)
-   [Microsoft Entra ID integration for new hire onboarding](azure-active-directory-integration-for-new-hire-onboarding.md)

## Activation information

The Business Roles \[com.snc.businessroles\] plugin is automatically activated with the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

-   **[Configure a business role](../task/configure-business-role.md)**  
Create or modify a business role based on job function, geography, and so on.
-   **[Update the assign\_business\_roles\_catalog system property](../task/update-assign-business-roles-catalog-item-system-property.md)**  
The **assign\_business\_roles\_catalog** system property enables you to assign business roles to users through a catalog item as part of a lifecycle event, and is included with the Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin. If you are using a custom catalog item with your lifecycle event, you must update the system property with the sys id of that item.

**Parent Topic:**[Lifecyle events for enterprise](../reference/enterprise-onboarding-transitions-landing-page.md)

