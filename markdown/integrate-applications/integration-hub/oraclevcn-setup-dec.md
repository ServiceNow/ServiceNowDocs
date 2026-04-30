---
title: Set up the Oracle Virtual Cloud Network spoke
description: Integrate the ServiceNow instance and Oracle Virtual Cloud Network account by using the OCI SHA256WithRSA Signature credentials to authenticate ServiceNow requests.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Oracle Virtual Cloud Network Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Oracle Virtual Cloud Network spoke

Integrate the ServiceNow instance and Oracle Virtual Cloud Network account by using the OCI SHA256WithRSA Signature credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate and set up the [Oracle Cloud IAM Spoke](../concept/oracle-iam.md).
-   Activate the Oracle Virtual Cloud Network spoke.
-   Role required: admin.

## Procedure

1.  Create a JKS certificate.

    You can create a JKS certificate for the Oracle Virtual Cloud Network spoke or use the certificate created for the Oracle Cloud IAM spoke. For information about creating the JKS Certificate, see [Create a Java KeyStore \(JKS\) certificate](setup-oracle-iam.md#).

2.  Create X.509 certificate.

    You can create a X.509 certificate for the Oracle Virtual Cloud Network spoke or use the certificate created for the Oracle Cloud IAM spoke. For information about creating a X.509 certificate, see [Create X.509 certificate for the Oracle Cloud IAM spoke](setup-oracle-iam.md#).

3.  Create credential record for the Oracle Virtual Cloud Network spoke.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Click **New**.

        The system displays this message: `What type of Credentials would you like to create?`

    3.  Select **OCI SHA256WithRSA Signature**.

    4.  On the form, fill these values.

        **Note:** You can specify details of the certificates you created specifically for the Oracle Virtual Cloud Network spoke or specify details of the existing certificates you had created for the Oracle Cloud IAM spoke.

        |Field|Description|
        |-----|-----------|
        |Name|Name to uniquely identify the record. For example, `Oracle Virtual Cloud Network Cred`.|
        |Certificate Sys ID|Sys ID of the Signing Certificate.|
        |Alias|Alias of the KeyStore.|
        |Alias Password|Alias password of the KeyStore.|
        |Key ID|Key ID helps identify which key is used when multiple keys are used to sign tokens. The Key ID must be slash \(/\) separated values of Tenancy OCID, User OCID, and Fingerprint in this format:`ocid1.tenancy.oc1..<unique_ID>/ocid1.user.oc1..<unique_ID>/<key_fingerprint>`.|
        |Applies to|Option to specify if the credential applies to all MID Servers in the network.|
        |Active|Option to actively use the credential record.|
        |Authentication Algorithm|Custom authentication algorithm for outbound signing requests. Select `OCI SHA256RSA Signing Algorithm`|

    5.  Right-click the form header and click **Submit**.

4.  Create connection record for the Oracle Virtual Cloud Network spoke.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Open the alias record of the Oracle Virtual Cloud Network spoke, for example, **Oracle\_VCN\_Connection**.

    3.  From the **Connections** tab, click **New**.

    4.  On the form, fill these fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name to uniquely identify the record. For example, `Oracle_VCN_Conn`.|
        |Credential|Credential record created for Oracle Virtual Cloud Network spoke. For example, `Oracle Virtual Cloud Network Cred`.|
        |Connection alias|Alias record associated with this connection.|
        |Connection URL|Base URL to connect to Oracle Virtual Cloud Network. For example, `https://iaas.ap-mumbai-1.oraclecloud.com`.|
        |Active|Option to actively use the connection record.|
        |Domain|Domain that the action runs in.|

    5.  Click **Submit**.

    The ServiceNow instance and Oracle Virtual Cloud Network account are integrated. You can use the spoke actions to build flows and automate tasks as required.


