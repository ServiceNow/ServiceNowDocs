---
title: Configure password for a user
description: Set your user's password for the instance based on the password policy that is configured.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure your password policy, Password complexity requirements, Local authentication, Authentication, Access Management]
---

# Configure password for a user

Set your user's password for the instance based on the password policy that is configured.

## Before you begin

Users created for setting the password for their first login. For more information, see Create a user.

To populate the **Password** field directly on the user form, enable the **Enable to show the password field on the sys\_user Form** \(glide.user.show.password.field\). To know more about the properties, see [Password policy properties](../reference/password-policy-properties.md).

Role required: password\_policy\_admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Select the user from the list in the Users page.

3.  To set the password based on the password policy, click **Set Password**.

    The Set Password pop-up is displayed.

    ![Set Password](../images/set-password.png)

4.  In the Set Password, perform the following.

    1.  Click **Generate** to generate the password.

        ![Generate Password](../images/generate-password.png)

    2.  Click the **View** icon to view the password.

        ![View Password](../images/view-password.png)

    3.  Click the **Copy** icon to copy the password to share to the user.

        ![Copy Password](../images/copy-password.png)

5.  Click **Save Password**.

    The password is set for the user. Also the Password needs rest check-box is automatically enabled.

    The user during the first login must use the same password for login and change the password upon login adhering to the password policy configured by the administrators.


