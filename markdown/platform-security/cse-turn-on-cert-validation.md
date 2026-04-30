---
title: Turn on certificate validation
description: Protect your instance with certificate based validation.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Code Signing, Code Signing, Platform Security]
---

# Turn on certificate validation

Protect your instance with certificate based validation.

## Before you begin

Role required:

-   codesigning\_admin
-   security\_admin
-   sn\_kmf.cryptographic\_manager

## Procedure

1.  On your trusted non-production instance \(TNPI\), navigate to **All** &gt; **Code Signing** &gt; **Code Signing Configuration** to open the Code Signing configuration page.

2.  In the **Instance type** field, select **Trusted non-production instance**.

3.  Select the **Next** button.

4.  In the **Action** field under **Select the action you’d like to accomplish**, select **Turn on Cert Validation**.

5.  Select the **Next** button.

6.  Next to **Attachments** in the **Customer signing key pair and certificate** section select **+Add File** to upload a cryptographic key pair \(p12 file extension\) to use for customer signing.

    **Tip:** If the **+Add File** option is not available, verify that you are in the Global scope, and that you have the sn\_kmf.cryptographic\_manager role.

7.  In the **Password** field, enter the password for the uploaded key pair.

8.  Select **Import**.

9.  Select **Continue** to move to the next section.

10. Next to **Attachments** in the **COT administration key pair and certificate** section select **+Add File** to upload a cryptographic key pair \(p12 file extension\) to use for customer signing.

11. In the **Password** field, enter the password for the uploaded key pair.

12. Select **Import**.

13. Select **Continue** to move to the next section.

14. In the **Perform Trusted non-production tasks** section, wait for all tasks to be completed.

    Your instance generates and executes these tasks automatically. If you used Code Signing prior to the Vancouver release, tasks are created and executed to update your signatures.

    In some cases, no tasks are needed. **No tasks needed** displays on this page.

15. Select **Continue** to move to the next section.

16. On the **Export Configuration** file page, select **Export** to create and download a configuration file used to turn on Code Signing on your protected production instance.

    The export process downloads an XML file to your local machine for use in the steps detailed in [Configure Code Signing Enterprise on your protected production instance](cse-ppi-config.md).

17. On your Protected Production Instance \(PPI\), navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

18. Select **Import Update Set from XML** at the bottom of the Retrieved **Update Sets** list.

19. Select **Choose File**, and select your configuration file \(xml file extension\).

20. Select **Upload**.

21. Return to the code signing configuration page at **All** &gt; **Code Signing** &gt; **Code Signing Configuration**.

22. Use the wizard to complete your configuration, selecting the options for completing certificate validation activation.


**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

