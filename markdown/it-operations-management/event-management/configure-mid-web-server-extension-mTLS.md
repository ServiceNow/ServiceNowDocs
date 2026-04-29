---
title: Configure mTLS authentication for a MID Web Server
description: Enhance security in your MID Web Server extension by enabling mTLS authentication.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MID Web Server and agent mTLS Authentication, Configure the MID Web Server extension, MID Web Server, Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure mTLS authentication for a MID Web Server

Enhance security in your MID Web Server extension by enabling mTLS authentication.

## Before you begin

Ensure that you have enabled Transport Layer Security \(TLS\) on the agent. For details, see [Connect the agent to the MID Server using mTLS](../../agent-client-collector/task/enable-tls-agent.md).

Ensure that the **insecure-skip-tls-verify** parameter in the `acc.yml` configuration file is set to **false**. For details on the `acc.yml` file, see [Configuration file options](../../agent-client-collector/reference/acc-yml-options.md).

Role required: agent\_client\_collector\_admin

## About this task

The MID Web Server extension searches the following locations \(in the specified order\) to access the truststore location and password:

-   Truststore location: The **mid.webserver.truststore.path** JVM system property.

    If that property is empty, the extension retrieves the location from the **javax.net.ssl.trustStore** JVM system property.

    If no location is specified, the truststore location defaults to the absolute path of the `cacerts` file of the JRE running the MID Server.

-   Truststore password: The **Truststore Password** field on the extension form in the instance.

    If that field is empty, the system retrieves the password from the **javax.net.ssl.trustStorePassword** JVM system property.

    If no location is specified, the password defaults to **changeit**.


## Procedure

1.  Navigate to the root folder of your MID Server.

2.  Run the following command to add your certificate to the MID trust store:

    ```
    ./jre/bin/keytool -importcert -file /etc/pki/ca-trust/source/anchors/labcacert.pem -destkeystore ./jre/lib/security/cacerts -alias mtlsca
    ```

3.  Enter **changeit** when prompted for a password.

4.  Select **yes** on the confirmation message window to indicate that you trust the certificate.

5.  Run the following command to verify that your certificate was successfully added to the MID trust store.

    ```
    ./jre/bin/keytool -list -keystore ./jre/lib/security/cacerts -alias mtlsca
    ```

6.  Enter **changeit** when prompted for a password.

7.  In the MID Server wrapper override configuration file \(`wrapper-override.conf`, located in the `home/conf` directory of the MID Server\), configure the revocation of client certificates in the **mid.webserver.cert.revocation.check.enabled** property.

    -   If you have a custom internal certificate, set to **false** by adding the following line to the `conf/wrapper-override.conf` file on the MID Server:

        ```
        wrapper.java.additional.4=-Dmid.webserver.cert.revocation.check.enabled=false
        ```

    -   When enabling this property \(**true**\), configure the **mid.webserver.ocsp.responder.url** property with the OCSP responder URL. This value overrides any URL embedded in the certificate.
8.  If you have changed properties in the wrapper override configuration file, restart the MID Server.

9.  On your ServiceNow® instance, access the MID Server record and change the value of the **Authentication type** field to **mTLS**.

10. Restart the MID Web Server.

11. Verify that the MID Web Server and websocket endpoint are up and running.


## What to do next

[Connect the agent to the MID Server using mTLS](../../agent-client-collector/task/enable-tls-agent.md).

