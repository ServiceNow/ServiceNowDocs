---
title: Plan your Password Reset processes
description: To ensure security and efficiency, take the time to plan your Password Reset implementation.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Plan your Password Reset processes

To ensure security and efficiency, take the time to plan your Password Reset implementation.

## Before you begin

Role required: password\_reset\_admin or admin

## Procedure

1.  Decide on the password reset process:

    -   **Self-service process:** Users reset their password over the Internet using a browser on any supported interface, including mobile devices. To make the Password Reset application with Orchestration available to all users publicly, create a new Password Reset process only for this purpose and make it accessible to all users by setting the **Public access** property. See [Example: The default self-service Password Reset process](https://www.servicenow.com/docs/access?context=c_SelfServicePasswordReset&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
    -   **Service desk-assisted process:** Users reset passwords by requesting the assistance of a service desk agent, over the phone or in person. Only service desk agents with the password\_reset\_service\_desk role can reset user passwords. Watch the videos: [Resetting User Passwords \(Video\)](https://www.youtube.com/watch?v=CokNL8aw6hA) and [How to Set Up a Service Desk-Assisted Password Reset Process \(Video\)](https://www.youtube.com/watch?v=6VbPR7CWF0M).
2.  Decide how groups and roles differ in access and security needs.

    Analyze and assess how members of each group in your organization access the system. For example, if members of the sales group primarily access the system remotely, consider using a stronger method or multiple methods to verify the identity of each user.

    Identify user roles that have access to critical information and resources. For example, stronger verifications might be required for roles that have access to employee data, accounting information, or network configurations.

    Based on your analysis of groups and roles, determine the number and variety of verifications needed for the different Password Reset processes.

3.  Decide how to manage credentials.

    Determine whether single sign-on is enabled with the type of directory service or other credential store used. If the directory service is configured for single sign-on, consider increasing the level of security by using multiple methods to verify identity of a user. A compromised user name and password can easily allow access to associated systems in a single sign-on environment.

4.  Decide how to implement enrollment in the Password Reset program.

    For example, will enrollment be optional or required? Will users be auto-enrolled? How will users be notified to enroll in the program? The answers to these questions will help you determine the appropriate verification types to use.

5.  Decide which Password Reset options to offer to users.

    -   If your organization uses single sign-on, how will users reset their password if they are unable to log on?
    -   What options are available to users working off-site?

**Parent Topic:**[Configuring Password Reset](../concept/password-reset-admin-guide.md)

**Related topics**  


[Configure your Password Reset process](t_CreateAPasswordResetProcess.md)

