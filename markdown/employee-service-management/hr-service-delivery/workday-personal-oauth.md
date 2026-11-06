---
title: Enable personal OAuth for a Workday HR use case
description: Enable personal OAuth for a Workday use case so that it runs under the signed-in user’s identity and Workday permissions instead of the shared integration account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/hr-service-delivery/workday-personal-oauth.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 1
breadcrumb: [Configuring, HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Enable personal OAuth for a Workday HR use case

Enable personal OAuth for a Workday use case so that it runs under the signed-in user’s identity and Workday permissions instead of the shared integration account.

## Before you begin

Role required: admin

## About this task

With personal OAuth, a use case runs under the identity of the signed-in user. Workday applies that user’s own roles and permissions, so users see or change only what they are authorized to access. Every action is also recorded in Workday under the real user. By default, every use case runs through the existing system connection, which authenticates with a shared integration account. Nothing changes until you enable personal OAuth for a use case.

**Note:** Create a separate connection alias for personal OAuth rather than modifying the existing one. Changing the existing alias breaks REST integrations that depend on it, such as scheduled imports.

The following use cases support personal OAuth:

-   Workday HR - Get Time Off Balance
-   Workday HR - Request Time Off
-   Workday HR - Look Up Worker Profile
-   Workday HR - Get User Compensation Details
-   Workday HR - Get Employee Payslip
-   Workday HR - Look up Time off and Leave of Absence Details
-   Workday HR - Get Look up Direct Reportees Information
-   Workday HR - Update Personal Details
-   Workday HR - Get Total Rewards
-   Workday HR - Approve Reject Request

## Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credentials**.

2.  Select **WorkdayHR**.

3.  Select the **Child Aliases** tab.

4.  Select **New**.

5.  Enter the name for your child alias and select **Submit**.

6.  Select your child alias record.

7.  Select **Create New Connection &amp; Credential** related link.

8.  On the form, fill in the fields.

    For more information, see [Create connection and credential form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/hr-service-delivery/cereate-connection-and-cred-form.md).

9.  Select **Create and Get OAuth Token**.

10. Select the credential record for your child alias.

11. In the **Integration Type** field, select **Personal**.

12. Select **Get OAuth Token**.

13. Select **Update**.

14. Enable personal OAuth for your use case.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Select **Use case Connection Alias Mapping** table.

    3.  Select **Show List** related link.

    4.  Select the **Description** field for your use case.

    5.  Select the lookup using list icon\[Omitted image "magnifying-glass.png"\] Alt text: beside the **Connection Alias** field.

    6.  Select the ID for your child alias.

    7.  Select **Update**.


