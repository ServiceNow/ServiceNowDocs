---
title: Create a JKS file
description: Generate a Java KeyStore \(JKS\) file for OAuth authentication setup. This process involves extracting the private key from a credentials JSON file and converting it through PEM format to create the required JKS file.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Create a JKS file

Generate a Java KeyStore \(JKS\) file for OAuth authentication setup. This process involves extracting the private key from a credentials JSON file and converting it through PEM format to create the required JKS file.

## Before you begin

Role required: admin

This task requires a credentials JSON file from the Card Data Security tokenizer service. See [Initial setup for Vault schema, Connections and Service Account for Card data security \(KB2830577\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2830577) for more information.

## Procedure

1.  Create a blank file in a text editor.

2.  From the credentials JSON file, copy the `privateKey` value into the blank file.

3.  Replace the `\n` values with new line characters.

4.  Save the file with the extension `.pem`.

5.  Convert the `.pem` file to a JKS file.

    When converting the file, you will need to provide the key store password and the key alias—make a note of these.


## Result

A JKS file is generated for use in your ServiceNow instance.

## What to do next

[Create an X.509 Certificate](create-an-x-509-certificate.md).

