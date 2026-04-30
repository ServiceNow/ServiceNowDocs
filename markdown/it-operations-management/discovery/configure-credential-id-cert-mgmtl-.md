---
title: Configure Credential Identifier for Certificate Management credential type
description: Ensure unique identification and effective management of credentials by configuring credential identifier for Certificate Inventory and Management.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure Credential Identifier for Certificate Management credential type

Ensure unique identification and effective management of credentials by configuring credential identifier for Certificate Inventory and Management.

## Before you begin

Role required: admin

## About this task

To enable external storage credential support for TLS certificate discovery from CA types such as GoDaddy, DigiCert, and Sectigo, set up the credential identifier within the instance for the respective Certificate Management credential type.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials**.

2.  Select **New**.

3.  Select a credential type labeled as **Certificate Management Credential**.

4.  In the Credential form, select the **External Credential Store** check box.

5.  Fill in the **Credential Alias** and **Credential ID** fields.

    **Note:**

    Ensure that the Credential ID and Arg\_ID in the Credential Resolver file match.

    Based on the Certificate Authority you choose, the appropriate fields will appear requesting the specific information required by each CA. For additional information, refer to KB article for [Digicert](https://support.servicenow.com/kb_view.do?sysparm_article=KB2166364), [Entrust](https://support.servicenow.com/kb_view.do?sysparm_article=KB2173533), [Let’s encrypt](https://support.servicenow.com/kb_view.do?sysparm_article=KB2197962), [Microsoft CA](https://support.servicenow.com/kb_view.do?sysparm_article=KB2198094).

6.  Select **Submit**.


