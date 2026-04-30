---
title: Create keys and certificates
description: Create keys and certificates in your root directory to enable Transport Layer Security \(TLS\) setup. TLS setup is necessary before you can configure mTLS on the MID Web Server and agent.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [MID Web Server and agent mTLS Authentication, Configure the MID Web Server extension, MID Web Server, Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create keys and certificates

Create keys and certificates in your root directory to enable Transport Layer Security \(TLS\) setup. TLS setup is necessary before you can configure mTLS on the MID Web Server and agent.

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

**Note:** The commands specified in the following procedure are relevant only for a Centos7 host. When working with another OS, use the commands relevant for your host.

Role required: agent\_client\_collector\_admin

## Procedure

1.  In your root directory, create subdirectories for your certificates.

    ```
    mkdir -p labca labmid labacc;
    ```

2.  In your root directory:

    1.  Generate a custom certificate authority key pair.

        ```
        openssl ecparam -list_curves;
        openssl ecparam -out labca/ec-labcakey.pem -name prime256v1 -genkey; 
        ls labca/; 
        
        ```

        The generated output is the `ec-labcakey.pem` file.

    2.  Run the following commands:

        ```
        openssl ecparam -in labca/ec-labcakey.pem -text -noout; 
        openssl req -x509 -new -nodes -key labca/ec-labcakey.pem -sha512 -days 365 -out labca/labcacert.pem -subj "/C=<country>/ST=<state>/L=<location>/O=<organization> Lab/OU=<organization unit>/CN=<cn abbreviation>"; 
        openssl verify labca/labcacert.pem; 
        
        ```

        The generated output is:

        -   `labca/labcacert.pem: C = <country>, ST = <state>, L = <location>, O = <organization>, OU = <organization unit>, CN = <cn abbreviation>`
        -   `error 18 at 0 depth lookup: self signed certificate`
        -   `OK`
        **Note:** The `error` message can be ignored.

3.  Prepare the MID Web Server key and certificate.

    1.  Run the following commands in the root directory:

        ```
        sudo cp -a labca/labcacert.pem /etc/pki/ca-trust/source/anchors/;
        sudo update-ca-trust extract;
        openssl verify labca/labcacert.pem
        ```

        The generated output is: `labca/labcacert.pem: OK`

    2.  Run the command `"hostname --all-fqdns"` to obtain all of the valid hostnames for the specific VM.

    3.  Run the following commands:

        ```
        openssl req -new -newkey rsa:4096 -keyout labmid/rsa-labmidkey.pem -sha512 -nodes -out labmid/mid.csr -subj "/C=<country>/ST=<state>/L=<location>/O=<organization>/OU=<organization unit>/CN=<hostname>";
        openssl x509 -req -days 365 -in labmid/mid.csr -CA labca/labcacert.pem -CAkey labca/ec-labcakey.pem -CAcreateserial -extensions SAN -extfile <(cat /etc/pki/tls/openssl.cnf <(printf "\n[SAN]\nsubjectAltName=DNS:<hostname>")) -out labmid/mid.crt; 
        
        ```

        Enter the FQDN as the `<hostname>` value in the previous command. If more than one fqdn value is returned by the command, use the value with the following format: `hostname.domain.domain.com`.

        The generated output is: `Signature ok subject=/C=<country>/ST=<state>/L=<location>/O=<organization>/OU=<organization unit>/CN=<mid server host fqdn>: Getting CA Private Key`

4.  In your root directory, combine the key and cert files into one file, named `mid.pem`.

    ```
    cat labmid/rsa-labmidkey.pem labmid/mid.crt > labmid/mid.pem;
    ```


## What to do next

[Install the .pem file in the MID unified keystore and set up the MID Web Server](set-mid-web-server.md).

**Parent Topic:**[MID Web Server and agent mTLS Authentication](../../event-management/concept/mid-web-server-mTLS-authentication.md)

