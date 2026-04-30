---
title: Setting up cloud user
description: Set the credentials for the cloud user to be able to generate and run tests. This is a one time setup after the admin user installs the application.
locale: en-US
release: xanadu
product: ATF Test Generator and Cloud Runner
classification: atf-test-generator-and-cloud-runner
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ATF Test Generator and Cloud Runner, Extend ServiceNow AI Platform capabilities]
---

# Setting up cloud user

Set the credentials for the cloud user to be able to generate and run tests. This is a one time setup after the admin user installs the application.

## Before you begin

Role required: admin

**Note:** The cloud runner works as expected, even if you have [Multi-factor authentication \(MFA\)](https://www.servicenow.com/docs/access?context=explore-mfa&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) set up for your cloud user.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Administration** &gt; **Select Cloud User**.

    **Note:** The **Select Cloud User** module is visible only to the admins. Even an ATF test admin can't access the **Select Cloud User** module.

2.  Select an admin user from the list.

    **Note:** Even if you are an admin, it is recommended to select a dedicated admin user.

3.  Click **Submit**.

    If the admin user is selected successfully, the following message shows up:![Image showing user selection success message](../image/atf-app-credentials-success.png)

    If the selected user is not an admin, an error message shows up. The following message is an example of one of the possible error messages. The error messages vary depending on the reason of the error.![Image showing user selection failed message](../image/atf-app-credentials-failed.png)

    The selection of a cloud user can fail for the following reasons:

    -   User wasn't found
    -   User is inactive
    -   User is locked out
    -   User needs a password reset
    -   User doesn't have an admin role
    -   User has read-only access
    -   User has web services only access
    **Note:** Selecting an admin user might take some time because it tries spinning a cloud browser and then log in to the selected user.


