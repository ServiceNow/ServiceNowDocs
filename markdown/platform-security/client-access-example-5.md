---
title: Upload the public/private keypair to the MID Server
description: Upload your public/private keypair to your MID Server. This keypair enables the MID Server to handle authentication requests from your instance.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring client accessible secrets, Secrets Management, Platform Security]
---

# Upload the public/private keypair to the MID Server

Upload your public/private keypair to your MID Server. This keypair enables the MID Server to handle authentication requests from your instance.

## Before you begin

Role required: none

Since ServiceNow lacks access to the private key, it can't pair it with the public key to decrypt the symmetric key, and then decrypt the credential. If the MID Server tries to use this encrypted credential, it's unable to decrypt the credential for authentication without access to the private key.

In these steps, you upload the private key to the MID Server to complete the Public/Private keychain. This upload grants the MID Server access without giving ServiceNow access.

To grant the MID Server access to the private key, you must construct a command to be run as administrator in Powershell. In this example, the command is for the Azure Windows virtual machine.

**Important:**

Ensure that the system you perform these steps on has access to both the MID Server and the keypair file.

## Procedure

1.  In your local environment, locate the folder where you created your key pair in the [Create encryption keys and certificate](client-access-example-1.md) steps.

2.  Find and copy the full path to the `manage-certificates.bat` file.

    **Note:** This file is located on your MID Server folder. Depending on where you've stored your MID Server folder, your path may look like this example:

    ```
    C:\Users\<your_user_account>\Documents\SM_Implementation\mid.utah-07-08-2022__patch4b01-31-2023_02-07-2023_1702.windows.x86-64\sm_ig_MIDS\bin\scripts\manage-certificates.bat
    ```

3.  Create a text file, and paste the path into the file.

4.  In the text file, add the following after the path:

    `-a your_identity_key_alias`

    Replace `your_identity_key_alias` with the name of the identity key alias that you created when you uploaded your public certificate.

5.  Find and copy the full path to your key pair file.

    **Note:** If you used the names in these steps that file is named `sm_keypair_bundle.pem`.

6.  In your text file, add this path to the end of the line, adding a space between this path and the previous information.

    The text within your text file should look similar to this example:

    ```
    C:\Users\<your_user_account>\Documents\SM_Implementation\mid.utah-07-08-2022__patch4b01-31-2023_02-07-2023_1702.windows.x86-64\sm_ig_MIDS\bin\scripts\manage-certificates.bat -a your_identity_key_alias C:\Users\<your_user_account>\Desktop\sm_keypair_bundle.pem
    ```

    **Note:** In this example, the `sm_keypair_bundle.pem` file is on the desktop to make the path shorter.

7.  Copy the entire text of your text file to the clipboard.

8.  Find Powershell on your system, and choose the **Run as Administrator** option.

9.  Paste the text from your text file into Powershell, and press Enter.

    If successful, you can see the following message:

    ```
    Installed certificate with alias: <your_identity_key_alias> into the MID keystore.
    ```

    **Tip:** If you don't see this message, ensure that your command has no errors, spaces, or unnecessary quotes. Ensure that the full path is typed correctly.

10. Restart your MID Server by navigating to your MID Server record, right-clicking the record, and selecting **Restart MID**.

    ![Restarting a MID Server](../images/client-side-7.png)

    Restarting the MID Server synchronizes the uploaded key pair in the MID keystore for use with operations. Wait for the MID Server to restart, with a status of **Up** and a validated value of **Yes** before continuing.


**Parent Topic:**[Configuring client accessible secrets](../concept/client-access-secret-landing.md)

