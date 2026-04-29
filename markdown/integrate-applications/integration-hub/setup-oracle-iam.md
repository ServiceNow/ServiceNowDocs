---
title: Set up the Oracle Cloud IAM spoke
description: Integrate the ServiceNow instance and Oracle Cloud IAM by using the OCI SHA256WithRSA Signature credentials to authenticate ServiceNow requests.Use the keytool utility to generate, import, and export certificates.You must create a X.509 certificate and attach the Java Keystore file to it. This certificate is used for connecting to Oracle Cloud IAM.Create a credential record for the Oracle Cloud IAM account. The Oracle Cloud IAM spoke connection and credential alias uses these credentials to authorize actions.Modify the short description to provide spoke specific information.Create a connection record for your Oracle Cloud IAM account. The Oracle Cloud IAM spoke connection and credential aliases use these connections to perform actions in Oracle Cloud IAM.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Oracle Cloud IAM Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Oracle Cloud IAM spoke

Integrate the ServiceNow instance and Oracle Cloud IAM by using the OCI SHA256WithRSA Signature credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Oracle Cloud IAM spoke.
-   Role required: admin

## Create a Java KeyStore \(JKS\) certificate

Use the keytool utility to generate, import, and export certificates.

### Before you begin

-   Make sure that the keytool utility is installed on your computer.
-   Role required: admin

### Procedure

1.  Change to the directory where the certificate is to be saved.

    By default, keytool creates a keystore file in the directory where the keystore commands are run.

2.  Enter the following keytool command to generate the certificate in the keystore file, keystore.jks:

    `keytool -genkeypair -alias <mycertificate> -keyalg RSA -keysize 2048 -validity 365 -keystore keystore.jks -storepass your_keystore_password -keypass your_key_password`

    **Note:** Replace the placeholders &lt;mycertificate&gt;, &lt;your\_keystore\_password&gt;, and &lt;your\_key\_password&gt; with your certificate name, keystore password, and key password in all the sample commands.

3.  Enter your first name and last name, organization, and other details in the keytool prompt.

    These details are required for generating the certificate.

4.  Enter the following commands in the following sequence.

    ```
    keytool -export -alias sample -storepass <storepassword> -file server.cer -keystore keystore.jks
    keytool -import -v -trustcacerts -alias sample -file server.cer -keystore cacerts.jks -keypass <keypassword> -storepass <storepassword>
    keytool -export -alias sample -keystore keystore.jks -rfc -file public.cert
    keytool -export -alias sample -keystore keystore.jks -rfc -file certificate.pem
    keytool -list -rfc -keystore keystore.jks -alias sample -storepass <storepassword>
    keytool -importkeystore -srckeystore keystore.jks -destkeystore keystore.p12 -deststoretype PKCS12 -srcalias <alias> -deststorepass <storepassword> -destkeypass <keypassword>
    openssl pkcs12 -in keystore.p12 -nokeys -out cert.pem
    openssl pkcs12 -in keystore.p12 -nodes -nocerts -out PrivateKey.pem
    openssl rsa -in key.pem -pubout -out PublicKey.pem
    keytool -list -v -keystore keystore.p12 -storetype PKCS12 -storepass <storepassword>
    ```

    Verify the generated keystore.jks file in the target directory.

5.  Enter the following command to extract public key from the Java Keystore file.

    `openssl x509 -pubkey -noout -in cert.pem > publickey.pem`


## Create X.509 certificate for the Oracle Cloud IAM spoke

You must create a X.509 certificate and attach the Java Keystore file to it. This certificate is used for connecting to Oracle Cloud IAM.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Click **New**.

3.  In the form, fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the certificate. For example, `OCI IAM certificate`|
    |Type|Type of the certificate. Select **Java Key Store**.|
    |Notify on expiration|List of persons who are to be notified when a ceritificate is about to expire.|
    |Keystore password|Password of the keystore.|
    |Warn in days to expire|Number of days when a warning is sent to the user before the certificate expires.|
    |Active|Option to make the certificate active.|
    |Short description|Short description for the keystore.|

4.  Click the attachments icon and upload the keystore.jks file.

5.  Click **Validate Stores/Certificates**.


## Create a credential record for the Oracle Cloud IAM spoke

Create a credential record for the Oracle Cloud IAM account. The Oracle Cloud IAM spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Use the public key from the Java Keystore \(JKS\) file and generate a fingerprint from your Oracle Cloud account. For more information about fingerprint, see [Required Keys and OCIDs](https://docs.cloud.oracle.com/en-us/iaas/Content/API/Concepts/apisigningkey.htm#three).

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **OCI SHA256WithRSA Signature**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, Oracle IAM Cloud Cred.|
    |Certificate Sys ID|Sys ID of the OCI Signing Certificate.|
    |Alias|Alias of the KeyStore.|
    |Alias Password|Alias password of the KeyStore.|
    |Key ID|Key ID helps identify which key is used when multiple keys are used to sign tokens. The Key ID must be slash \(/\) separated values of Tenancy OCID, User OCID, and Fingerprint in this format:`ocid1.tenancy.oc1..<unique_ID>/ocid1.user.oc1..<unique_ID>/<key_fingerprint>`.|
    |Applies to|Option to specify if the credential applies to all MID Servers in the network.|
    |Active|Option to actively use the credential record.|
    |Authentication Algorithm|Custom authentication algorithm for outbound signing requests. Select `OCI SHA256RSA Signing Algorithm`|

5.  Right-click the form header and click **Submit**.


## Create a connection record for the Oracle Cloud IAM spoke

Create a connection record for your Oracle Cloud IAM account. The Oracle Cloud IAM spoke connection and credential aliases use these connections to perform actions in Oracle Cloud IAM.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record for **OracleIAM\_credentialANDconnecton**.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Oracle IAM conn`.|
    |Credential|Credential record created for Oracle Autonomous DB spoke. For example, `Oracle IAM Cred`.|
    |Connection alias|Alias record associated with this connection. Search and select `sn_oci_iam_spoke.OracleIAM_credentialAN`|
    |Connection URL|Base URL to connect to **Oracle Cloud IAM**. For example, `https://database.ap-mumbai-1.oraclecloud.com`.|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|

5.  Click **Submit**.


