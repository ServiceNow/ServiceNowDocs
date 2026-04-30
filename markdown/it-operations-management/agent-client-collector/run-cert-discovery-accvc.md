---
title: Run Certificate Discovery via Agent Client Collector for Visibility - Content
description: Discover TLS/SSL certificates used by ports running on the agent's server. The Certificate Inventory and Management application uses this information to manage TLS/SSL certificates.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC certificates, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Run Certificate Discovery via Agent Client Collector for Visibility - Content

Discover TLS/SSL certificates used by ports running on the agent's server. The Certificate Inventory and Management application uses this information to manage TLS/SSL certificates.

## Before you begin

Verify that the latest version of Agent Client Collector for Visibility - Content \(ACC-VC\) is installed.

Verify that the latest version of Certificate Inventory and Management is installed.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

2.  Enable the **TLS SSL Certificate Capture** policy.

3.  Navigate to **All** &gt; **System properties** &gt; **All properties**.

4.  To discover certificates on specific ports:

    1.  Locate and select the **sn\_acc\_vis\_content.tls\_ssl\_scanner\_ports** property.

    2.  Enter a comma-separated list of port numbers on which to scan for certificates in the **Choices** field.

        By default, the values are identical to those values configured for the **tls\_ssl\_certs** property.

5.  To discover certificates on all available open ports:

    1.  Locate and select the **sn\_acc\_vis\_content.tls\_ssl\_scan\_all\_open\_ports** property.

    2.  Assign the value **true**.

6.  To store the original certificate in the instance, set the **sn\_acc\_vis\_content.tls\_ssl\_keep\_original** property to **true**.


## Result

The Agent Client Collector collects the data and discovers the TLS/SSL certificates. This data is the same as what is gathered by the IP-based **tls\_ssl\_probe** property.

The TLS/SSL certificates are populated in the following tables:

-   Discovered Certificates \[sn\_disco\_certmgmt\_certificate\_history\]
-   Unique Certificates \[cmdb\_ci\_certificate\]
-   Installed Certificates \[sn\_disco\_certmgmt\_cmdb\_installed\_certificate\]

A CI relationship is created between the discovered certificates and the corresponding Host CI \(in this case, the agent's server\).

**Parent Topic:**[Agent Client Collector certificates](../concept/acc-certificates.md)

**Related topics**  


[Certificate Inventory and Management](../../discovery/reference/cert-inventory-mgmt.md)

[Run Certificate Discovery via port scans](../../discovery/task/run-cert-inventory-mgmt-ports.md)

