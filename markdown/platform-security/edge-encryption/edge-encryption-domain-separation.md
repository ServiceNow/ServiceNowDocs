---
title: Domain separation and Edge Encryption
description: Domain separation is supported in limited circumstances with Edge Encryption. Edge Encryption provides the ability to encrypt data from within the customer's environment through the use of specific configurations, rules, and keys defined on the Edge Encryption proxy. The Edge Encryption proxy is not domain aware and cannot support domain-specific settings. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Domain separation and Edge Encryption

Domain separation is supported in limited circumstances with Edge Encryption. Edge Encryption provides the ability to encrypt data from within the customer's environment through the use of specific configurations, rules, and keys defined on the Edge Encryption proxy. The Edge Encryption proxy is not domain aware and cannot support domain-specific settings. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: No support

-   The domain field may exist on data tables but there is no business logic to manage the data.
-   This level is not considered domain-separated.

For more information on support levels, see [Application support for domain separation](../../company-and-domain-separation/reference/domain-separated-apps.md).

## How domain separation works in Edge Encryption

Edge Encryption can be used where domain-specific keys, configurations, and rules are not required.

**Parent Topic:**[Configuring Edge Encryption](edge-config.md)

**Related topics**  


[Domain separation for service providers](../../company-and-domain-separation/reference/domain-sep-landing-page.md)

