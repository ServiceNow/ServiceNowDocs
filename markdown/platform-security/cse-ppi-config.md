---
title: Configure Code Signing Enterprise on your protected instance
description: Turn on and configure Code Signing on your protected instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Code Signing, Platform Security]
---

# Configure Code Signing Enterprise on your protected instance

Turn on and configure Code Signing on your protected instance.

## Before you begin

Roles required:

-   admin
-   security\_admin
-   codesigning\_admin

    **Note:** The codesigning\_admin role can be assigned using the process detailed in [Assign the Code Signing Administrator Role](cse-assign-roles.md).

-   sn\_kmf.cryptographic\_manager

## Procedure

1.  On your PPI, navigate to **All** &gt; **Code Signing** &gt; **Configuration** &gt; **Guided Setup** to open the Code Signing configuration page.

2.  In the **Instance type** field, select **protected instance**.

3.  Select the **Next** button.

4.  Select the **Please confirm the Code Signing configuration update set was imported and committed** check box.

5.  Select the **Next** button.

6.  Wait for the certificate installation to complete.

    A blue alert message displays indicating that items from the configuration file are installing. The alert disappears in a few seconds when the installation finishes.

7.  Next to **Attachments** in the **Runtime/notarization key pair and certificate** section select **+Add File** to upload a cryptographic key pair \(p12 file extension\) to use for runtime/notarization purposes.

    You can re-use a key pair from the trusted instance or upload a new one specifically for this use.

    **Tip:** If the **+Add File** option is not available, verify that you are in the Global scope, and that you have the sn\_kmf.cryptographic\_manager role.

8.  In the **Password** field, enter the password for the uploaded key pair.

9.  Select **Import**.

10. Select **Continue** to move to the next section.

11. Wait while your instance performs a guardrail check.

    This check scans your instance for any invalid or missing signatures, and might take some time to complete. Don't exit or refresh the page until the scan completes.

    This workflow identifies signatures that were generated with expired or inactive certificates and re-signs the affected records. To improve performance, the workflow now divides the process into multiple events and runs them in parallel.

12. If the scan finds invalid signatures, select **Download Report**.

    Selecting **Download Report** downloads a report \(`scan_report.txt`\) that you can use to investigate and fix the invalid signatures.

    After resolving errors, refresh the page to re-run the check.

13. If there are no errors, select **Complete setup**.

14. Wait for the configuration jobs to complete.

    Your instance runs one or more jobs to complete the configuration process. Don’t exit or refresh the page until the jobs have finished. When finished, you should see a **Code Signing configuration completed successfully** message.


## Result

Signature validation is now being enforced on your production instance. You can verify successful completion by looking at your system properties. Look for the **com.snc.kmf.signature.validation.flag** property on the System Properties \[sys\_property\] table, and verify that it has a value of **true**. Verify that the **com.snc.kmf.signature.validation.certificate\_trust** property doesn’t have an empty value.

![Property values verifying that signature validation is now being enforced](../image/cse-verify.png)

**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

