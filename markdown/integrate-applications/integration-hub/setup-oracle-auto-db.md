---
title: Set up the Oracle Autonomous DB spoke
description: Integrate the ServiceNow instance and Oracle Autonomous DB by using the credentials to authenticate ServiceNow requests.Create a credential record for the Oracle Cloud IAM account. The Oracle Cloud IAM spoke connection and credential alias uses these credentials to authorize actions.Modify the short description to provide spoke specific information.Create a connection record for your Oracle Cloud IAM account. The Oracle Cloud IAM spoke connection and credential aliases use these connections to perform actions in Oracle Cloud IAM.Create a credential record for the Oracle Autonomous DB account. The Oracle Autonomous DB spoke connection and credential alias uses these credentials to authorize actions.Modify the short description to provide spoke specific information.Create a connection record for your Oracle Autonomous DB account. The Oracle Autonomous DB spoke connection and credential aliases use these connections to perform actions in Oracle Autonomous DB.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Oracle Autonomous DB Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Oracle Autonomous DB spoke

Integrate the ServiceNow instance and Oracle Autonomous DB by using the  credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate and set up the [Oracle Cloud IAM Spoke](../concept/oracle-iam.md).
-   Activate the Oracle Autonomous DB spoke.
-   Role required: admin.

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
    |Key ID|Key ID helps identify which key is used when multiple keys are used to sign tokens. The Key ID must be slash \(/\) separated values of Tenancy OCID, User OCID, and Fingerprint in this format: `ocid1.tenancy.oc1..<unique_ID>/ocid1.user.oc1..<unique_ID>/<key_fingerprint>`.|
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
    |Host|Fully qualified domain name of the target host where the **Oracle Cloud IAM** server is hosted. For example, `database.ap-mumbai-1.oraclecloud.com` .|
    |Connection URL|Base URL to connect to **Oracle Cloud IAM**. For example, `https://database.ap-mumbai-1.oraclecloud.com`.|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|
    |Override default port|Target port used by the connection. If blank, the system uses the default port.|
    |Use MID server|Option to use a MID Servers for this connection. If the check box is selected, define the fields in the Advanced MID Server Configuration related list.|

5.  Click **Submit**.


## Create a credential record for the Oracle Autonomous DB spoke

Create a credential record for the Oracle Autonomous DB account. The Oracle Autonomous DB spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

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
    |Key ID|Key ID \(kid\) helps identify which key is used when multiple keys are used to sign tokens. The Key ID must be slash \(/\) separated values of Tenancy OCID, User OCID, and Fingerprint in this format: ocid1.tenancy.oc1..&lt;unique\_ID&gt;/ocid1.user.oc1..&lt;unique\_ID&gt;/&lt;key\_fingerprint&gt;.|
    |Applies to|Option to specify if the credential applies to all MID Servers in the network.|
    |Active|Option to actively use the credential record.|
    |Credential alias|Associated credential record. If you have already created a credential alias, search and select the record.|
    |Authentication Algorithm|Custom authentication algorithm for outbound signing requests. Select `OCI SHA256RSA Signing Algorithm`|

5.  Right-click the form header and click **Submit**.


## Create a connection record for the Oracle Autonomous DB spoke

Create a connection record for your Oracle Autonomous DB account. The Oracle Autonomous DB spoke connection and credential aliases use these connections to perform actions in Oracle Autonomous DB.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record for **Oracle Autonomous Database**.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Oracle Auto DB Connection`.|
    |Credential|Credential record created for Oracle Autonomous DB spoke. For example, `Oracle ADB Creds`.|
    |Connection alias|Alias record associated with this connection. Search and select `sn_oci_adb_spoke.Oracle_Autonomous_Database`|
    |Host|Fully qualified domain name of the target host where the **Oracle Autonomous DB** server is hosted. For example, `database.ap-mumbai-1.oraclecloud.com` .|
    |Connection URL|Base URL to connect to **Oracle Autonomous DB**. For example, `https://database.ap-mumbai-1.oraclecloud.com`.|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|
    |Override default port|Target port used by the connection. If blank, the system uses the default port.|
    |Use MID server|Option to use a MID Servers for this connection. If the check box is selected, define the fields in the Advanced MID Server Configuration related list.|

5.  Click **Submit**.


