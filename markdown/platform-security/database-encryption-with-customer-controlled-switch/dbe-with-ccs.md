---
title: Database Encryption with Customer Controlled Switch
description: Database Encryption with Customer-Controlled Switch \(DBE-CCS\) is an encryption solution that encrypts all data-at-rest when not in use in the database.
locale: en-US
release: australia
product: Database Encryption with Customer Controlled Switch
classification: database-encryption-with-customer-controlled-switch
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Database Encryption, Encryption]
---

# Database Encryption with Customer Controlled Switch

Database Encryption with Customer-Controlled Switch \(DBE-CCS\) is an encryption solution that encrypts all data-at-rest when not in use in the database.

**Important:**

Database Encryption with Customer Controlled Switch has begun its End of Life process, and has reached the End Of Sale and End of Renewal milestones as of the Yokohama release. For data-at-rest encryption support, see [Cloud Encryption with Key Management](../../encryption-dare/concept/dare-overview.md).

## Overview

Database Encryption with customer controlled switch uses industry standard AES encryption, with no impact to functionality. The database encrypts data as it is written to the disk and decrypted by the database as it is read from the disk. Applications always have the data in an unencrypted state to perform the necessary logic and functions.

DBE-CCS utilizes technology native to the database, often called Tablespace Encryption or Transparent Data Encryption. For more details on the technology, refer to the [MariaDB website](https://mariadb.com/kb/en/data-at-rest-encryption-overview/) under "Tablespace Encryption."

DBE-CCS requires you to set up an HTTPS REST service endpoint that periodically provides the secret key to the ServiceNow instance. The CCS endpoint then returns the customer secret key encrypted with the public key of the database instance.

## Customer endpoint

**Important:** Your organization is solely responsible for setting up and maintaining your CCS endpoint. The customer endpoint specification is provided in [KB0789788](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0789788).

A ServiceNow technology partner, Fortanix, is available to implement your customer endpoint for you. Contact the technology partner directly for details of the integration. For details, see [Using Fortanix Data Security Manager with ServiceNow](https://support.fortanix.com/hc/en-us/articles/4404181731732-Using-Fortanix-Data-Security-Manager-with-ServiceNow).

## Multiple ServiceNow version support

**Important:** Database Encryption is a paid infrastructure offering that is release agnostic. It can be applied to any supported release and to new or existing instances.

## Other references

Refer to these references for additional information about DBE with CCS:

|Reference|Description|
|---------|-----------|
|[KB0993681](https://support.servicenow.com/kb_view.do?sysparm_article=KB0993681)|Architecture of Database Encryption Customer Controlled Switch|
|[KB0789788](https://support.servicenow.com/kb_view.do?sysparm_article=KB0789788) |Implementation guide for DBE with CCS|

**Note:** To access KB articles, you must first authenticate into Now Support.

**Parent Topic:**[Database Encryption](db-full-disk-encryption.md)

