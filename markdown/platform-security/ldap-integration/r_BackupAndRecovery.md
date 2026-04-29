---
title: Backup and recovery with ADAM
description: All ADAM data can be backed up using standard file system backup methods.
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Backup and recovery with ADAM

All ADAM data can be backed up using standard file system backup methods.

## Redundancy

ADAM has built-in replication utilities based on the same technology as AD. A full read and write replica of an ADAM partition can exist on the same or different computer. You can use this replica in a variety of ways to provide a fault-tolerant LDAP integration with the instance. One option is to expose both partitions to the instance through the firewall and define both servers in the LDAP Properties server field.

**Related topics**  


[Active Directory Application Mode \(ADAM\)](../concept/c_ActiveDirectoryApplicationMode.md)

[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

