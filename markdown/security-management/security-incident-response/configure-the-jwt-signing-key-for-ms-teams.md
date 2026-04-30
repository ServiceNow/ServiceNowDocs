---
title: Configure the JWT signing key for MS Teams
description: Create a JSON Web Token \(JWT\) signing key to assign to your Java Key Store certificate.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Certificates for authentication, Establish MS Teams Graph connection on ServiceNow AI Platform, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure the JWT signing key for MS Teams

Create a JSON Web Token \(JWT\) signing key to assign to your Java Key Store certificate.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System OAuth** &gt; **JWT Keys**.

2.  Open the record **Microsoft Teams Connector JWT**.

3.  Enter the password that is used to encrypt private key to generate the .PFX file and .CER file in **Signing Key Password**.

4.  Click **Update**.


**Parent Topic:**[Using Certificates for authentication](using-certificates-for-authentication.md)

