---
title: Run certificate discovery via certificate authority query
description: Run certificate discovery via certificate authority \(CA\) query to identify and import TLS certificates from specific CAs. Discover TLS certificates from CAs with Certificate Inventory and Management, using Patterns for diverse certificate authority vendors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/run-cert-inventory-mgmt-ca-query.html
release: brazil
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Visibility to TLS certificates, Configure, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Run certificate discovery via certificate authority query

Run certificate discovery via certificate authority \(CA\) query to identify and import TLS certificates from specific CAs. Discover TLS certificates from CAs with Certificate Inventory and Management, using Patterns for diverse certificate authority vendors.

## Before you begin

Role required: pki\_admin or discovery\_admin

## About this task

In Certificate discovery, the CA pattern uses specific API elements. The user added to the instance credentials needs permissions for these queries. For more information on the Certificate Authorities \(CA\) pattern and the associated API elements, see [Certificate authorities pattern API elements and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/ca-api-permission.md).

## Procedure

1.  Create a credential for the CA.

    1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials**.

    2.  On the Credentials form, select **New**.

    3.  Select **Certificate Management Credentials**.

    4.  Select a CA in the CA type field.

        The available options are: DigiCert, GoDaddy, Entrust, Sectigo, Let's Encrypt, EJBCA, CyberArk Certificate Manager SaaS, Sectigo Universal, and Sectigo Public.

    5.  Fill in the fields that are specific to the CA type you selected.

        |Field|Description|
        |-----|-----------|
        |Name|Descriptive name for the credential.|
        |Credential alias|Create or add a credential alias for the credential. For more information, see [Credential aliases for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/discovery-credential-alias.md).|
        |API Key|API key generated from the CA for DigiCert, GoDaddy, and CyberArk Certificate Manager SaaS CA types.|
        |Secret Key|API secret key generated from GoDaddy CA.|
        |User name|User name associated with this credential for Entrust,|
        |Authentication Key|Authentication key associated with this credential for Sectigo|
        |Password|Password associated with this credential, it is stored in the database in encrypted form. This field is visible only for Entrust and Sectigo CA types.|
        |Customer URI|Customer URI generated from the CA for Secitgo CA type.|
        |Keystore|JKS or PKCS12 keystore to use when this protocol is selected for Entrust and EJBCA CA types.|
        |Private Key|Private key associated with the CA for Let's Encrypt, EJBCA, Sectigo Universal, and Sectigo Public CA types.|
        |Key Type|Encryption algorithm type for the private key. The available options are: None, RSA, and ECDSA. This field is visible only for Let's Encrypt, EJBCA, Sectigo Universal, and Sectigo Public CA types.|
        |Key ID|Key ID for the ACME account for Sectigo Universal and Sectigo Public CA types.|
        |Contacts|Email IDs to use when creating ACME account. The IDs must be comma separated. For example, `username1@domain.com,username2@domain.com`. This field is visible only for Let's Encrypt and EJBCA CA types.|
        |MAC Key|MAC Key ID for the ACME account for Sectigo Universal and Sectigo Public CA types.|
        |Active|Option to make the credential active.|
        |ACME|Option to enable to Automated Certificate Management Environment \(ACME\) protocol. For more information, see [Automated certificate management for TLS certificates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/automated-cert-requests.md). This check box is available for DigiCert, Entrust, Let's Encrypt, EJBCA, Sectigo Universal, and Sectigo Public CA types.|
        |External Account Binding|Option to enable external account binding for EJBCA CA.|

2.  Create a Discovery schedule.

    For more information on setting up your Discovery schedules, see [Schedule a horizontal discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/t_CreateADiscoverySchedule.md).

    1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

    2.  Select **New**.

    3.  Select **Certificates** in the **Discovery** field.

    4.  Select **CA Trust Discovery** in the **Certificate Discovery Type** field.

    5.  Select **Auto-Select MID Server** or **Specific MID Server** in the **MID Server selection method** field.

    6.  Fill out any other necessary fields.

        For more information, see [Discovery Schedule form reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-schedule-form.md).

    7.  Select **Submit**.

3.  Open the Discovery schedule.

4.  To add the CA pattern you need, select the **Serverless Execution pattern** tab and then select **New**.

    If you enable the **Include cert status** option, you can specify multiple certificate statuses by separating them with commas.

5.  Select **Submit**.


## Result

When your Discovery schedule runs, it automatically scans your files.

