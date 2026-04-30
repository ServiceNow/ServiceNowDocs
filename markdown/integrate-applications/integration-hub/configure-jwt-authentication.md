---
title: Generate X.509 key pair and fingerprints on your Windows machine
description: Generate the X.509 key pair and its fingerprint on your Windows machine that you upload to the Oracle HCM tenant.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the Oracle HCM Cloud spoke, Oracle HCM Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Generate X.509 key pair and fingerprints on your Windows machine

Generate the X.509 key pair and its fingerprint on your Windows machine that you upload to the Oracle HCM tenant.

## Before you begin

Role required: admin

Ensure that OpenSSL is installed.

## Procedure

1.  On your Windows machine, copy the path to the `bin` folder under the `OpenSSL-Win<bit>` folder.

2.  Run the Command Prompt as an administrator.

3.  On the prompt, use the `cd` command to change the current directory to the `bin` folder.

4.  To generate the private key, run the command `openssl genrsa -out private.key 2048`.

    The private is generated under the bin folder.

5.  To generate the public key, run the command `openssl req -new -x509 -key private.key -out publickey.cer -days 365`.

6.  Enter the information.

    You can choose to leave one or more fields empty.![Information fields on command prompt.](../image/oracle-hcm-spoke-x509-generate-public-key-windows.png)

    The public key is generated in the bin folder.

7.  To generate the fingerprint, run the command `openssl x509 -sha1 -in publickey.cer -noout -fingerprint`.

    The fingerprint is generated in the form of a hexadecimal value.

8.  Convert the hexadecimal value to a Base64 value.

9.  Copy the Base64 value and store in a secure place.

    You need the Base64 value when you configure the connections and credential records on your ServiceNow instance.


