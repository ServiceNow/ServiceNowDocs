---
title: Configure Code Signing Enterprise on your trusted non-production instance
description: Turn on and configure Code Signing on your Trusted non-production instance \(TNPI\).
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Code Signing, Code Signing, Platform Security]
---

# Configure Code Signing Enterprise on your trusted non-production instance

Turn on and configure Code Signing on your Trusted non-production instance \(TNPI\).

## Before you begin

Roles required:

-   admin
-   security\_admin
-   codesigning\_admin

    **Note:** The codesigning\_admin role can be assigned using the process detailed in [Assign the Code Signing Administrator Role](cse-assign-roles.md).

-   sn\_kmf.cryptographic\_manager

You must have at least one cryptographic key pair and certificate \(p12 file extension\) for customer signing and Circle of Trust \(COT\) administration. For improved security, consider using separate cryptographic key pairs for customer signing and COT administration.

**Warning:** After completing this process, you’ll have downloaded a configuration file that must be installed on your PPI within an hour. Verify that you have time available after this process to upload the configuration file to your production instance. For details on that process, see [Upload your Code Signing configuration file to your protected production instance](cse-upload-cs-config.md).

## Procedure

1.  On your TNPI, navigate to **All** &gt; **Code Signing** &gt; **Code Signing Configuration** to open the Code Signing configuration page.

2.  In the **Instance type** field, select **Trusted non-production instance**.

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

13. In the **Perform Trusted non-production tasks** section, wait for all tasks to be completed.

    Your instance generates and executes these tasks automatically. If you used Code Signing prior to the Vancouver release, tasks are created and executed to update your signatures.

    In some cases, no tasks are needed. **No tasks needed** displays on this page.

14. Select **Continue** to move to the next section.

15. On the **Export Configuration** file page, select **Export** to create and download a configuration file used to turn on Code Signing on your protected production instance.

    The export process downloads an XML file to your local machine for use in the steps details in [Configure Code Signing Enterprise on your protected production instance](cse-ppi-config.md).


**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

