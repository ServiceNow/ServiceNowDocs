---
title: Generate certificates for Headless Browser setup for Microsoft Windows
description: Generate TLS/SSL certificates to secure the Docker REST API and authenticate HTTP requests.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Headless Browser setup for Microsoft Windows, Headless Browser for Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Generate certificates for Headless Browser setup for Microsoft Windows

Generate TLS/SSL certificates to secure the Docker REST API and authenticate HTTP requests.

## Before you begin

Role required: admin on your ServiceNow instance and local administrator on the host machine.

**Warning:** The only version of Microsoft Windows that ServiceNow supports as a host is Windows Server 2019 v10.0.17763.737. No other versions are supported. If you are unable to meet these requirements, a Linux host is recommended.

-   Complete the prerequisites listed in the [Headless Browser setup for Microsoft Windows](../concept/headless-browser-procedure-windows.md) topic. Make sure that the following programs are installed on your Windows server:
    -   Docker: [Docker application for Windows](https://docs.docker.com/engine/install/)
    -   Java keytool: [Chocolatey tool for javaruntime](https://community.chocolatey.org/packages/javaruntime)
    -   OpenSSL: [Chocolatey tool for openssl](https://community.chocolatey.org/packages/openssl)

Note the following requirements:

-   Two-way communication

    **Warning:** Be sure to get certificate authority keys from a trusted certificate authority.

    -   There must be two-way communication between the instance URL and your server.
    -   Find the IP address of your server and get your hostname. You can use one or both of them, but you need at least one.

        **Note:** If you don't have a hostname and are connecting via the IP address, you can enter the IP address and put "localhost" in the Hostname environment variable.

    **Tip:** To make remembering these easier, set the following environment variables:

    -   `export PASSWORD="<password to generate the certificates with>"`
    -   `export SERVERIP="<this server's IP address>"`
    -   `export HOSTNAME="<hostname of this server>"`
-   Port: Use Port 2376 or your own default port for this procedure.

    **Note:** Make sure your firewall rules allow inbound requests on this port

-   To learn more, see [Use TLS \(HTTPS\) to protect the Docker daemon socket](https://docs.docker.com/engine/security/protect-access/#:~:text=Use%20TLS%20(HTTPS)%20to%20protect,to%20a%20trusted%20CA%20certificate.).

## About this task

By default when exposing the Docker API, requests are not authenticated, which can leave your host machine vulnerable to attack. Docker API, however, does support TLS authentication where requests are verified against public private keys provided in the HTTPS encryption. In this step you create those keys for the server and the client.

## Procedure

1.  Open a command line.

2.  Generate a self-signed certificate authority key or retrieve a keypair from a trusted certificate authority.

    The following commands are an example. Note that your configuration might vary.

    ```
    openssl genrsa -aes256 -passout pass:%PASSWORD% -out ca-key.pem 4096
    openssl req -passin pass:%PASSWORD% -new -x509 -days 365 -key ca-key.pem -sha256 -out ca.pem 
    ```

3.  Generate the server keypair using the certificate authority key.

    The following commands are an example. Note that your configuration might vary.

    ```
    openssl genrsa -out server-key.pem 4096
    openssl req -subj /CN=%HOSTNAME% -new -key server-key.pem -out server.csr
    echo extendedKeyUsage = clientAuth > extfile.cnf
    openssl x509 -passin pass:%PASSWORD% -req -days 365 -in server.csr -CA ca.pem -CAkey ca-key.pem -CAcreateserial -out server-cert.pem -extfile extfile.cnf
    ```

4.  Create the client keypair using the certificate authority key.

    The following commands are an example. Note that your configuration might vary.

    ```
    openssl genrsa -out client-key.pem 4096
    openssl req -subj /CN=%HOSTNAME% -new -key client-key.pem -out client.csr
    echo subjectAltName = DNS:%HOSTNAME%,IP:%SERVERIP%,IP:127.0.0.1 > extfile.cnf
    openssl x509 -passin pass:%PASSWORD% -req -days 365 -in client.csr -CA ca.pem -CAkey ca-key.pem -CAcreateserial -out client-cert.pem -extfile extfile.cnf
    ```

5.  Import the CA Public Key and Client Keypair to a Java keystore.

    This instructions are an example Your configuration might vary.

    Create the keystore file and create a password for it \(and save for later use\): `keytool -genkey -keyalg RSA -alias dse -keystore my.keystore`

    Delete a default entry from the keystore file: `keytool -delete -alias dse -keystore my.keystore`

    **Note:** This entry is auto-generated, s.o is not needed.

    Import the CA public key to the keystore: `keytool -import -keystore my.keystore -trustcacerts -alias ca -file ca.pem`

    Import the client keypair.

    **Note:** You are creating a new pkcs12 keystore file and importing the keypair to it. Then copy the contents to your original keystore file.

    -   `openssl pkcs12 -export -name clientkeypair -in client-cert.pem -inkey client-key.pem -out clientkeypair.p12`
    -   `keytool -importkeystore -destkeystore my.keystore -srckeystore clientkeypair.p12 -srcstoretype pkcs12 -alias clientkeypair`
    Now that you have added all of the certificates to the keystore file, save the file **my.keystore** for later, as it will be uploaded to the ServiceNow instance. In addition, be sure to remember the password that you entered when prompted to create the keystore file; you will need to enter that into a form in the ServiceNow instance.


**Parent Topic:**[Headless Browser setup for Microsoft Windows](../concept/headless-browser-procedure-windows.md)

**Previous topic:**[Install Docker for Headless Browser setup for Microsoft Windows](headless-browser-install-docker.md)

**Next topic:**[Configure Docker for Headless Browser setup in Microsoft Windows](headless-browser-configure-docker-windows.md)

