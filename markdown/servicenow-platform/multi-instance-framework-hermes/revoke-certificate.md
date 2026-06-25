---
title: Revoke a Hermes certificate
description: Revoke a ServiceNow instance-signed certificate so that it can't be used in secure connections to the Hermes Messaging Service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/revoke-certificate.html
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Revoke a Hermes certificate

Revoke a ServiceNow® instance-signed certificate so that it can't be used in secure connections to the Hermes Messaging Service.

## Before you begin

Role required: hermes\_admin or sn\_kmf.cryptographic\_manager

## Procedure

1.  Navigate to **All** &gt; **Certificate Generator** &gt; **Instance PKI Certificate Generator**.

2.  Select **Manage Certificates**.

3.  In the **Hermes IPKI Certificates** dialog box, select one or more certificates that you want to revoke.

4.  Select **Revoke**.

5.  Select a reason for the revocation and then select **OK**.


## Result

The certificates are revoked and can no longer be used in secure connections to Hermes. You can view the revocation date and the reason it was revoked in the Certificates \[sys\_kmf\_certificate\] table.

**Parent Topic:**[Configuring Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/configuring-hermes-messaging-service.md)

**Related topics**  


[Activating the Hermes Messaging Service]()

[Set up a secure connection to the Hermes Messaging Service]()

[Restricting access to Hermes]()

