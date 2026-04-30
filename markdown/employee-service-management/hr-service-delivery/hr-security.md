---
title: HR security
description: HR Service Delivery provides Restricted Caller Access, Encryption Support, and Edge Encryption security features.Restricted caller access \(RCA\) defines cross-scope access to HR Service Delivery applications.HR Service Delivery and Employee Document Management provides encryption to secure sensitive information.HR Service Delivery and Employee Document Management provides edge encryption to secure sensitive information.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR security

HR Service Delivery provides Restricted Caller Access, Encryption Support, and Edge Encryption security features.

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

## Restricted caller access for HR

Restricted caller access \(RCA\) defines cross-scope access to HR Service Delivery applications.

RCA is available to help secure sensitive information in HR scoped tables and script include APIs. Without RCA, tables that are not private to a scope are susceptible to queries by any server-side script.

The **Scoped Application Restricted Caller Access \[com.glide.scope.access.restricted\_caller\]** plugin is activated during the HR application installation or upgrade.

-   **Caller tracking**

    This setting is recommended for the development stage. Access is allowed to tables and script includes, but tracked in the Restricted Caller Access table. Access information can be viewed from **Application Restricted Caller Access**.

-   **Caller restriction**

    This setting is recommended for the production phase after development is complete.


To define cross-scope access to an application resource, refer to [Define cross-scope access to an application resource](https://www.servicenow.com/docs/access?context=set-RCA-level&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

**Related topics**  


[Set the application scope, application resources, and event access](https://www.servicenow.com/docs/access?context=scope-resource-access&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

## Encryption for HR and Employee Document Management

HR Service Delivery and Employee Document Management provides encryption to secure sensitive information.

Encryption prevents unauthorized users from downloading and viewing employee documents or viewing specific fields. To encrypt employee documents or fields in HR, Field Encryption is activated by default and provides role-based encryption functions.

A cryptographic manager configures the fields or applications that are to be encrypted using encryption modules and module access policies:

-   **Note:** Ensure the **Application** field has Employee Document Management selected.

-   From the module access policy, set the role for encryption access. Specify the role to the user adding employee documents. Users with this role can access encrypted documents. See [Create a module access policy](https://www.servicenow.com/docs/access?context=create-module-access-policy&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
-   Employees can view their own documents when HR Service Delivery is licensed, activated, and the document type allows employee access. The role specified in the encryption module is not required for employees to view their own documents that are encrypted. [Define policies for a document type](hr-doc-management-config.md#) To configure the field or attachment for encryption, see [Encrypting fields and attachments](https://www.servicenow.com/docs/access?context=field-encryption-key-management&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Note:** Documents that were previously encrypted using encryption contexts have the same access using encryption modules in Yokohama.

For details on Field Encryption see, [Field Encryption](https://www.servicenow.com/docs/access?context=field-encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Edge Encryption for HR and Employee Document Management

HR Service Delivery and Employee Document Management provides edge encryption to secure sensitive information.

Edge encryption provides you with direct control over your data security. Encryption and key management are performed on your intranet between your browser and your ServiceNow instance.

See [Understanding Edge Encryption](https://www.servicenow.com/docs/access?context=c_EdgeEncryptionOverview&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Because edge encryption is enabled on a proxy server on your side of the network, there is significant planning, network administration and management, and setup required.

See [Planning for Edge Encryption](https://www.servicenow.com/docs/access?context=c_EdgeEncryptionPlanning&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

To install edge encryption, see [Edge Encryption installation](https://www.servicenow.com/docs/access?context=c_InstallEdgeEncryptionProxy&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

To configure edge encryption, see [Edge Encryption configuration](https://www.servicenow.com/docs/access?context=edge-config&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

### Edge encryption for HR

You can encrypt columns \(fields\) or attachments associated with an HR table. See [Encrypt fields using encryption configurations](https://www.servicenow.com/docs/access?context=c_ConfigureCloudEdge&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Note:** There are limitations when using edge encryption. See [Edge Encryption limitations](https://www.servicenow.com/docs/access?context=edge-encryption-limitations&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

