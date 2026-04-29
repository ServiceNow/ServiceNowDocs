---
title: Edge Encryption ODBC driver integration
description: Configure your ODBC driver to query data encrypted by Edge Encryption. The Edge Encryption proxy server encrypts ODBC driver requests to the ServiceNow instance when Edge Encryption is integrated with the ODBC driver.If a Certificate Authority trusted by the ODBC driver has not signed the Edge Encryption proxy server certificate, you must import a self-signed certificate to the ODBC truststore. You can export the certificate from the Edge Encryption proxy server and import it into the ODBC truststore.Set the ODBC driver properties to route requests through the Edge Encryption proxy server.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data integration with Edge Encryption, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Edge Encryption ODBC driver integration

Configure your ODBC driver to query data encrypted by Edge Encryption. The Edge Encryption proxy server encrypts ODBC driver requests to the ServiceNow instance when Edge Encryption is integrated with the ODBC driver.

Encrypted responses from the instance are decrypted through the Edge Encryption proxy server before passing to the ODBC driver in your network.

For a successful integration, the ODBC driver must trust the Edge Encryption proxy server certificate. If the Edge Encryption proxy server certificate is signed by a Certificate Authority trusted by the ODBC driver, the Edge Encryption proxy server is automatically trusted. However, if a Certificate Authority trusted by the ODBC driver has not signed the Edge Encryption proxy server certificate, you must import the self-signed certificate to the ODBC truststore.

**Parent Topic:**[Data integration with Edge Encryption](data-integration.md)

## Import a self-signed certificate to the ODBC truststore

If a Certificate Authority trusted by the ODBC driver has not signed the Edge Encryption proxy server certificate, you must import a self-signed certificate to the ODBC truststore. You can export the certificate from the Edge Encryption proxy server and import it into the ODBC truststore.

### Before you begin

Role required: admin

To determine whether a Certificate Authority trusted by the ODBC driver has signed the Edge Encryption proxy server certificate, run the following command in the keystore directory in the proxy home directory to view a list of Certificate Authorities trusted by the ODBC driver:

```
keytool -keystore "<ODBC directory>\ip\Java\jre\lib\security\cacerts" -list
```

**Note:**

In most cases, the client connects to the Edge Encryption proxies through a load balancer, so the certificate would be the certificate configured in the load balancer.

In the case where there is no load balancer between the client and the Edge proxy server, the certificate is the certificate presented by the Edge proxy and is configured in the **edgeencryption.properties** file.

```
edgeencryption.proxy.https.port = 9090
edgeencryption.proxy.https.keystore.path = keystore/keystore
edgeencryption.proxy.https.keystore.password = password
edgeencryption.proxy.https.cert.alias = jetty
```

For details on editing properties, see [Configure additional properties in the Edge Encryption properties file](../task/set-props.md)

### Procedure

1.  Change to the keystore directory in the proxy home directory.

2.  Check the keystore for the self-signed certificate.

    1.  To check the keystore for the certificate, you can run the following command to list all the items in the keystore.

        ```
        keytool -list -keystore keystore.jceks -storetype jceks -v
        ```

    2.  Locate the key alias in the list of items.

3.  Using the key alias, export the certificate to a .cer file.

    ```
    keytool -export -alias <key alias> -keystore keystore.jceks -storetype jceks -rfc -file <file name>.cer
    ```

4.  Change to your ODBC truststore directory: `ODBC\ip\Java\jre\lib\security\cacerts`.

5.  Import the certificate to your ODBC truststore.

    ```
    keytool -keystore cacerts -importcert -alias $<key alias> -file <file name>.cer
    ```


## Set the ODBC driver properties

Set the ODBC driver properties to route requests through the Edge Encryption proxy server.

### Before you begin

Role required: admin

### Procedure

1.  In Windows, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC Management Console**.

2.  Expand the console tree root to: `ServiceNow ODBC Manager\Manager\<installation location>\Services\ServiceNow_ODBC\Data Source Settings\ServiceNow\IP Parameters`.

3.  Double-click the **DataSourceIPProperties** attribute.

4.  Change the **Value** to the URL of your Edge Encryption proxy server, such as `https://<IP address>:<port>`

    ![DataSourceIPProperties](../images/OBDCPropertyforEdge.png "DataSourceIPProperties")

5.  Click **OK**.


### What to do next

The ODBC driver is now configured to route requests to the instance through the Edge Encryption proxy server.

