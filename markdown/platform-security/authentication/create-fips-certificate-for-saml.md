---
title: Create self-signed BCFKS keystore for SAML
description: Generate a FIPS 140-2 compliant self-signed BCFKS keystore for use in SAML signing and encryption operations within the Multi-Provider SSO plugin.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [\(Optional\) Set keystore properties for signing logout requests for SAML, Service Provider \(SP\) system properties, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Create self-signed BCFKS keystore for SAML

Generate a FIPS 140-2 compliant self-signed BCFKS keystore for use in SAML signing and encryption operations within the Multi-Provider SSO plugin.

## Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

Do the following:

-   Install Java on your machine and the key tool command-line tool accessible in your terminal \(or "command prompt" if you are running it on a windows machine\).
-   Perform the following steps to create a keystore using FIPS-approved cryptographic algorithms \(such as RSA 2048-bit or higher paired with SHA-256\) that meets federal security requirements for identity federation and single sign-on implementations.

## Procedure

1.  Download the [FIPS Provider Library](https://www.bouncycastle.org/download/bouncy-castle-java-fips/#latest).

    **Note:**

    Use the latest version `bc-fips-2.1.0.jar`. Make sure you use the most recent version.

2.  Generate the FIPS-compliant keystore and certificate.

    1.  Run the following key tool command to generate a self-signed certificate and keystore.

<table id="table_ozs_52s_d3c"><thead><tr><th>

Running on Linux/macOS

</th><th>

Running on Windows:

</th></tr></thead><tbody><tr><td>

```
keytool -genkeypair \
  -providername BCFIPS \
  -providerclass org.bouncycastle.jcajce.provider.BouncyCastleFipsProvider \
  -providerpath <path_to_bc-fips-<version>>.jar \
  -alias <key_alias> \
  -keyalg RSA \
  -keysize <key_size> \
  -keystore <keystore_name>.bcfks \
  -validity <validity> \
  -storetype BCFKS \
  -storepass <keystore_password>
```

</td><td>

```
keytool -genkeypair ^
-providername BCFIPS ^
-providerclass org.bouncycastle.jcajce.provider.BouncyCastleFipsProvider ^
-providerpath <path_to_bc-fips-<version>>.jar ^
-alias <key_alias> ^
-keyalg RSA ^
-keysize <key_size> ^
-keystore <keystore_name>.bcfks ^
-validity <validity> ^
-storetype BCFKS ^
-storepass <keystore_password>
```

</td></tr></tbody>
</table>    2.  Replace placeholders `(<...>)` with appropriate values:

        -   `<path_to_bc-fips-<version>>.jar`: Path to `bc-fips-<version>.jar`
        -   `<key_alias>`: Alias for the key pair
        -   `<key_size>`: 2048 or 4096
        -   `<keystore_name>.bcfks`: Desired file name for the keystore
        -   `<validity>`: Expiry in days
        -   `<keystore_password>`: Password for the keystore
    3.  Follow the prompts to enter additional DN \(Distinguished Name\) details for the certificate.

        **Note:** When you are prompted for a password for the key \(alias\), press the Enter or Return key to use the same password you used for the keystore. Do not give a different password.

    4.  Securely store the key alias and keystore password.

        Provide these credentials while:

        -   Creating the `sys_certificate` record for this keystore.
        -   Configuring the SAML Identity Provider to provide the signing key or encryption key alias and password.
        **Note:** The key password is same as the keystore password specified during creation. Use the same password when configuring signing or encryption for the SAML Identity Provider.

3.  Extract the Certificate Chain.

<table id="table_lmx_yfs_d3c"><thead><tr><th>

Running on Linux/macOS

</th><th>

Running on Windows:

</th></tr></thead><tbody><tr><td>

```
keytool -exportcert \
  -provider org.bouncycastle.jcajce.provider.BouncyCastleFipsProvider \
  -providerpath <path_to_bc-fips-<version>>.jar \
  -storetype BCFKS \
  -keystore <keystore_name>.bcfks \
  -storepass <keystore_password> \
  -alias <key_alias> \
  -rfc \
  -file <file_name>.cer
```

</td><td>

```
keytool -exportcert ^
-provider org.bouncycastle.jcajce.provider.BouncyCastleFipsProvider ^
-providerpath <path_to_bc-fips-<version>>.jar ^
-storetype BCFKS ^
-keystore <keystore_name>.bcfks ^
-storepass <keystore_password> ^
-alias <key_alias> ^
-rfc ^
-file <file_name>.cer
```

</td></tr></tbody>
</table>    Replace placeholders `(<...>)` with appropriate values:

    -   `<path_to_bc-fips-<version>>.jar`: Path to `bc-fips-<version>.jar`
    -   `<keystore_name>.bcfks`: keystore file name as given in previous step
    -   `<keystore_password>`: keystore password as given in previous step
    -   `<key_alias>`: Key alias as given in previous step
    -   `<file_name>.cer`: Desired file name for the extracted certificate in PEM format
4.  Create a record on `sys_certificate` table.

    1.  Log in to ServiceNow AI Platform.

    2.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Administration** &gt; **x509 Certificate**.

    3.  Click **New** to create a record.

    4.  Select **BCFKS keystore** as Type.

    5.  Attach the generated BCFKS keystore file `(<keystore_name>.bcfks)`.

        **Note:** To configure certificate expiry notification, use **Notify on expiration** and **Groups to notify on expiration**, and set the notification timing using **Warn in days to expire** and **Frequency**.

    6.  Fill in other required fields, including the keystore password provided during keystore creation.

    7.  Click **Validate Stores/Certificates** related link to ensure the keystore is valid.

    8.  Copy the `sys_id` of this record.


