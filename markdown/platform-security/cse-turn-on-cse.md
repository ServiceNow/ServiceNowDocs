---
title: Configure Code Signing Enterprise on your trusted instance
description: Turn on and configure Code Signing on your trusted instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Code Signing, Platform Security]
---

# Configure Code Signing Enterprise on your trusted instance

Turn on and configure Code Signing on your trusted instance.

## Before you begin

Roles required:

-   admin
-   security\_admin
-   codesigning\_admin

    **Note:** The codesigning\_admin role can be assigned using the process detailed in [Assign the Code Signing Administrator Role](cse-assign-roles.md).

-   sn\_kmf.cryptographic\_manager

You must have at least one cryptographic key pair and certificate \(p12 file extension\) for customer signing and Circle of Trust \(COT\) administration. For improved security, consider using separate cryptographic key pairs for customer signing and COT administration.

**Warning:** After completing this process, you will have downloaded a configuration file that must be installed on your protected instance within an hour. Verify that you have time available after this process to upload the configuration file to your protected instance. For details on that process, see [Upload your Code Signing configuration file to your protected instance](cse-upload-cs-config.md).

## Procedure

1.  On your trusted instance, navigate to **All** &gt; **Code Signing** &gt; **Configuration** &gt; **Guided Setup** to open the Code Signing configuration page.

2.  In the **Instance type** field, select **trusted instance**.

3.  Select the **Next** button.

4.  In the **Action** field under **Select the action you’d like to accomplish**, select **Turn on Code Signing**.

5.  Next to **Attachments** in the **Customer signing key pair and certificate** section select **+Add File** to upload a cryptographic key pair \(p12 file extension\) to use for customer signing.

    **Tip:** If the **+Add File** option is not available, verify that you are in the Global scope, and that you have the sn\_kmf.cryptographic\_manager role.

6.  In the **Password** field, enter the password for the uploaded key pair.

7.  Select **Import**.

8.  Select **Continue** to move to the next section.

9.  Next to **Attachments** in the **COT administration key pair and certificate** section select **+Add File** to upload a cryptographic key pair \(p12 file extension\) to use for customer signing.

10. In the **Password** field, enter the password for the uploaded key pair.

11. Select **Import**.

12. Select **Continue** to move to the next section.

13. On the **Export Configuration** file page, select **Export** to create and download a configuration file used to turn on Code Signing on your protected instance.

    The export process downloads an XML file to your local machine for use in the steps details in [Configure Code Signing Enterprise on your protected instance](cse-ppi-config.md).

    **Note:** Code Signing enforces limits on large update sets to improve the user experience. The maximum size for an update set is 10,000 records.


**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

