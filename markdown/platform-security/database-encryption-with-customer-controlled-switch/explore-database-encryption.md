---
title: Exploring Database Encryption
description: ServiceNow offers database encryption \(DBE\) and full-disk encryption methods for customers with statutory obligations for data protection which may require at-rest protection for all data.
locale: en-US
release: xanadu
product: Database Encryption with Customer Controlled Switch
classification: database-encryption-with-customer-controlled-switch
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Database Encryption, Encryption]
---

# Exploring Database Encryption

ServiceNow® offers database encryption \(DBE\) and full-disk encryption methods for customers with statutory obligations for data protection which may require at-rest protection for all data.

**Important:** Starting with the Washington DC release, Database Encryption is being prepared for future deprecation. Cloud Encryption is the replacement solution for data at rest encryption. For details, see [Cloud Encryption with Key Management](../../encryption-dare/concept/dare-overview.md)

Database Encryption enables all data to be protected with symmetric AES-256 encryption, whether the database is online or offline. From the ServiceNow AI Platform perspective, all data flows in decrypted.

-   Database Encryption supports all stored data to be encrypted in real time providing protection for data online and offline with no loss of functionality.
-   Full disk encryption protects offline data if there is disk loss or theft.

![Database Encryption](../image/fig-5-database-encryption.png)

With Database Encryption, all stored data is encrypted and individual records or tables are decrypted in memory while being accessed. New or changed data is encrypted as it is entered into a table and associated activity log files \(bin, redo, undo, and error\) are also encrypted.

Database Encryption is transparent to users, with no loss of functionality. When using this feature, all instances are encrypted, along with replication traffic and backups. Instance cloning is still available with a minor performance impact for using Database Encryption of up to 5%. Both new and existing instances on supported releases of the ServiceNow AI Platform can take advantage of database encryption.

As illustrated, ServiceNow stores and manages keys using a three-level key hierarchy:

![Key management](../image/fig-6-key-management.png)

1.  A customer specific AES-256 key is created by the database engine and is used to encrypt the data.
2.  A second customer specific AES-256 key is created by the database engine and is used to protect the first-level key.
3.  A third AES-256 key is created by and stored within FIPS 140 validated key management appliances in the ServiceNow datacenters. This key protects the second-level key and is unique per customer instance.

The ServiceNow AI Platform also supports database encryption with a customer supplied switch, DBE with CCS. This is an encryption solution that encrypts all data-at-rest when not in use in the database. It uses industry standard AES encryption with no impact to functionality. The database encrypts data as it is written to the disk, and decrypts data as it is read from the disk. That means that applications always have the data in an unencrypted state to perform the necessary logic and functions without impact.

**Note:** Database Encryption is not supported for on-premise instances.

If you are using your own keys for database encryption, see [Database Encryption with Customer-Controlled Switch](dbe-with-ccs.md).

**Parent Topic:**[Database Encryption](db-full-disk-encryption.md)

