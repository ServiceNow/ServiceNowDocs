---
title: Clone Target Registration and Authentication
description: A clone target record specifies the instance URL and credentials used for cloning.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-03-24"
reading_time_minutes: 1
breadcrumb: [Request a clone, System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Clone Target Registration and Authentication

A clone target record specifies the instance URL and credentials used for cloning.

## Before you begin

-   Provide credentials for the target instance for a user with the admin role. Use a local, user account, not an LDAP or SSO user account. The target instance credentials must exist in the User \[sys\_user\] table as a user record or as part of an LDAP integration. Clone requests cannot redirect authentication requests to a single sign-on identity provider.
-   Verify the system property **glide.db.clone.allow\_clone\_target** is set to **True**. By default, this property is enabled on instances whose name ends in Dev, Test, Stage, UAT, or QA.
-   If the target instance uses [IP range based authentication](https://www.servicenow.com/docs/access?context=c_IPRangeBasedAuthentication&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), it must allow the IP range 10.0.0.0/10.255.255.255 to communicate on a local network.
-   Role required: clone\_admin or admin.

## Procedure

1.  Navigate to **All** &gt; **System Clone** &gt; **Clone Targets**.

2.  Click **New**.

3.  Enter the URL for the receiving instance \(target\).

    The system validates the instance allows clone targets and that High Availability Cloning is active. Production and demonstration instances fail these validation checks.

    ![Clone target error message](../image/CloneTargetInvalid.png "Clone target invalid")

4.  Enter the basic authentication credentials for a user account with the admin role on the target instance.

    ![Clone target](../image/CloneTarget.png)

    **Note:** You cannot request cloning multiple targets from the same source. Instead, make a separate request for each target.

    The system validates the user credentials have admin access to the target instance.

5.  Click **Submit**.

    The system checks connectivity and validates the user credentials against the target instance.


