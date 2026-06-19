---
title: Customize Certificate Inventory and Management
description: Customize various aspects within Certificate Inventory and Management using Discovery properties, enabling you to tailor the solution to your specific needs and enhance the overall management of TLS certificates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/customize-cert-inventory-mgmt.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Customize Certificate Inventory and Management

Customize various aspects within Certificate Inventory and Management using Discovery properties, enabling you to tailor the solution to your specific needs and enhance the overall management of TLS certificates.

## Before you begin

Role required: discovery\_admin or admin

## Procedure

1.  To edit [Discovery properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/r_DiscoveryProperties.md), navigate to **All** &gt; **Discovery Definition** &gt; **Properties**.

    -   glide.discovery.certs.cert\_admin\_user\_id
    -   glide.discovery.certs.days\_before\_expiration\_to\_create\_renewal\_task
    -   glide.discovery.certs.enable\_incident\_creation\_for\_expired\_certificates
    -   glide.discovery.certs.enable\_renewal\_task\_creation\_for\_discovered\_certificates
    -   glide.discovery.certs.slack\_channel\_id

