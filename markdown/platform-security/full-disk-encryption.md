---
title: Full disk encryption
description: Full disk encryption \(FDE\) applies encryption to the entire storage system within the database server only, because this is the only customer data-storing component. FDE protects only against physical loss or theft of storage devices. When encrypted disk servers are powered on and providing data, the encryption provides no additional protection.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Encryption]
---

# Full disk encryption

Full disk encryption \(FDE\) applies encryption to the entire storage system within the database server only, because this is the only customer data-storing component. FDE protects only against physical loss or theft of storage devices. When encrypted disk servers are powered on and providing data, the encryption provides no additional protection.

## Full disk encryption

Full disk encryption may be relevant to heavily regulated organizations, but can add significant cost to a customer’s ServiceNow deployment. Measures in place by ServiceNow to mitigate loss or theft of storage devices may also be a factor in its selection.

From the ServiceNow AI Platform perspective, all data flows in decrypted.

Commercial environments use full disk encryption \(FDE\) with FIPS 140 validated hardware or storage devices that are in the process of validation along with a ServiceNow dedicated hardware option at extra cost. FDE applies to the hardware itself, and therefore provides encryption at rest for all data stored in every instance assigned to you.

For further details on selecting FDE and dedicated hardware options, contact your ServiceNow representative.

**Parent Topic:**[Encryption](../../security/concept/encryption-landing.md)

