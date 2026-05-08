---
title: Asynchronous password reset subflow
description: When a user requests a password reset, based on the application for which the password reset is requested, the process works either synchronously or asynchronously.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customizing Password Reset processes, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Asynchronous password reset subflow

When a user requests a password reset, based on the application for which the password reset is requested, the process works either synchronously or asynchronously.

When a user requests a password reset for a credential store for which the REST APIs are available to reset the password, the password is reset immediately. This process is synchronous.

In the asynchronous process, when a user requests a password reset for credential stores that don't provide REST APIs, you can configure such credential stores to reset passwords using an external system, such as Robotic Process Automation.

For more information about Robotic Process Automation, see Robotic Process Automation \(RPA\) Hub.

When a user requests a password reset, the password doesn't get reset immediately. The user receives a message that shows the request has been submitted, and the request status is displayed as **Pending With External System** on the Password Reset Requests page for that request.

When the process completes, the password is reset. The user receives an appropriate message based on the success or failure of the password reset action from the external system, which resets a password for the user. If the password reset is successful, the user receives an email containing the new password from the external system if the credential store doesn’t accept the password.

If a credential store processes a password reset request asynchronously, then to update the corresponding password reset request status from pending to either **Completed With Success** or **Completed With Failure**, the process must use the **Update Password Reset Request** subflow as a callback.

**Note:** To open the **Update Password Reset Request Status** subflow, navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**, and click the **Subflows** tab. Then search for and select the **Update Password Reset Request Status** subflow.

|Input Parameters|Description|
|----------------|-----------|
|Password Reset Request|Glide record of the password reset request.|
|Request Status|Determines which choices are available as input. For example, **Completed With Success** or **Completed With Failure**.|

When this subflow is used, the input parameters are considered in this subflow to set the corresponding password reset status.

![Update Password Reset Request Status subflow.](../image/update-password-reset-subflow.png "Update Password Reset Request Status subflow")

**Parent Topic:**[Customizing Password Reset processes](../concept/customizing-password-reset.md)

