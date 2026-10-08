---
title: Configuring the HRBP productivity assistant
description: Plan and configure your implementation of the HRBP productivity assistant. Complete the tasks to install the app, activate skills, assign roles, define the employees each HR business partner covers, and set up urgency rules and the weekly digest.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/hrbp-pa-configure.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [configure]
breadcrumb: [HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# Configuring the HRBP productivity assistant

Plan and configure your implementation of the HRBP productivity assistant. Complete the tasks to install the app, activate skills, assign roles, define the employees each HR business partner covers, and set up urgency rules and the weekly digest.

## Prerequisite applications

Install and configure these applications before you configure the HRBP productivity assistant.

-   **[EmployeeWorks Web App](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/employee-experience-foundation/empworks-set-up-moveworks.md)**

    HR business partners use the HRBP productivity assistant in the EmployeeWorks Web App.

-   **[ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)**

    Provides the conversational AI that HR business partners use to interact with the HRBP productivity assistant. It also provides the HR Case Enrichment skill, which runs the enrichment process on HR cases.

-   **[Human Resources Scoped App: Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/configuring-ckm.md)**

    Provides Case and Knowledge Management, which generates the HR case records that the assistant uses.


**Note:** The HRBP productivity assistant requires HRSD Advanced licensing. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Configuration overview

Complete these tasks in the following order:

1.  [Set up OAuth access](https://docs.moveworks.com/service-management/access-requirements/ticketing-systems-and-itsms/servicenow-access-requirements#setting-up-oauth-access)

    Connect your Moveworks instance to your ServiceNow instance.

2.  [Install HRBP Productivity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/install-hrbp-sa.md)

    Install the HRBP Productivity app on your instance.

3.  [Activate HRBP skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/activate-hrbp-skills.md)

    Activate the HR Case Enrichment skill and, optionally, the HR Case Summarization skill in AI Admin Hub.

4.  [Assign HRBP roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/create-hrbp-sa-user.md)

    Assign the HRBP roles to your administrators and HR business partners, and assign the roles that give HR business partners access to HR data.

5.  [Define HRBP data access and data access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)

    Define the employees that each HR business partner covers. HR cases for those employees are assigned to the HR business partners you define in the data access record.

6.  [Configure HRBP urgency rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/configure-hrbp-urgency.md)

    Define condition-based and prompt-based rules that set a minimum urgency for HR cases that trigger each rule.

7.  [Configure the HRBP productivity assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/configure-hrbp-pa.md)

    Set the system property that links the button in the weekly digest and critical urgency notifications to the HRBP productivity assistant.

8.  [Configure the HRBP weekly digest](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/configure-hrbp-weekly-digest.md)

    Review the scheduled job that sends each HR business partner a weekly summary of their open cases.


## Roles required to configure the HRBP productivity assistant

The HRBP Productivity app includes the following roles:

-   **HRBP administrator \[sn\_hrbp\_hub.admin\]**

    Configures the HRBP productivity assistant, including data access records, rules, assignments, system properties, and the weekly digest. This role contains the sn\_hrbp\_hub.user role, which allows administrators to access the HR business partner pages.

-   **HRBP user \[sn\_hrbp\_hub.user\]**

    Accesses the HR business partner pages in the EmployeeWorks Web App. Only users with this role can be assigned HR cases through data access records and receive the weekly digest. Assign this role to your HR business partners.


