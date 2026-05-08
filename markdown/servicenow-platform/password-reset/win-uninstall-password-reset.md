---
title: Uninstall the Password Reset Windows Application
description: You can run either an EXE or an MSI file to uninstall the application.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Password Reset Windows Application, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Uninstall the Password Reset Windows Application

You can run either an EXE or an MSI file to uninstall the application.

## Before you begin

Role required: Windows Local Administrator

## Procedure

1.  Follow either procedure.

<table id="choicetable_or2_xw4_tx"><tbody><tr><td id="d369139e55">

**Use an EXE file from the command line**

</td><td>

1.  Navigate to the uninstall directory that you created during installation, for example:

    ```
C:\Program Files\ServiceNow\uninstall\
    ```

2.  Double-click the `unins000.exe` file.


</td></tr><tr><td id="d369139e78">

**Use an MSI file from the command line**

</td><td>

1.  Navigate to the directory that holds the `PasswordResetWinAppInstall.msi` file.
2.  Run the following command at the command line:

    ```
msiexec.exe /x PasswordResetWinAppInstall.msi /quiet
    ```

</td></tr></tbody>
</table>
**Parent Topic:**[Installing and configuring Password Reset Windows Application](../concept/install-configure-password-reset-windows-app.md)

