---
title: Set up the account onboarding playbook
description: Use the account onboarding playbook to import, stage, manage, and publish account data.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Account onboarding, Configure, Customer Success Management]
---

# Set up the account onboarding playbook

Use the account onboarding playbook to import, stage, manage, and publish account data.

**Note:** Some features in the account onboarding playbook aren’t working correctly. To address this issue, you must install the latest version of the playbook from the ServiceNow Store. For more details on the issues, see [KB1651378](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=79e2c24e4763ca1077748d01426d4319).

An account boarding case is created in two ways:

-   **Automatically**: When a new customer account is created, the **Creation of account onboarding case** flow is triggered, and an onboarding case is automatically generated. This trigger condition is optional and can be customized based on your requirements. You can configure playbook tasks that include identifying key team members, data import setup, and create collaborative activities.
-   **Manually**: For existing customer accounts that are being onboarded in a phased manner, you can create additional onboarding cases from the **List** view. See [Create an account onboarding case](../task/account-lifecycle-create-case.md) for details.

When you open the account onboarding case, you’re directed to the first activity in the Initial setup stage. While working on the activities, you can view:

-   The entire playbook process in the horizontal stage picker.
-   The activities in the current stage in the stacked playbook activity view.
-   Related items, activity stream, and recommended actions in the contextual side panel. Select the links in the Related items card to navigate to the record page.

The Customer Success Management playbook includes the following stages and activities that can be used in the account onboarding process.

-   [Initial setup](account-lifecycle-use-playbook-initiate.md)
-   [Data capture and validation](account-lifecycle-use-playbook-data-capture.md)
-   [Development and automation](account-lifecycle-use-playbook-development.md)
-   [Testing and training](account-lifecycle-use-playbook-test-golive.md)
-   Go-live/Post Support

-   **[Create an account onboarding case](../task/account-lifecycle-create-case.md)**  
Create an onboarding case for an existing customer account.
-   **[Initial setup](account-lifecycle-use-playbook-initiate.md)**  
This phase is meant to gather the initial information required onboard a customer. For example, gathering core information like onboarding manager name, key customer contact, internal and external stakeholders, their responsibilities, and so on.
-   **[Data capture and validation](account-lifecycle-use-playbook-data-capture.md)**  
This phase is meant to gather the necessary information about the account such as support contacts, locations, sold products, entitlements.
-   **[Development and automation](account-lifecycle-use-playbook-development.md)**  
This phase is used to track and complete critical activities including account relationship management, maintenance scheduling, Service Level Agreement \(SLA\) definition, and Service Exchange installation \(when required\).
-   **[Testing and training](account-lifecycle-use-playbook-test-golive.md)**  
These phases are designed to involve customers in testing and confirm that they have received adequate training before the go-live date.
-   **[Close or cancel an account onboarding case](../task/account-lifecycle-cancel-case.md)**  
You can close or cancel an account boarding case and all the related activities.

**Parent Topic:**[Account onboarding](account-lifecycle-configure.md)

