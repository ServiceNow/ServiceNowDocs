---
title: Approve restricted caller access privileges for Healthcare and Life Sciences Service Management
description: Approve restricted caller access \(RCA\) privileges for accessing document templates from the Healthcare and Life Sciences Service Management applications.Allow restricted caller access \(RCA\) privileges for the Document Templates application in the target scope to access document templates from a Healthcare and Life Sciences Service Management application.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Approve restricted caller access privileges for Healthcare and Life Sciences Service Management

Approve restricted caller access \(RCA\) privileges for accessing document templates from the Healthcare and Life Sciences Service Management applications.

RCA privileges define cross-scope access to an application, an event, or an application resource. Application resources include access control roles, business rules, UI actions, and script includes.

The real and requested RCAs required for accessing document templates from a Healthcare and Life Sciences Service Management application are included within the Healthcare and Life Sciences Service Management Core application.

When you install a Healthcare and Life Sciences Service Management application, the status of Real RCAs of the Document Templates application are set to **Requested**. For more information, see [Requested restricted caller access \(RCA\)](https://www.servicenow.com/docs/access?context=requested-rca&version=australia&pubname=australia-application-development&ft:locale=en-US).

To be able to use document templates in a Healthcare and Life Sciences Service Management application, as an administrator, you must set the status of Real RCAs of the Document Templates application to **Allowed**. For more information, see [Allow a restricted caller access privilege for document templates in Healthcare and Life Sciences Service Management Core](hcls-approving-rca.md#).

## Allow a restricted caller access privilege for document templates in Healthcare and Life Sciences Service Management Core

Allow restricted caller access \(RCA\) privileges for the Document Templates application in the target scope to access document templates from a Healthcare and Life Sciences Service Management application.

### Before you begin

Ensure that the application scope is set to Document Templates in the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access**.

2.  In the **Source Scope** column of the Restricted Caller Access Privileges list, search for the **Healthcare and Life Sciences Service Management Core**.

3.  Click a requested RCA with the **Document Templates** target scope.

4.  On the Restricted Caller Access Privilege form, set the **Status** field value to **Allowed**.

5.  Click **Update**.

6.  Repeat steps 3 through to 5 for each requested RCA.


