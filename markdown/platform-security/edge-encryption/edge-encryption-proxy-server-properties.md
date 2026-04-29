---
title: Edge Encryption proxy server properties
description: The edgeencryption.properties configuration file located in the &lt;installation directory&gt;/conf/ folder contains properties used to configure your environment.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# Edge Encryption proxy server properties

The `edgeencryption.properties` configuration file located in the `<installation directory>/conf/` folder contains properties used to configure your environment.

You must restart the proxy server after making changes to any proxy server properties.

## Clear text and static IV properties

<table id="table_sdk_r5j_nsb"><tbody><tr><td>

edgeencryption.customer.assigned.known.cleartext

</td><td>

Clear text to let the instance verify that all proxies are using the same keys. At startup, the proxy encrypts the clear text and sends the encrypted text to the instance. The instance does not know the clear text, nor are keys sent to the instance. This property must be the same for all proxies.

</td></tr><tr><td>

edgeencryption.encrypter.static.iv

</td><td>

Static IV \(initialization vector\) used in equality-preserving and order-preserving encryption. This property must be the same for all proxies and must be exactly 16 bytes \(16 ASCII characters\).

</td></tr></tbody>
</table>## Digital signature properties

<table id="table_kkk_wtj_nsb"><tbody><tr><td>

edgeencryption.proxy.signature.keystore.path

</td><td>

Path and Java KeyStore file name.

</td></tr><tr><td>

edgeencryption.proxy.signature.keystore.password

</td><td>

Password. The default password is &lt;changeme&gt;. Change the password after installing the Java KeyStore.

</td></tr><tr><td>

edgeencryption.proxy.signature.keystore.keyalias

</td><td>

The key alias given as the -alias argument when the RSA key pair is generated.

</td></tr></tbody>
</table>## File store property

<table id="table_o4z_gvj_nsb"><tbody><tr><td>

edgeencryption.keyfile.directory

</td><td>

The directory specifies where key files are stored. If using the Java KeyStore or a SafeNet KeySecure keystore, leave this property commented out.Example:

```
edgeencryption.keyfile.directory=keys
```

 If using Unbound Technology keys, uncomment this property and set the value to the keys directory.

</td></tr></tbody>
</table>## General configuration properties

<table id="table_pzx_4vj_nsb"><tbody><tr><td>

edgeencryption.config.poll.interval

</td><td>

Poll interval in seconds. The default setting means that it takes 5 seconds for the proxy to learn of encryption configuration changes. Larger values cause the instance to take longer to detect an offline proxy. **Warning:** Do not change this property. Changing the default setting of the Proxy Poll Interval can result in detection delays when a proxy comes online.

</td></tr><tr><td>

edgeencryption.rules.dir

</td><td>

Folder where the encryption rules are stored on the proxy.

</td></tr><tr><td>

edgeencryption.encryption.order\_preserving.cache.enable

</td><td>

Setting determines whether caching is used to support order-preserving encryption types.

</td></tr><tr><td>

edgeencryption.encryption.order\_preserving.cache.size

</td><td>

Maximum cache size, in bytes.

</td></tr><tr><td>

edgeencryption.jobs.concurrency

</td><td>

Maximum number of mass encryption jobs that can run concurrently on this proxy.

</td></tr><tr><td>

edgeencryption.jobs.requests\_per\_second

</td><td>

Number of http job requests per second that can be sent to the instance by this proxy.

</td></tr><tr><td>

edgeencryption.attachments.request.timeout.seconds

</td><td>

Attachment upload request timeout in seconds.

</td></tr><tr><td>

edgeencryption.request.buffer.size

</td><td>

Size of an encryption request. If an encryption request is larger than this size, the excess is saved to disk. **Warning:** Do not change this property.

</td></tr><tr><td>

edgeencryption.httpclient.request.buffer.size

</td><td>

Size of the client request. If the client request is larger than this size, the excess is saved to disk. **Warning:** Do not change this property.

</td></tr><tr><td>

edgeencryption.httpclient.header.size

</td><td>

Size of the request/response header.-   Minimum value: 8K
-   Maximum value: 32K

 **Warning:** Do not change this property.

</td></tr><tr><td>

edgeencryption.proxy.idle.timeout

</td><td>

Time in seconds after which a transaction times out.Default value: 300 \(seconds\)

</td></tr><tr><td>

edgeencryption.proxy.keepalive.interval

</td><td>

Time in seconds between pings issued by the proxy to the instance. Pings are issued periodically to verify connectivity between the proxy and the instance.-   Default value: 10 \(seconds\)
-   Minimum value: 5 \(seconds\)

</td></tr><tr><td>

edgeencryption.register.retry.count

</td><td>

Maximum number of times the proxy pings the instance to try to register.Default value: 0 \(no limit\)

</td></tr><tr><td>

edgeencryption.tokenization.exclusion.list

