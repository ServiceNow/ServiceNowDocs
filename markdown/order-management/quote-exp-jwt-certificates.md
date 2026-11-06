---
title: Generate JWT certificates for ServiceNow Quote Experience
description: Create the security files that the ServiceNow Quote Experience guided setup needs to set up authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/quote-exp-jwt-certificates.html
release: australia
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 3
breadcrumb: [With guided setup, Setting up ServiceNow CPQ, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Generate JWT certificates for ServiceNow Quote Experience

Create the security files that the ServiceNow Quote Experience guided setup needs to set up authentication.

## Before you begin

Role required: admin

## About this task

You create these files on your computer by using two command-line tools: `keytool`, which comes with Java, and `openssl`. The files are created in one folder that you choose. Keep the folder and its files secure.

## Procedure

1.  Install Java.

    1.  Use one of these options:

        -   Company-approved install: use your company's approved software installation process, such as a software portal or a request to IT.
        -   Public download: download the latest LTS version for your operating system from a public site.
    2.  Run the installer and accept the default settings.

2.  If you use Windows, install OpenSSL.

    Mac users don't need to take action. OpenSSL is already installed.

    1.  Use one of these options:

        -   Company-approved install: use your company's approved software installation process to get OpenSSL.
        -   Public download: go to the [OpenSSL binaries page](https://www.openssl.org/community/binaries.html), download the **Win64 OpenSSL** installer, and run it with the default settings.
3.  Check that Java and OpenSSL work.

    1.  Open a terminal window.

        Use the option for your operating system:

        1.  Mac: search for Terminal.
        2.  Windows: search for Command Prompt.
    2.  Type `keytool -help` and press Enter.

        A list of options appears. If you see an error, Java isn't installed correctly. Repeat the Java step.

    3.  Type `openssl version` and press Enter.

        A version number appears. If you see an error, OpenSSL isn't installed correctly. Repeat the OpenSSL step.

4.  Create the security key file.

    1.  Create a folder for these files, such as `ServiceNow Certificates`, and open it in your terminal.

        -   Mac: find the folder in Finder, type `cd` with a space in the terminal, drag the folder into the terminal, and press Enter.
        -   Windows: open the folder in File Explorer, copy the path from the address bar, type `cd` with a space followed by the path in quotes, and press Enter. For example: `cd "C:\Users\jsmith\Documents\ServiceNow Certificates"`
    2.  Choose a strong password and record it in a safe place.

        **Note:** Check with your internal IT team about password storage guidelines. Your company may require a specific method, such as a password manager. You need this password for the guided setup and to recreate these files later.

    3.  Run this command.

        Replace both instances of *&lt;keystore-password&gt;* with your password, and remove the angle brackets.

        ```
        keytool -genkey -alias snclient -keyalg RSA -validity 365 -keystore snclient.keystore -storepass <keystore-password> -keypass <keystore-password>
        ```

    4.  Complete the prompts about the certificate, and confirm your inputs.

    5.  Confirm that a file named `snclient.keystore` is in your folder.

5.  Convert the key file to PKCS12 format.

    1.  Run the following command in the same terminal window and folder.

        Replace both instances of *&lt;keystore-password&gt;* with the password you chose.

        ```
        keytool -importkeystore -srckeystore snclient.keystore -srcstoretype JKS -destkeystore snclient.p12 -deststoretype PKCS12 -storepass <keystore-password> -deststorepass <keystore-password>
        ```

    2.  When prompted, enter the password you chose.

        The terminal doesn't show characters as you type.

    3.  Confirm that a file named `snclient.p12` is in your folder.

        If the file is not present, run the previous command again.

6.  Extract your private key.

    1.  Run this command in the same terminal window and folder.

        ```
        openssl pkcs12 -in snclient.p12 -nocerts -nodes -out private_key.pem
        ```

    2.  When prompted, enter the password you chose.

        The terminal doesn't show characters as you type.

    3.  Confirm that a file named `private_key.pem` is in your folder.

        You open this file in a plain-text editor, such as Notepad on Windows or TextEdit on Mac set to plain text, when you complete the guided setup.

7.  Export your public certificate.

    1.  Run this command in the same terminal window and folder.

        Replace *&lt;keystore-password&gt;* with the password you chose.

        ```
        keytool -exportcert -alias snclient -keystore snclient.keystore -storepass <keystore-password> -file snclient.cer
        ```

    2.  Confirm that a file named `snclient.cer` is in your folder.

8.  Convert the certificate to PEM format.

    1.  Run this command in the same terminal window and folder.

        ```
        openssl x509 -inform der -in snclient.cer -out certificate.pem
        ```

    2.  Confirm that a file named `certificate.pem` is in your folder.

        The terminal doesn't print a response.

9.  Copy the certificate contents.

    1.  Open `certificate.pem` in a plain-text editor, such as Notepad on Windows or TextEdit on Mac set to plain text.

    2.  Copy the entire contents, including the lines that start with `-----BEGIN` and end with `-----END`.

        Paste these contents into the **Public Certificate** field in the Quote Experience guided setup.


## What to do next

Continue with [Set up ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/setup-quote-experience.md) to add the certificate and private key to the guided setup.

