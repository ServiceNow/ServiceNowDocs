---
title: HR security
description: HR Service Delivery provides Restricted Caller Access, Encryption Support, and Edge Encryption security features.Restricted caller access \(RCA\) defines cross-scope access to HR Service Delivery applications.HR Service Delivery and Employee Document Management provides encryption to secure sensitive information.HR Service Delivery and Employee Document Management provides edge encryption to secure sensitive information.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
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


To define cross-scope access to an application resource, refer to Define cross-scope access to an application resource.

**Related topics**  


[bundle-cadev.scope-resource-access]

## Encryption for HR and Employee Document Management

HR Service Delivery and Employee Document Management provides encryption to secure sensitive information.

Encryption prevents unauthorized users from downloading and viewing employee documents or viewing specific fields. To encrypt employee documents or fields in HR, Field Encryption is activated by default and provides role-based encryption functions.

A cryptographic manager configures the fields or applications that are to be encrypted using encryption modules and module access policies:

-   **Note:** Ensure the **Application** field has Employee Document Management selected.

-   From the module access policy, set the role for encryption access. Specify the role to the user adding employee documents. Users with this role can access encrypted documents. See Create a module access policy.
-   Employees can view their own documents when HR Service Delivery is licensed, activated, and the document type allows employee access. The role specified in the encryption module is not required for employees to view their own documents that are encrypted. [Define policies for a document type](hr-doc-management-config.md#) To configure the field or attachment for encryption, see Encrypting fields and attachments.

**Note:** Documents that were previously encrypted using encryption contexts have the same access using encryption modules in Australia.

For details on Field Encryption see, Field Encryption.

## Edge Encryption for HR and Employee Document Management

HR Service Delivery and Employee Document Management provides edge encryption to secure sensitive information.

Edge encryption provides you with direct control over your data security. Encryption and key management are performed on your intranet between your browser and your ServiceNow instance.

See Understanding Edge Encryption.

Because edge encryption is enabled on a proxy server on your side of the network, there is significant planning, network administration and management, and setup required.

See Planning for Edge Encryption.

To install edge encryption, see Edge Encryption installation.

To configure edge encryption, see Edge Encryption configuration.

### Edge encryption for HR

You can encrypt columns \(fields\) or attachments associated with an HR table. See Encrypt fields using encryption configurations.

**Note:** There are limitations when using edge encryption. See Edge Encryption limitations.

