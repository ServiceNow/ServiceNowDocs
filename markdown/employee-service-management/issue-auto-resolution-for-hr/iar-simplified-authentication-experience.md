---
title: Simplifying the authentication experience for your remote employees
description: With the Issue Auto Resolution application, you can simplify the authentication experience for your remote employees. Instead of entering a user name and password to access the service portal, your remote employees can get to the portal through a link in a short messaging service \(SMS\) or email.
locale: en-US
release: australia
product: Issue Auto Resolution for HR
classification: issue-auto-resolution-for-hr
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Issue Auto Resolution for HR, HR Service Delivery, Employee Service Management]
---

# Simplifying the authentication experience for your remote employees

With the Issue Auto Resolution application, you can simplify the authentication experience for your remote employees. Instead of entering a user name and password to access the service portal, your remote employees can get to the portal through a link in a short messaging service \(SMS\) or email.

By using the Issue Auto Resolution application, your remote employees who don't have the corporate credentials can still access your service portal without entering a user name and password. When you create a case for the employee, that employee gets a link through a text \(SMS\) or email. That link directs them to the login page where they’re prompted to enter a user name and password. With this simplified authentication experience feature, these employees, who fulfill the user criteria mentioned in the **sn\_iar\_hr.digest\_link\_user\_criteria** system property, can access the portal without entering credentials.

You can install the Time Limited Authentication \(com.snc.authenticate.time\_limited\_authentication\) plugin to extend the core functionality of the Issue Auto Resolution application.

## Successful and simplified login experience

Let's say that a remote employee recently joined your organization. Your employee doesn't have the corporate credentials to access the service portal but that employee has a query about the dental benefits enrollment. With the Issue Auto Resolution application, your employee can access the service portal through an email by using a personal device.

The following example shows how a remote employee can log in to the portal without credentials by using a digest link.



The process is as follows:

1.  The remote employee gets the digest link through an email.
2.  The link directs the employee to verify the identity page, where the employee has to enter a one-time password \(OTP\) received through an email.
3.  The employee is then directed to the standard ticket page, where the employee can view the recommendations.

    **Note:** The link’s validity depends on the values that are defined in the time-limited authentication configuration record. In this case, the maximum number of times an employee can use the link is set to one.

4.  The employee is redirected to the expired link page when the employee tries to use the same link again.
5.  The employee gets an email with a new digest link.

## Time-limited authentication

You can do the following tasks to set the existing time-limited authentication properties:

-   Enable the time-limited authentication glide.authenticate.enable.time\_limited\_authentication property.
-   Disable the account recovery property.
-   Enable multi-provider single sign-on \(SSO\).
-   Enable the **Active** field in the time limited authentication properties config record.

To learn how to configure the properties, see [Time Limited Authentication Properties form](../reference/iar-time-limited-authentication-properties-form.md).

To learn more about time-limited authentication, see Time limited authentication.

## User criteria for generating the digest link

You can use the sn\_iar\_hr.digest\_link\_user\_criteria system property to get and validate the user criteria for generating the digest link. This link appears in an SMS or email that is sent to the employee. The value should be the sys\_id of the active user criteria. For more information, see [User criteria form](../../universal-request/concept/ur-landing-limitedaccess.md).

Users with the admin and sn\_hr\_core.admin roles can assign the sn\_iar\_hr.digest\_link\_user role. This role is added to the available user criteria to validate if that user qualifies for digest link generation.

