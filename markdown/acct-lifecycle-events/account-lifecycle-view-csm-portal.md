---
title: View account onboarding cases in the Consumer Service Portal
description: View Account Lifecycle Events onboarding case records or case task records on the Customer Service Management \(CSM\) portal.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using account onboarding, Account onboarding, Account Lifecycle Events]
---

# View account onboarding cases in the Consumer Service Portal

View Account Lifecycle Events onboarding case records or case task records on the Customer Service Management \(CSM\) portal.

## Before you begin

Role required:

-   sn\_acct\_lc\_agent
-   sn\_customerservice\_customer.admin
-   sn\_customerservice\_case\_manager
-   sn\_customerservice.customer

## Procedure

1.  Use the name and password that you created during the registration process to log in to the Consumer Service Portal.

    See [Using the Consumer Service Portal](https://www.servicenow.com/docs/access?context=use-consumer-service-portal&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) for details.

2.  Click **My Lists** to view the account onboarding cases and case tasks.

    Both internal and external users can view the onboarding cases in the consumer service portal. The case list is filtered based on the user type and the role.

    -   Internal users: When an internal user logs in with the **sn\_acct\_lc.agent** role, the filter is set to the **Assigned to** field and the lists are filtered as follows.
        -   All Onboarding Cases: All onboarding cases present in the system are displayed.
        -   My Onboarding Cases and Case Tasks: All onboarding cases and case tasks assigned to the logged in user are displayed.
    -   External users: When an external user logs in, the filter is set to the **Contact** field and the lists are filtered as follows:
        -   For users with the **sn\_customerservice.customer\_case\_manager** role, the lists are filtered as follows:
            -   All Onboarding Cases: All onboarding cases associated with the account managed by the logged in user are displayed.
            -   My Onboarding Cases and Case Tasks: All onboarding cases and case tasks assigned to the logged in user are displayed.
        -   Users with the **sn\_customerservice.customer role**: Can view cases and case tasks to assigned to the logged in user in the My Onboarding Cases and My Onboarding Case Tasks lists.
3.  Click on the **All Onboarding Cases** list.

    All the onboarding cases related to the selected account are displayed.

4.  Click on an onboarding case in the list.

    **Note:** The Header section for the case and case tasks can be configured and you can add or remove fields as required.

    The following details are displayed for each case.

    -   Header section that provides basic information about the case including account name, go-live date, number of days before go-live date, and status of the onboarding case.
    -   All the onboarding tasks related to the case. Click on the task to view additional information such as status, activities, and any attachments.
    -   The left hand section provides the following details:
        -   General instructions: Provides short description and a detailed case description. Click **View More** to view all the details related to the case.
        -   Product information: Shows product information only if the **Customer visible** flag is set to True in the account onboarding case playbook.
        -   Shared articles: Shows articles that have been shared with you. Click on the article link to view details.
5.  Click on an onboarding case task in the list.

    The following details are displayed for each case task:

    -   Header section that provides information about the case task including case number, parent or onboarding case with which the task is associated, the account name, and status of the task.
    -   The left hand section provides the following details:
        -   General instructions: Provides short description and a detailed case description. Click **View More** to view all the details related to the case.
        -   Shared articles: Displays articles that logged in users have access to. Click on the article link to view details.
    -   All the activities related to the case task are displayed.

