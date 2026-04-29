---
title: Add a self-signed certificate to your operating system's truststore
description: Add a self-signed certificate to the truststore of your operating system \(OS\). By adding a certificate to the truststore, you can verify that the certificate is authentic and that your connections are secure.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ACC certificates, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Add a self-signed certificate to your operating system's truststore

Add a self-signed certificate to the truststore of your operating system \(OS\). By adding a certificate to the truststore, you can verify that the certificate is authentic and that your connections are secure.

## About this task

The procedure for adding a certificate to a truststore depends on the host's OS.

Adding a self-signed certificate to the truststore instructs the operating system to trust the certificate when it’s establishing secure connections. This way, the applications can communicate securely with services that use the self-signed certificate. If you add a certificate that isn't trustworthy, you might compromise your system's security.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  On a Windows OS:

    1.  Press the Windows button + `R` on your keyboard.

        The **Run** field opens.

    2.  Enter the string `certmgr.msc` and press **Enter**.

        The Certificate Manager opens.

    3.  Expand the Trusted Root Certification Authorities directory.

    4.  Select and hold \(or right-click\) **Certificates**.

    5.  Select **All tasks** &gt; **Import**.

        The Certificate Import Wizard opens.

    6.  Follow the steps in the Certificate Import Wizard.

        For details, see [Import a self-signed certificate](import-self-signed-certificate.md).

    Alternatively, you can add a Windows certificate using PowerShell by running the following command as an administrator:

    ```
    Import-Certificate -FilePath <path to your certificate file> -CertStoreLocation Cert:\LocalMachine\Root
    ```

2.  On a macOS:

    1.  Import the certificate into a keychain by running the following command in a terminal window:

        ```
        bash  code: sudo security add-trusted-cert -d -r trustRoot -k "/Library/Keychains/System.keychain" <path to your certificate file>
        ```

    2.  Enter the administrator password when prompted.

    3.  Open the Keychain Access application to verify that the certificate has been added.

        A successfully added certificate is labeled as, **This certificate is marked as trusted for...plugin verification.**

3.  On a Linux OS:

    1.  Prepare the self-signed certificate file as a Privacy Enhanced Mail \(PEM\) file.

    2.  Copy the certificate to the Certificate Authority \(CA\) directory, which is the directory where the certificates are stored.

        -   On a Debian/Ubuntu-based system, run the following command:

            ```
            sudo cp <path to certificate file> /usr/local/share/ca-certificates/
            ```

        -   On a Red Hat/Fedora-based system, run the following command:

            ```
            sudo cp <path to certificate file> /etc/pki/ca-trust/source/anchors
            ```

    3.  Update the CA certificates:

        -   On a Debian/Ubuntu-based system, run the following command:

            ```
            update-ca-certificates
            ```

            The command reads the certificate bundle in the `/usr/local/share/ca-certificates` directory, updates the certificate bundle, and stores it in `/ext/ssl/certs/ca-certificates.crt`.

        -   On a Red Hat/Fedora-based system, run the following command:

            ```
            sudo update-ca-trust extract
            ```


## Result

Your self-signed certificate is on the OS that you are working with.

**Parent Topic:**[Agent Client Collector certificates](../concept/acc-certificates.md)

