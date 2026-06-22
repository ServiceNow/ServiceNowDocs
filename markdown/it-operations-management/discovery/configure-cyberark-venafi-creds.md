---
title: Configure CyberArk Certificate Manager SaaS credentials
description: Configure authentication credentials so Certificate Inventory and Management can communicate with CyberArk Certificate Manager SaaS for automated certificate life-cycle management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/configure-cyberark-venafi-creds.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [CyberArk Certificate Manager SaaS credentials configuration]
breadcrumb: [Certificate management with CyberArk Certificate Manager SaaS, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Configure CyberArk Certificate Manager SaaS credentials

Configure authentication credentials so Certificate Inventory and Management can communicate with CyberArk Certificate Manager SaaS for automated certificate life-cycle management.

## Before you begin

Access to CyberArk Certificate Manager SaaS with appropriate permissions for certificate operations is required.

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    1.  From the credentials list, select **Certificate Management Credentials**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Descriptive name for the credential.|
        |CA Type|This value should be **CyberArk Venafi SaaS**.|
        |API Key|API key generated from CyberArk.|
        |Active|Option to make the credential active.|

3.  Select **Submit** to save the credential configuration.

4.  Validate that the credential is valid and reachable.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**

    2.  Open the credential you created.

    3.  Select **Validate Credential**.

        If the validation result is unsuccessful, verify the **API Key** value and retry.

5.  Assign a credential alias to the credential.

    For more information, see [Credential aliases for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/discovery-credential-alias.md).

    1.  In the **Credential alias** field, select the Unlock Credential alias icon \[Omitted image "lock-icon.png"\].

    2.  Select the Lookup using list icon \[Omitted image "lookup-using-list.png"\] to find and select the credential alias.

    3.  Select the Lock Credential alias icon \[Omitted image "unlock-outline-24.svg"\].

    4.  Select **Update**.