</td><td>

Encryption patterns cannot tokenize strings found in these fields.

</td></tr></tbody>
</table>## Java KeyStore properties

<table id="table_rpj_bvj_nsb"><tbody><tr><td>

edgeencryption.keystore.path

</td><td>

Path to the Java KeyStore. If using a file store or a SafeNet KeySecure keystore, leave this property commented out. Example:

```
edgeencryption.keystore.path = keystore/keystore.jceks

```

</td></tr><tr><td>

edgeencryption.keystore.password

</td><td>

Password the proxy uses to connect to the Java KeyStore. If using a file store or a SafeNet KeySecure keystore, leave this property commented out.

</td></tr></tbody>
</table>## Logging properties

Logging properties are found in the lo4gj2.properties file found in the `<installation directory>/conf/` directory. These properties are only changed for troubleshooting or when directed by ServiceNow support. For details see [How to increase debug logging for the Edge Encryption proxy](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0621289).

## NAE device keystore properties

<table id="table_wh3_b5j_nsb"><tbody><tr><td>

edgeencryption.nae.retries

</td><td>

Number of retries to make.

</td></tr><tr><td>

edgeencryption.nae.enabled

</td><td>

Setting indicates whether an NAE device is available.

</td></tr><tr><td>

edgeencryption.nae.server

</td><td>

Name of the NAE server.

</td></tr><tr><td>

edgeencryption.nae.port

</td><td>

Port used by the NAE server.

</td></tr><tr><td>

edgeencryption.nae.protocol

</td><td>

Protocol used by the NAE server.

</td></tr><tr><td>

edgeencryption.nae.keystore.path

</td><td>

Path to the keystore on the NAE server.

</td></tr><tr><td>

edgeencryption.nae.keystore.password

</td><td>

NAE keystore password.

</td></tr><tr><td>

edgeencryption.nae.username

</td><td>

User name to use to authenticate with the NAE device.

</td></tr><tr><td>

edgeencryption.nae.password

</td><td>

Password to use to authenticate with the NAE device.

</td></tr><tr><td>

edgeencryption.nae.client.certificate

</td><td>

Certificate located in the keystore on the NAE server. Set this property to authenticate using a certificate instead of a username and password.

</td></tr></tbody>
</table>## Password property

<table id="table_jy2_l5j_nsb"><tbody><tr><td>

edgeencryption.encrypter.properties.password

</td><td>

Name of the file in the `conf` folder that contains a string used within a secure process to obfuscate passwords in the `edgeencryption.properties` file. **Note:** Name of the file in the `conf` folder that contains a string used within a secure process to obfuscate passwords in the `edgeencryption.properties` file.

</td></tr></tbody>
</table>## Proxy properties

<table id="table_q2d_4tj_nsb"><tbody><tr><td>

edgeencryption.proxy.host

</td><td>

Server name, IP address, or fully qualified domain name of the computer running the proxy. Along with the port, this property defines the URL used by the client to access the proxy server.

</td></tr><tr><td>

edgeencryption.proxy.name

</td><td>

Proxy name. Must be unique for each proxy.

</td></tr><tr><td>

edgeencryption.proxy.http.port

</td><td>

Port on the proxy for HTTP communication.

</td></tr><tr><td>

edgeencryption.proxy.https.port

</td><td>

Port on the proxy for HTTPS communication.

</td></tr></tbody>
</table>## Proxy configuration locked property

<table id="table_jxx_ssj_nsb"><tbody><tr><td>

edgeencryption.proxy.locked

</td><td>

When true, the proxy does not accept encryption configuration changes or encryption rule changes from the instance. Set this property on the production instance after all encryption configurations and rules are final.

</td></tr></tbody>
</table>## Proxy database properties

<table id="table_v23_vsj_nsb"><tbody><tr><td>

edgeencryption.db.url

</td><td>

Proxy database location. Must be the same for all encryption proxies connecting to the same instance.

</td></tr><tr><td>

edgeencryption.db.user

</td><td>

User name for accessing the proxy database. Must be the same for all encryption proxies connecting to the same instance.

</td></tr><tr><td>

edgeencryption.db.password

</td><td>

Password to access the proxy database. Must be the same for all encryption proxies connecting to the same instance.

</td></tr><tr><td>

edgeencryption.db.name

</td><td>

Proxy database name. Must be the same for all encryption proxies connecting to the same instance. The default for this property is `edgeencryption`.

</td></tr><tr><td>

edgeencryption.db.bootstrap.file

</td><td>

Bootstrap file for the proxy database. The file is relative to the `sql/` directory. Must be the same for all encryption proxies connecting to the same instance.**Warning:** Under normal circumstances, do not change this parameter.

</td></tr></tbody>
</table>## Proxy server performance properties

