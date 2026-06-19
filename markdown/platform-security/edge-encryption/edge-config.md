---
title: Configuring Edge Encryption
description: After the Edge Encryption proxy server is installed and running, manage Edge Encryption through the proxy server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/edge-encryption/edge-config.html
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Edge Encryption, Encryption]
---

# Configuring Edge Encryption

After the Edge Encryption proxy server is installed and running, manage Edge Encryption through the proxy server.

You must complete all the steps in [Installing Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_InstallEdgeEncryptionProxy.md) before creating encryption configurations and encryption patterns on the instance.

**Note:** To access the Edge Encryption configuration, you must log in through the proxy server and elevate to the security\_admin role.

-   **[Rotate encryption keys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_EncryptionKeyRotation.md)**  
Perform encryption key rotation from the instance. Add a new key, change the default key assignment, and then schedule a mass key rotation or a single key rotation.
-   **[Encrypt fields using encryption configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_ConfigureCloudEdge.md)**  
Encrypt fields by creating encryption configurations.
-   **[Encrypt attachments using standard encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_EncryptingAttachments.md)**  
You can encrypt attachments for specific tables.
-   **[Change a field or attachment's encryption type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/t_ChangeAFieldsEncryptionType.md)**  
You can change a field or attachment's encryption type by selecting a new encryption type in the existing encryption configuration record. A specific table and field combination can only have one active configuration at a time.
-   **[Tokenize strings using encryption patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/t_ConfigureBasicEncryptionPatterns.md)**  
You can replace string patterns with tokens before they are sent to and stored in the instance.
-   **[Repair or recover order-preserving encrypted data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_EdgeEncryptionJobs.md)**  
If you have the security-admin role, you can schedule jobs performed by the Edge Encryption proxy to repair or recover fields that use order preserving encryption.
-   **[Configure the IP address deny list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/deny-list-IPs.md)**  
Prevent an IP address in your network from sending requests to your instance
-   **[Encrypt data from a record producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/record-producers-edge.md)**  
Configure your Edge Encryption proxy server to allow inserts from a record producer by creating encryption rules from the record producer record.
-   **[Define a custom encryption rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_EncryptionRules.md)**  
It may be necessary to identify and encrypt sensitive information in HTTP requests on the way to your instance. You can write encryption rules to identify, interpret, and encrypt data in such requests, mapping fields in the request to table-field names on your instance.
-   **[Edge Encryption dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/r_EdgeEncryptionDictAttributes.md)**  
Add dictionary attributes to tables and fields to control how they work with Edge Encryption.
-   **[Domain separation and Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/edge-encryption-domain-separation.md)**  
Domain separation is supported in limited circumstances with Edge Encryption. Edge Encryption provides the ability to encrypt data from within the customer's environment through the use of specific configurations, rules, and keys defined on the Edge Encryption proxy. The Edge Encryption proxy is not domain aware and cannot support domain-specific settings. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Data integration with Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/data-integration.md)**  
To integrate third-party data with an instance using Edge Encryption, you must route the data through the Edge Encryption proxy server using supported integrations. Supported integrations use base system encryption rules that map data in each payload to fields in a table.
-   **[Edge Encryption diagnostics and performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/edge-stats.md)**  
Monitor Edge Encryption proxy server performance trends and drill into errors generated by the Edge Encryption proxy server.
-   **[Increase debug logging for the Edge Encryption proxy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/edge-debug-logging.md)**  
Increase the level of logging to interpret the logs and debug issues with the proxy.

**Parent Topic:**[Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/edge-encryption.md)

