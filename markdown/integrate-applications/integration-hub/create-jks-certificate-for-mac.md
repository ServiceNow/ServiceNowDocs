---
title: Generate the X.509 key pair and fingerprints on your Mac machine
description: Generate the X.509 key pair and its fingerprint on your Mac machine that you upload to the Oracle HCM tenant.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the Oracle HCM Cloud spoke, Oracle HCM Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Generate the X.509 key pair and fingerprints on your Mac machine

Generate the X.509 key pair and its fingerprint on your Mac machine that you upload to the Oracle HCM tenant.

## Before you begin

Role required: admin

Ensure that OpenSSL is installed. To verify that OpenSSL is installed, execute the command `openssl version` on the terminal.

## Procedure

1.  Open the terminal.

2.  To generate the private key, run the command `openssl genrsa -out private.key 2048`.

    The private key is generated.![Private key generation message.](../image/oracle-hcm-spoke-generate-x509-private-key.png)

3.  To generate the public key, run the command `openssl req -new -x509 -key private.key -out publickey.cer -days 365`.

4.  Enter the information.

    ![Public key information.](../image/oracle-hcm-spoke-x509-generate-public-key.png)

    The public key is generated.

5.  To generate the fingerprint, execute the command `openssl x509 -sha1 -in publickey.cer -noout -fingerprint`.

    The fingerprint is generated in the form of a hexadecimal value.

6.  Convert the hexadecimal value to a Base64 value.

7.  Copy the Base64 value and store in a secure place.

    You need the Base64 value when you configure the connections and credential record on your ServiceNow instance.


