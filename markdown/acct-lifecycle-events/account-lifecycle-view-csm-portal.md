---
title: View account onboarding cases in the CSM portal
description: View the account onboarding case records or case task records on the Customer Service Management \(CSM\) portal.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Account onboarding, Use, Customer Success Management]
---

# View account onboarding cases in the CSM portal

View the account onboarding case records or case task records on the Customer Service Management \(CSM\) portal.

## Before you begin

Role required:

-   sn\_acct\_lc\_agent
-   sn\_customerservice\_customer.admin
-   sn\_customerservice\_customer\_manager
-   sn\_customerservice.customer

## Procedure

1.  Use the name and password that you created during the registration process to log in to the Customer Service Portal.

    See [Using the Customer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/use-the-customer-portal.md) for details.

2.  Select **My Lists** to view the account onboarding cases and case tasks.

    Depending on your user role, you can view the following lists:

    -   All Onboarding Cases: Available for users with sn\_acct\_lc\_agent, sn\_customerservice\_customer.admin, and sn\_customerservice\_customer\_manager roles. All onboarding cases related to the account are displayed under the My Lists section.
    -   My Onboarding Cases: Available for users with sn\_acct\_lc\_agent, sn\_customerservice\_customer.admin, sn\_customerservice\_customer\_manager, and sn\_customerservice.customer roles.
    -   My Onboarding Case Tasks: Available for users with sn\_acct\_lc\_agent, sn\_customerservice\_customer.admin, sn\_customerservice\_customer\_manager, and sn\_customerservice.customer roles.
    **Note:**

    When you search for something on the service portal, the search results are shown in separate **Sources**: Onboarding case and Onboarding Case Tasks.

3.  Select the All Onboarding Cases list.

    All the onboarding cases related to the selected account are displayed.

4.  Select an onboarding case in the list.

    **Note:** The Header section for the case and case tasks can be configured and you can add or remove fields as required.

    The following details are displayed for each case.

    -   Header section that provides basic information about the case including account name, go-live date, number of days before go-live date, and status of the onboarding case.
    -   All the onboarding tasks related to the case. Select the task to view additional information such as status, activities, and any attachments.
    -   The left-hand section provides the following details:
        -   General instructions: Provides a short description and a detailed case description. Select **View More** to view all the details related to the case.
        -   Product information: Shows product information only if the **Customer visible** flag is set to True in the account onboarding case playbook.
        -   Shared articles: Shows articles that have been shared with you. Select the article link to view details.
5.  Select an onboarding case task in the list.

    The following details are displayed for each case task:

    -   Header section that provides information about the case task including case number, parent, or onboarding case with which the task is associated, the account name, and status of the task.
    -   The left-hand section provides the following details:
        -   General instructions: Provides a short description and a detailed case description. Select **View More** to view all the details related to the case.
        -   Shared articles: Shows articles that have been shared with you. Select the article link to view details.
    -   All the activities related to the case task are displayed.

**Parent Topic:**[Account onboarding](../concept/account-lifecycle-use.md)

