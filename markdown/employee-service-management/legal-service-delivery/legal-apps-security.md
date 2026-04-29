---
title: Security in Legal Service Delivery
description: Legal Service Delivery provides security through various ServiceNow AI Platform security features such as Restricted Caller Access, Encryption Support, and Edge Encryption.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Security in Legal Service Delivery

Legal Service Delivery provides security through various ServiceNow AI Platform security features such as Restricted Caller Access, Encryption Support, and Edge Encryption.

## Restricted caller access for Legal Service Delivery

Restricted caller access \(RCA\) privilege settings define cross-scope access to an application, application resource \(for example, access control role, business rule, UI action, script include\), event, or to allow or deny requests for access. Using RCA, the administrators can track cross-scope applications or scripts that request access to a Legal Service Delivery application, application resources, or events and secure sensitive information in scoped tables and script includes.

The **Scoped Application Restricted Caller Access \[com.glide.scope.access.restricted\_caller\]** plugin is activated during the Legal Service Delivery application installation or upgrade.

When you define cross-scope access to an application resource, use the following settings:

-   **Caller tracking**

    This setting is recommended for the development stage. Access is allowed to the tables and script includes, but tracked in the Restricted Caller Access table. Access information can be viewed from **Application Restricted Caller Access**.

-   **Caller restriction**

    This setting is recommended for the production phase after development is complete.


For more information, refer to [Define cross-scope access to an application resource](https://www.servicenow.com/docs/access?context=set-RCA-level&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Encryption for Legal Service Delivery

Legal Service Delivery provides encryption to secure sensitive information.

Encryption prevents unauthorized users viewing specific fields. To encrypt fields in Legal Service Delivery, Column Level Encryption is activated by default and provides role-based encryption functions.

For more information on encryption, see Field Encryption.

## Edge Encryption for Legal Service Delivery

ServiceNow® Edge Encryption ™ encrypts sensitive data on your company premises before sending it over the internet to your ServiceNow instance \(encrypted in flight\), where it remains encrypted at rest.

For more information, see [Understanding Edge Encryption](https://www.servicenow.com/docs/access?context=c_EdgeEncryptionOverview&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Because edge encryption is enabled on a proxy server on your side of the network, there is significant planning, network administration and management, and setup required. For more information, see [Planning for Edge Encryption](https://www.servicenow.com/docs/access?context=c_EdgeEncryptionPlanning&version=australia&pubname=australia-platform-security&ft:locale=en-US).

To install edge encryption, see [Edge Encryption installation](https://www.servicenow.com/docs/access?context=c_InstallEdgeEncryptionProxy&version=australia&pubname=australia-platform-security&ft:locale=en-US).

To configure edge encryption, see [Edge Encryption configuration](https://www.servicenow.com/docs/access?context=edge-config&version=australia&pubname=australia-platform-security&ft:locale=en-US).

You can encrypt columns \(fields\) or attachments associated with tables. See [Encrypt fields using encryption configurations](https://www.servicenow.com/docs/access?context=c_ConfigureCloudEdge&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Note:** There are limitations when using edge encryption. See [Edge Encryption limitations](https://www.servicenow.com/docs/access?context=edge-encryption-limitations&version=australia&pubname=australia-platform-security&ft:locale=en-US).

