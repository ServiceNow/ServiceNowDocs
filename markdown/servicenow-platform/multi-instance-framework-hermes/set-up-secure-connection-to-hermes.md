---
title: Set up a secure connection to the Hermes Messaging Service
description: Secure your Kafka topics by generating a ServiceNow instance-signed certificate.
locale: en-US
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up a secure connection to the Hermes Messaging Service

Secure your Kafka topics by generating a ServiceNow® instance-signed certificate.

## Before you begin

Setting up the Hermes Messaging Service requires coordination with your network administrator and with your Kafka administrator. Work with your network administrator to obtain required security certificates and open the required ports. Work with your Kafka administrator to ensure that your Kafka environment is configured correctly and that your applications can connect to the Hermes Messaging Service using the standard Kafka protocol.

Make sure the following setup is in place:

-   The Hermes Messaging Service is activated. See [Activating the Hermes Messaging Service](../concept/hermes-messaging-service-activation.md).
-   The Key Management Framework plugin \(com.glide.kmf.global\) is activated.
-   The Certificates \[sys\_kmf\_certificate\] table contains a ServiceNow instance root CA certificate.
-   The instance isn't configured with a Custom URL. Custom URLs are not supported with the Instance PKI Certificate Generator.

Role required: hermes\_admin, sn\_kmf.cryptographic\_manager, or admin

For details on assigning KMF roles, see [Roles installed with Key Management Framework](https://www.servicenow.com/docs/access?context=kmf-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Certificate Generator** &gt; **Instance PKI Certificate Generator**.

2.  Control access to topics by configuring Access Control Lists \(ACLs\) at the namespace or topic-level.

<table id="choicetable_ebz_1jn_zyb"><thead><tr><th align="left" id="d372397e128">

Option

</th><th align="left" id="d372397e131">

Description

</th></tr></thead><tbody><tr><td id="d372397e137">

**Apply ACLs to namespaces**

</td><td>

1.  Select **Configure ACLs**.
2.  In the Topic ACLs dialog box, select **Namespaces**.
3.  Enter a namespace that you want to configure.
4.  Set the permission level by selecting either **Read Only** or **Read/Write**.
5.  Select **Add**.


</td></tr><tr><td id="d372397e179">

**Apply ACLs to defined topics**

</td><td>

1.  Select **Configure ACLs**.
2.  In the Topic ACLs dialog box, select **Defined topics**.
3.  Enter an existing topic that you want to configure.
4.  Set the permission level by selecting either **Read Only** or **Read/Write**.
5.  Select **Add**.


</td></tr></tbody>
</table>    The bearer of the certificate is granted read or read/write access to the topics in the namespace or the existing topic that you selected.

3.  Set up security for the Hermes Messaging Service.

    1.  Navigate back to the Instance PKI Certificate Generator page.

    2.  Enter a keystore password in the **Certificate Password** field.

    3.  Select **Generate**.

    The system generates an instance-signed certificate in the Certificates \[sys\_kmf\_certificate\] table, creates a keystore, and creates a truststore.

    If Restricted Caller Access isn't allowed for the IPKI Certificate Generator, a cross scope access error appears. Contact Customer Service and Support for assistance with allowing Restricted Caller Access. To resolve this issue, Customer Service and Support can reference source\_scope=76f9d51369115083f4ea77aab1677cc0 in the Restricted Caller Access Privileges \[sys\_restricted\_caller\_access\] table.

4.  Save a copy of the keystore by selecting **Download Keystore**.

5.  Save a copy of the truststore by selecting **Download Truststore**.

6.  Copy the keystore and truststore files to each producer and consumer client that will connect to the Hermes Messaging Service.


## Result

You can now create a secure connection to the Hermes Messaging Service.

**Note:** You must use the keystore that you generated using the Instance PKI Certificate Generator to connect to Hermes. Custom-generated keystores that aren't created according to the ServiceNow documentation aren't supported.

## What to do next

-   Review the guidance in [Exchanging data using Hermes](../concept/exchanging-data-hermes-messaging-service.md).
-   [Prepare your Apache Kafka client environment](prepare-kafka-client-environment.md)
-   Configure the SSL connection to Hermes in the producer and consumer properties files using the truststore and keystore files that you generated. For more information, refer to the following topics:
    -   [Create a test topic in Hermes using the Kafka client](create-hermes-topic.md)
    -   [Produce test messages to a Hermes topic using the Kafka client](produce-messages-hermes.md)
    -   [Consume test messages from a Hermes topic using the Kafka client](consume-messages-hermes.md)

**Parent Topic:**[Configuring Hermes Messaging Service](../concept/configuring-hermes-messaging-service.md)

**Related topics**  


[Activating the Hermes Messaging Service](../concept/hermes-messaging-service-activation.md)

[Revoke a Hermes certificate](revoke-certificate.md)

[Restricting access to Hermes](../concept/restricting-access-hermes-topics.md)

