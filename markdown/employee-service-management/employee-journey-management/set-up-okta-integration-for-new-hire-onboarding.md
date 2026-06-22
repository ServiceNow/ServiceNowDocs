---
title: Set up the Okta integration for new hire onboarding
description: To set up the Okta integration for new hire onboarding, you must first set up the Okta spoke v1.1.1, next fetch the Okta groups into your instance, and last configure the required business roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-journey-management/set-up-okta-integration-for-new-hire-onboarding.html
release: zurich
product: Employee Journey Management
classification: employee-journey-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Okta integration for new hire onboarding, Integrate, Lifecyle events for enterprise, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Set up the Okta integration for new hire onboarding

To set up the Okta integration for new hire onboarding, you must first set up the Okta spoke v1.1.1, next fetch the Okta groups into your instance, and last configure the required business roles.

## Before you begin

This integration requires subscriptions to the following:

-   [Okta spoke v1.1.1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integration-hub/okta-v2-spoke.md)
-   Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin

    **Note:** The lifecycle event for new hire onboarding is included as demo data with this plugin.


Role required: admin

## Procedure

1.  Set up the Okta spoke v1.1.1.

    For instructions on how to set up the spoke, see [Set up Okta spoke v1.1.1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integration-hub/set-up-okta-v1.1.1.md).

2.  Fetch the Okta groups into your instance.

    For instructions on how to fetch the groups, see [Fetch Okta groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integration-hub/fetch-okta-groups.md).

    **Important:** If an Okta group is deleted from within the Okta system, that change will not be reflected in your instance. You must manually delete the record by navigating to **Okta Spoke** &gt; **Okta groups**, as well as remove it from any business role mappings.

3.  Configure the required business roles.

    **Note:** The Business Roles \[com.snc.businessroles\] plugin is automatically activated with the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

    For instructions on how to configure the business roles and map them to the relevant groups, see [Configure a business role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-journey-management/configure-business-role.md).


**Parent Topic:**[Okta integration for new hire onboarding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-journey-management/integrating-with-okta-service.md)

