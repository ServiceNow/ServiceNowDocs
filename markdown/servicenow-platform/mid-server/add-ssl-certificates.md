---
title: Add SSL certificates for the MID Server
description: Configure the MID Server to connect to a source over SSL.The MID Server JVM can utilize a TrustStore external to the MID installation directory so any certificates added to the TrustStore are not overwritten during an upgrade. It is important that this TrustStore file reside outside of the MID installation directory, and the Truststore location can be specified by adding additional parameters to the MID Server's wrapper-override.conf file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/add-ssl-certificates.html
release: brazil
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Add SSL certificates for the MID Server

Configure the MID Server to connect to a source over SSL.

## Before you begin

Role required: admin

<table id="table_kvf_3v4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>## About this task

You can add certificates to the MID Server to communicate over SSL/TLS in one of two ways:

-   Add certificates directly to the bundled JRE TrustStore file, using the following procedure.
-   Specify a different TrustStore file for the MID Server to use. For more information, see [Specify an external TrustStore for the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/mid-server/add-ssl-certificates.md).

Review both methods to evaluate which best meets your needs.

During MID upgrade the bundled TrustStore is overwritten. The MID Server attempts to migrate certificates from the existing TrustStore to the incoming one. To be migrated, certificates must meet the following criteria:

-   **Quebec \(backported to Orlando Patch 10 and Paris Patch 4\)**
    -   X.509 v3 certificates
    -   Basic Constraints Extension evaluates to false \(or is not present\)
-   **Rome \(backported to Paris Patch 7 and Quebec Patch 2\)**
    -   X.509 certificates
    -   Any certificate present in the source, but not the destination TrustStore

Certificates that do not meet the criteria are overwritten. Alternatively, you can specify an external TrustStore file which is unaffected by MID Server upgrades. For more information, see [Specify an external TrustStore for the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/mid-server/add-ssl-certificates.md)

In Rome and later families, the migration strategy utilized during upgrade is configurable via the MID Server configuration parameter **mid.truststore.migration.strategy**. It can take the following values:

-   **migrate\_delta**: the default strategy \(outlined above for Rome\)
-   **migrate\_non\_ca**: a strategy matching the one outlined above for the Quebec family
-   **do\_not\_migrate**: disables the TrustStore migration during upgrade, though a backup of the original TrustStore is made in the event of overwrite

During this migration process, a backup of the original and upgrade TrustStores are made and stored in the agent’s work directory: `…\agent\work\truststore_migration\<time epoch seconds>\`. The original TrustStore is renamed to `cacerts_before` and the upgrade TrustStore is renamed to `cacerts_from_upgrade`.

When switching to an external TrustStore, import all certificates from the bundled TrustStore into it. The MID Server might fail to start if a required certificate is missing from the new TrustStore.

## Procedure

1.  Open a command prompt and navigate to the folder containing the JRE [keytool](https://docs.oracle.com/javase/6/docs/technotes/tools/solaris/keytool.html).

    This is the location of the JRE bundled with the MID Server. An example path might be: `C:\Mid Server\agent\jre\bin`

2.  Import a certificate into the MID Server's cacerts keystore, using this command:

    `keytool -import -alias <certificate alias> -file "<path to certificate>" -keystore "<path to the MID Server bundled JRE>\lib\security\cacerts"`

    For example, you might enter: `keytool -import -alias MyCA -file "C:\myca.cer" -keystore "C:\Mid Server\agent\jre\lib\security\cacerts"`

    **Note:**

    The keytool utility prompts you for the TrustStore password. The default password for the MID Server bundled JRE TrustStore `cacerts` is `changeit`. If the default password has been changed, enter the current password. Don't change the TrustStore password unless your security policy requires it.

    If the certificate is for a CA, the keytool also asks whether to trust the certificate authority. To add a certificate to an instance, see [Upload a certificate to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/t_UploadACertificateToAnInstance.md).

3.  Display a list of the current certificates by running the command: `keytool.exe -list -keystore "C:\Mid Server\agent\jre\lib\security\cacerts"`


**Parent Topic:**[Securing and encrypting MID Server data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/mid-server/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies]()

[Encrypt or decrypt MID Server configuration file values]()

[MID Server configuration file security]()

[MID Server authentication credentials and SOAP requests]()

[MID Server unified key store]()

[Enable MID Server mutual authentication]()

[MID Server Azure Key Vault integration]()

[MID Server command audit log]()

[Rekey a MID Server]()

[MID Server SSH cryptographic algorithms]()

[Attach a script file to a file synchronized MID Server]()

[MID Server FIPS Enforced Mode]()

[MID Server Governance]()

## Specify an external TrustStore for the MID Server

The MID Server JVM can utilize a TrustStore external to the MID installation directory so any certificates added to the TrustStore are not overwritten during an upgrade. It is important that this TrustStore file reside outside of the MID installation directory, and the Truststore location can be specified by adding additional parameters to the MID Server's `wrapper-override.conf` file.

### Before you begin

Role required: admin

### Procedure

1.  In the MID Server host, navigate to the `wrapper-override.conf` file.

2.  Specify an external TrustStore by appending a custom parameter to the end of your MID’s `wrapper-override.conf` file.

    For example, on a Windows MID with an external TrustStore found at `C:\external_truststore\cacerts`, the end of the file would appear similar to:

    ```
    # Add additional custom parameters below
    
    wrapper.java.additional.3=-Djavax.net.ssl.trustStore=C:\external_truststore\cacerts
    
    wrapper.java.additional.4=-Djavax.net.ssl.trustStorePassword=<truststore’s password>
    ```

    **Note:** If you have specified other additional parameters in this file then the numerical identifier, in this case 3 and 4, may differ.


