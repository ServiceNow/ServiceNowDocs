---
title: Configure terms of use attestation
description: Configure attestation terms that employees must accept before accessing Employee Slate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/eslate-configure-terms-of-use.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 1
keywords: [Employee Slate, terms of use, attestation]
breadcrumb: [Employee Slate home, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure terms of use attestation

Configure attestation terms that employees must accept before accessing Employee Slate.

## Before you begin

You must have Moveworks administrator.

Role required: Moveworks setup admin.

## About this task

Require users to accept attestation terms to use the feature and functionality across supported channels. You can define multiple segments to present different terms to different user groups.

-   Supports adherence to organizational policies and regulations.
-   Creates an audit trail of user acknowledgment.
-   Reduces liability through transparency and user awareness of terms and conditions.
-   Supports governance requirements for access to organizational resources.

**Note:** Navigate to Moveworks Setup

## Procedure

1.  From the Moveworks setup, navigate to **Organization Details** &gt; **Tenant Settings** &gt; **General Information** &gt; **Terms of Use**.

2.  Select the **Enable Terms of Use Experience** check box.

    **Warning:** After you enable this configuration, new users cannot use the product on any supported channel until they accept the terms. New users see a prompt on the web asking them to agree to the terms.

    The Terms of Use configuration options appear.

3.  Under **Define Segments**, select **Add new segment**.

    A segment lets you configure a distinct set of terms of use for a specific group of users.

4.  In the **Define segment label** field, enter a title for the attestation form, for example, specify `Employee Terms v1`.

    This label helps you identify the segment in the configuration interface.

5.  In the **Specify the terms of use language** field, enter the main body content in plain text or HTML containing the attestation terms.

6.  In the **Define the user group** field, enter a DSL rule to target this segment to a specific set of users.

    Use DSL expressions to define user groups based on attributes such as department, location, or role. A rule of `FALSE` means the segment does not target any users.

7.  Repeat the previous steps to define additional segments for different user groups.


## Result

After you enable this configuration, employees must accept the terms of use matching their assigned segment. For the employee acceptance experience, see [Accept AI terms and conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/empworks-accept-terms-attestation.md).

