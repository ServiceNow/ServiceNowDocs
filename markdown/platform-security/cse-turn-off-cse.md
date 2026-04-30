---
title: Turn off Code Signing
description: Disable code signing on your protected instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Code Signing, Platform Security]
---

# Turn off Code Signing

Disable code signing on your protected instance.

## Before you begin

Role required: admin, codesigning\_admin

## Procedure

1.  On your trusted instance, navigate to **All** &gt; **Code Signing** &gt; **Configuration** &gt; **Guided Setup** to open the Code Signing configuration page.

2.  In the **Instance type** field, select **trusted instance**.

3.  Select the **Next** button.

4.  In the **Action** field under **Select the action you’d like to accomplish**, select **Turn off Code Signing**.

5.  In the **Export configuration file** panel, select **Export** to download the update set.

    The export process downloads an XML file to your local machine for use in the next steps.

6.  Select **Done**.

7.  Log in to your protected instance.

8.  Upload your configuration files using the steps in [Upload your Code Signing configuration file to your protected instance](cse-upload-cs-config.md).

9.  Navigate to **All** &gt; **Code Signing** &gt; **Configuration** &gt; **Guided Setup** to open the Code Signing configuration page.

10. In the **Instance type** field, select **protected instance**.

11. Select the **Next** button.

12. Select the **Please confirm the Code Signing configuration update set was imported and committed** check box.

13. Select the **Next** button.

14. Wait for the certificate installation to complete.

    After completion, a **Code Signing configuration completed successfully** message displays.


## Result

You can verify successful completion by looking at your system properties. Look for the **com.snc.kmf.signature.validation.flag** property on the System Properties \[sys\_property\] table, and verify that it has a value of **false**.

**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

