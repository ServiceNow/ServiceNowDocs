---
title: Planning for Edge Encryption
description: Successful implementation of Edge Encryption requires planning and preparation.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Edge Encryption, Encryption]
---

# Planning for Edge Encryption

Successful implementation of Edge Encryption requires planning and preparation.

Answer the following questions in the planning stage.

-   Which fields are to be encrypted?
-   Which encryption types are to be used?
-   How many Edge Encryption proxies are needed? See [Sizing your Edge Encryption environment](edge-environment-size.md) for recommendations and considerations.
-   If an order preserving encryption type or encryption patterns are to be used, where is the MySQL database located?
-   Which key management system is to be used?

System administrators, network administrators, and security team members have different tasks to fulfill for implementing Edge Encryption.

-   System administrators need the security-admin role. The system administrator must :
    -   Download the Edge Encryption proxy application.
    -   Set up an Edge Encryption user account for the proxies to use to connect to the instance. The user must be assigned the edge\_encryption role.
    -   Configure encryption keys, and set the default keys.
    -   Configure Edge Encryption on the instance.
    -   Schedule encryption jobs.
    -   Monitor Edge Encryption.
    -   Create and edit encryption rules.
-   Your network administrator must:
    -   Install the Edge Encryption proxy application.
    -   Know the network addresses for the proxy servers and the proxy database used for order-preserving encryption and encryption patterns.
    -   Install the proxy database to be used for order-preserving encryption and encryption patterns.
    -   Start and stop the proxy applications.
    -   Perform encryption key management.
    -   Determine how to map users to encryption proxy applications. This can be done with DNS settings or routing rules, and is specific to each network.
    -   Manage multiple proxy servers.
    -   Configure load balancer pools and settings.
-   Your security administrator must determine the encryption types to be assigned to each field.

-   **[Edge Encryption system requirements](../reference/r_CloudEdgeSystemRequirements.md)**  
You can run the Edge Encryption proxy application on servers or virtual machines that run on Microsoft Windows or Linux operating systems. For optimum performance, ensure that your configuration meets these requirements.
-   **[Sizing your Edge Encryption environment](edge-environment-size.md)**  
Choosing the number of proxy servers for your environment is an important task. Consider the number of users, redundancy needs, and acceptable latency.
-   **[Calculate the order-preserving and tokenization database size](../task/size-db.md)**  
If using order-preserving encryption or encryption patterns, determine the size of your MySQL database by multiplying the number of potential records by record size.
-   **[Edge Encryption limitations](../reference/edge-encryption-limitations.md)**  
Edge Encryption impacts system functions. Carefully evaluate the impact of encrypting a field.

**Parent Topic:**[Edge Encryption](../reference/edge-encryption.md)

