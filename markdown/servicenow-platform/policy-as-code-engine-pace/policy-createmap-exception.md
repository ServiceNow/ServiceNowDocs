---
title: Request exception for a policy
description: After a policy has been enabled and configured for exceptions, you can map a policy to a deployable and request an exception.
locale: en-US
release: australia
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Policy exceptions, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Request exception for a policy

After a policy has been enabled and configured for exceptions, you can map a policy to a deployable and request an exception.

## Before you begin

Role required: sn\_pace.admin

## Procedure

1.  Navigate to the Mappings page.

    ![Request an exception to a policy.](../image/pace-request-exception-1.jpg)

2.  Select a mapping from the list and click **Request exception.**.

3.  In the Request policy exception window, specify the following:

    -   Reason for exception: Select a reason for the exception from the drop-down list. Refer to the Governance, Risk, and Compliance for details.
    -   Business justification: Enter a business justification for the exception.
    -   Start and End Date: Specify the period for which the exception should be valid. The default validity period is 30 days. The default period can be modified by the Compliance administrator \(sn\_compliance.admin\).

        **Note:**

        -   You can also specify a Start Date that is in the future.
        -   When the request is approved, the sn\_compliance.admin can override the requested dates.
4.  Click **Request** and navigate to the **Exceptions** tab to view the requested exceptions.

    You can see that the exception status is **Pending**. The Compliance Manager assesses this exception request and can choose to approve or reject the request. See [Policy as Code Engine for Preventive compliance management](https://www.servicenow.com/docs/access?context=preventive-compliance-pace&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US) for details. For each exception request, the following details are displayed:

    -   Exception ID: Click the Exception ID to view detailed information about the exception request.
    -   Deployable: Click the link to view the details of the deployable mapped to the policy.
    -   Exception active: If the exception has been granted, the status is set to **Yes**.

        **Note:** If the exception has been granted for a future date, the status is set to **No** until the effective Start Date.

    -   Status: The status of the request:
        -   Pending: An exception request has been created but has not been approved.
        -   Granted: The exception request has been approved.
        -   Extension Pending: An extension request for a granted exception has been created.
        -   Extension Granted: The extension request has been approved.
        -   Declined: The exception request was not approved.
        -   Extension Declined: The request to extend a granted exception was declined.
        -   Expired: The period for which the exception was granted has expired.
        -   Withdrawn: The granted exception request is withdrawn.
    -   Expires in: The number of days after which the exception request expires.
5.  After the request is approved, navigate to the **Exceptions** tab.

    You can see that the exception request status has changed to **Granted**. You can also see the number of days and minutes for which the exception is valid.

6.  After an exception has been granted, you can request an extension before the end of the validity period.

7.  Select a request with a **Granted** status and click **Extend**.

    **Note:** You can request an extension for only one policy at a time.

8.  In the Request extension window, specify a business justification, an end date for the request and click **Request**.

9.  Navigate to the **Exceptions** tab.

    The exception status has changed to **Extension Pending**. The sn\_compliance.admin assesses this extension request and can choose to approve or reject the request. See Governance, Risk, and Compliance for details.

10. After the request is approved, navigate to the **Exceptions** tab.

    You can see that the exception request status has changed to **Extension Granted**. You can also see the number of days for which the extension is valid.

    **Note:** When you execute a policy with exceptions, it is validated and returns a **Compliant-exception** result.