Proxy server performance properties are not present in the configuration file by default. To change the default values, you must add the properties and restart the proxy server. For more information, see [Edge Encryption diagnostics and performance](../concept/edge-stats.md#).

<table id="table_jf2_kwj_nsb"><tbody><tr><td>

edgeencryption.stat.collection.enabled

</td><td>

Enables the collection of statistics used by the Edge Encryption proxy server performance dashboard.Default value: true

 Add this property and set the value to false to disable the collection of statistics used by the Edge Encryption proxy server performance dashboard.

</td></tr><tr><td>

edgeencryption.stat.collection.interval

</td><td>

Interval length in seconds during which the Edge Encryption proxy server collects statistics. The value cannot be less than 30 seconds. Default value: 30 \(seconds\)

</td></tr></tbody>
</table>## SSL certificate properties

Restart your proxy if you change the value of any SSL certificate property. The system uses the HTTPS keypair on startup to establish the proxy server connection and determine how the proxy answers client requests.

<table id="table_v1w_rtj_nsb"><tbody><tr><td>

edgeencryption.proxy.https.cert.alias

</td><td>

Alias of the certificate provided by the proxy server to connecting clients.

</td></tr><tr><td>

edgeencryption.proxy.https.keystore.path

</td><td>

Path to the keystore that contains the HTTPS certificate.

</td></tr><tr><td>

edgeencryption.proxy.https.keystore.password

</td><td>

Password for the keystore that contains the HTTPS certificate.

</td></tr></tbody>
</table>## Target \(instance\) properties

<table id="table_pmp_htj_nsb"><tbody><tr><td>

edgeencryption.target.host

</td><td>

Host name for the instance. Must be the same for all encryption proxies connecting to the same instance. This property is set when the proxy is installed. For example, `instancename.servicenow.com`

</td></tr><tr><td>

edgeencryption.target.port

</td><td>

Instance port. Must be the same for all encryption proxies connecting to the same instance. This property is set when the proxy is installed.

</td></tr><tr><td>

edgeencryption.target.protocol

</td><td>

Instance protocol. Must be the same for all encryption proxies connecting to the same instance. This property is set when the proxy is installed. Options include:-   http
-   https

</td></tr></tbody>
</table>## Unbound Technology provider properties

<table id="table_m43_lvj_nsb"><tbody><tr><td>

edgeencryption.ekm.provider.classname

</td><td>

Internal class name for the implementation.**Warning:** Do not change this property.

</td></tr><tr><td>

edgeencryption.thirdparty.vendor.library.path

</td><td>

Path to the Unbound API JAR file on the Unbound client machine.

</td></tr><tr><td>

edgeencryption.ekm.provider.rsa.wrapping.key.alias

</td><td>

Wrapping key alias in the Unbound Technology implementation. Must be the same for all proxies.

</td></tr></tbody>
</table>## User account properties

<table id="table_zgv_ltj_nsb"><tbody><tr><td>

edgeencryption.target.username

</td><td>

User name that the proxy uses to log in to the instance. The user must have the edge\_encryption role. See [Set up an Edge Encryption user account](../task/t_SetupEdgeEncryptionUser.md).

</td></tr><tr><td>

edgeencryption.target.password

</td><td>

Password that the proxy uses to log in to the instance.

</td></tr></tbody>
</table>## Web proxy properties

<table id="table_c4s_55j_nsb"><tbody><tr><td>

edgeencryption.webproxy.host

</td><td>

Web proxy name or IP address.

</td></tr><tr><td>

edgeencryption.webproxy.port

</td><td>

Port on the web proxy.

</td></tr><tr><td>

edgeencryption.webproxy.user

</td><td>

User name used to connect to the web proxy. If your web proxy does not use authentication, leave this property commented out.

</td></tr><tr><td>

edgeencryption.webproxy.password

</td><td>

Password to use to connect to the web proxy. If your web proxy does not use authentication, leave this property commented out.

</td></tr></tbody>
</table>## Deprecated proxy encryption properties

-   **edgeencryption.encrypter.default.key128**

    Specifies the name of the current AES 128 key. An AES 128 key must be available even if it is not used. Must be the same for all proxies.

    Perform maintenance of these keys on the instance.

-   **edgeencryption.encrypter.default.key256**

    Specifies the name of the current AES 256 key. Must be the same for all proxies.

    Perform maintenance of these keys on the instance.

-   **edgeencryption.encrypter.key**

    Specifies the key name for each key and is used to specify the default keys. This is the key alias integrated with the metadata that is included with each encrypted item and, therefore, is stored on the instance. The key name must use lowercase letters.

-   **edgeencryption.encrypter.type**

    Specifies the type of encryption keystore system.

-   **edgeencryption.encrypter.file**

    Specifies the path and file name of the text file associated with the key.

-   **edgeencryption.encrypter.password**

    Specifies the password for accessing the keystore.


**Parent Topic:**[Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md)

