---
title: Add SSL certificates for the MID Server
description: Configure the MID Server to connect to a source over SSL.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
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
-   Specify a different TrustStore file for the MID Server to use. For more information, see [Specify an external TrustStore for the MID Server](mid-external-truststore.md).

Review both methods to evaluate which best meets your needs.

During MID upgrade the bundled TrustStore is overwritten. The MID Server attempts to migrate certificates from the existing TrustStore to the incoming one. To be migrated, certificates must meet the following criteria:

-   **Quebec \(backported to Orlando Patch 10 and Paris Patch 4\)**
    -   X.509 v3 certificates
    -   Basic Constraints Extension evaluates to false \(or is not present\)
-   **Rome \(backported to Paris Patch 7 and Quebec Patch 2\)**
    -   X.509 certificates
    -   Any certificate present in the source, but not the destination TrustStore

Certificates that do not meet the criteria are overwritten. Alternatively, you can specify an external TrustStore file which is unaffected by MID Server upgrades. For more information, see [Specify an external TrustStore for the MID Server](mid-external-truststore.md)

In Rome and later families, the migration strategy utilized during upgrade is configurable via the MID Server configuration parameter **mid.truststore.migration.strategy**. It can take the following values:

-   **migrate\_delta**: the default strategy \(outlined above for Rome\)
-   **migrate\_non\_ca**: a strategy matching the one outlined above for the Quebec family
-   **do\_not\_migrate**: disables the TrustStore migration during upgrade, though a backup of the original TrustStore is made in the event of overwrite

During this migration process, a backup of the original and upgrade TrustStores are made and stored in the agent’s work directory: `…\agent\work\truststore_migration\<time epoch seconds>\`. The original TrustStore is renamed to `cacerts_before` and the upgrade TrustStore is renamed to `cacerts_from_upgrade`.

## Procedure

1.  Open a command prompt and navigate to the folder containing the JRE [keytool](https://docs.oracle.com/javase/6/docs/technotes/tools/solaris/keytool.html).

    This is the location of the JRE bundled with the MID Server. An example path might be: `C:\Mid Server\agent\jre\bin`

2.  Import a certificate into the MID Server's cacerts keystore, using this command:

    `keytool -import -alias <certificate alias> -file "<path to certificate>" -keystore "<path to the MID Server bundled JRE>\lib\security\cacerts"`

    For example, you might enter: `keytool -import -alias MyCA -file "C:\myca.cer" -keystore "C:\Mid Server\agent\jre\lib\security\cacerts"`

    **Note:** The keytool prompts you for a certificate password. If the certificate is for a CA, the keytool also asks whether to trust the certificate authority. To add a certificate to an instance, see Upload a certificate to an instance.

3.  Display a list of the current certificates by running the command: `keytool.exe -list -keystore "C:\Mid Server\agent\jre\lib\security\cacerts"`


**Parent Topic:**[Securing and encrypting MID Server data](../concept/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies](../concept/mid-security-checks.md)

[Encrypt or decrypt MID Server configuration file values](mid-server-manual-encryption.md)

[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

[MID Server authentication credentials and SOAP requests](../concept/mid-authentication-soap-requests.md#)

[MID Server unified key store](../concept/mid-unified-keystore.md#)

[Enable MID Server mutual authentication](install-mid-mutual-auth.md)

[MID Server Azure Key Vault integration](mid-azure-key-vault-integration.md#)

[MID Server command audit log](../concept/mid-audit-log.md)

[Rekey a MID Server](t_RekeyAMIDServer.md)

[Specify an external TrustStore for the MID Server](mid-external-truststore.md)

[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)

[Attach a script file to a file synchronized MID Server](mid-server-script-attach.md#)

[MID Server FIPS Enforced Mode](../concept/mid-fips-enforced.md#)

[MID Server Governance](../concept/mid-timeout.md)

