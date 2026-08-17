---
title: Create keys and certificates
description: Create keys and certificates in your root directory to enable Transport Layer Security \(TLS\) setup. TLS setup is required before you can configure mTLS on the MID Web Server and agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/create-keys-and-certificates.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [MID Web Server and agent mTLS Authentication, Configure the MID Web Server extension, MID Web Server, Event Management setup, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Create keys and certificates

Create keys and certificates in your root directory to enable Transport Layer Security \(TLS\) setup. TLS setup is required before you can configure mTLS on the MID Web Server and agent.

## Before you begin

-   Ensure that there are no keys installed in the MID unified keystore by running the following command:

    ```
    bin/scripts/manage-certificates.(sh/bat) -l
    ```

    When there are no keys installed, the output is: `defaultsecuritypairhandle`

-   Invalidate your MID Server.

    If additional keys exist in the output, reinstall those keys after invalidating the MID Server.

-   Ensure that the MID Server is connected to the instance.
-   Select a directory in which you want to create certificates, to be called the **root** directory.
-   For Windows environments only: Install [Win32/Win64 OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) with all dependencies and ensure it is on the system `PATH`.

**Note:** This procedure includes commands for both CentOS 7/Linux and Windows Server environments. Select the commands relevant for your host operating system. If working with another Linux distribution, adapt the commands as needed for your specific OS.

Role required: agent\_client\_collector\_admin

## Procedure

1.  In a Linux environment:

    1.  Create subdirectories for your certificates in your root directory.

        ```
        mkdir -p labca labmid labacc;
        ```

    2.  Generate the EC key pair.

        ```
        openssl ecparam -list_curves;
        openssl ecparam -out labca/ec-labcakey.pem -name prime256v1 -genkey; 
        ls labca/;
        ```

        The generated output is the `ec-labcakey.pem` file.

    3.  Create the root CA certificate.

        ```
        openssl ecparam -in labca/ec-labcakey.pem -text -noout; 
        openssl req -x509 -new -nodes -key labca/ec-labcakey.pem -sha512 -days 365 -out labca/labcacert.pem -subj "/C=<country>/ST=<state>/L=<location>/O=<organization> Lab/OU=<organization unit>/CN=<cn abbreviation>"; 
        openssl verify labca/labcacert.pem;
        ```

        Generated output:

        -   `labca/labcacert.pem: C = <country>, ST = <state>, L = <location>, O = <organization> Lab, OU = <organization unit>, CN = <cn abbreviation>`
        -   `OK`
    4.  Import the CA certificate into the system trust store.

        ```
        sudo cp -a labca/labcacert.pem /etc/pki/ca-trust/source/anchors/;
        sudo update-ca-trust extract;
        openssl verify labca/labcacert.pem
        ```

        Generated output: `labca/labcacert.pem: OK`

    5.  Obtain the fully qualified domain name \(FQDN\) for the host.

        ```
        hostname --all-fqdns;
        ```

    6.  Generate the server certificate signing request \(CSR\) and sign it with the CA.

        Enter the FQDN as the `<hostname>` value in the following commands. If more than one FQDN value is returned, use the value with the following format: `hostname.domain.domain.com`.

        ```
        openssl req -new -newkey rsa:4096 -keyout labmid/rsa-labmidkey.pem -sha512 -nodes -out labmid/mid.csr -subj "/C=<country>/ST=<state>/L=<location>/O=<organization>/OU=<organization unit>/CN=<hostname>";
        openssl x509 -req -days 365 -in labmid/mid.csr -CA labca/labcacert.pem -CAkey labca/ec-labcakey.pem -CAcreateserial -extensions SAN -extfile <(cat /etc/pki/tls/openssl.cnf <(printf "\n[SAN]\nsubjectAltName=DNS:<hostname>")) -out labmid/mid.crt;
        ```

        Generated output:

        ```
        Signature ok
        subject=/C=<country>/ST=<state>/L=<location>/O=<organization>/OU=<organization unit>/CN=<mid server host fqdn>
        Getting CA Private Key
        ```

    7.  Combine the key and certificate files into one file, named `mid.pem`.

        ```
        cat labmid/rsa-labmidkey.pem labmid/mid.crt > labmid/mid.pem;
        ```

2.  In a Windows environment:

    1.  Create subdirectories for your certificates in your root directory.

        ```
        mkdir labca labmid labacc
        ```

    2.  Generate the EC key pair.

        ```
        openssl ecparam -list_curves
        openssl ecparam -out labca\ec-labcakey.pem -name prime256v1 -genkey
        dir labca
        ```

        The generated output is the `ec-labcakey.pem` file.

    3.  Create the root CA certificate.

        ```
        openssl ecparam -in labca\ec-labcakey.pem -text -noout
        openssl req -x509 -new -nodes -key labca\ec-labcakey.pem -sha512 -days 365 -out labca\labcacert.pem -subj "/C=<country>/ST=<state>/L=<location>/O=<organization> Lab/OU=<organization unit>/CN=<cn abbreviation>"
        openssl verify labca\labcacert.pem
        ```

        Generated output: `C=<country>, ST=<state>, L=<location>, O=<organization> Lab, OU=<organization unit>, CN=<cn abbreviation>`

    4.  Import the CA certificate into the system trust store.

        ```
        certutil -addstore -f "Root" labca\labcacert.pem
        openssl verify -CAfile labca\labcacert.pem labca\labcacert.pem
        ```

        Generated output: `labca/labcacert.pem: OK`

    5.  Obtain the fully qualified domain name \(FQDN\) for the host.

        ```
        net config workstation | findstr /C:<Full Computer name>
        ```

        The `Full Computer name` value returned is the FQDN to use as the `<hostname>` later in this procedure.

    6.  Create the SAN \(Subject Alternative Name\) configuration file.

        ```
        copy "%ProgramFiles%\OpenSSL-Win64\bin\cnf\openssl.cnf" openssl-san.cnf
        echo.>>openssl-san.cnf
        echo [SAN]>>openssl-san.cnf
        echo subjectAltName=DNS:<hostname>>>openssl-san.cnf
        ```

        Adjust the source `openssl.cnf` path to match your OpenSSL installation location if it differs from the default.

    7.  Generate the server certificate signing request \(CSR\) and sign it with the CA.

        Enter the FQDN as the `<hostname>` value in the following commands. If more than one FQDN value is returned, use the value with the following format: `hostname.domain.domain.com`.

        ```
        openssl req -new -newkey rsa:4096 -keyout labmid\rsa-labmidkey.pem -sha512 -nodes -out labmid\mid.csr -subj "/C=<country>/ST=<state>/L=<location>/O=<organization>/OU=<organization unit>/CN=<hostname>"
        openssl x509 -req -days 365 -in labmid\mid.csr -CA labca\labcacert.pem -CAkey labca\ec-labcakey.pem -CAcreateserial -extensions SAN -extfile openssl-san.cnf -out labmid\mid.crt
        ```

        Generated output:

        ```
        Signature ok
        subject=/C=<country>/ST=<state>/L=<location>/O=<organization>/OU=<organization unit>/CN=<mid server host fqdn>
        Getting CA Private Key
        ```

        **Note:** With OpenSSL 3.x \(the Win32/Win64 installer\), the `Getting CA Private Key` line may not appear in the output, but `Signature ok` and the correct `subject=` line are still present. To confirm the certificate was signed correctly, verify `labmid\mid.crt` directly:

        ```
        openssl x509 -in labmid\mid.crt -noout -subject -dates
        ```

        This command shows the subject you specified and valid `notBefore`/`notAfter` dates.

    8.  Combine the key and certificate files into one file, named `mid.pem`.

        ```
        copy /b labmid\rsa-labmidkey.pem+labmid\mid.crt labmid\mid.pem
        ```


## What to do next

[Set up the MID Web Server with a .pem file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/set-mid-web-server.md).

