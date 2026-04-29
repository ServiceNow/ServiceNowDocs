---
title: Create a public/private key pair for the Microsoft SharePoint Online external content connector
description: Generate a public/private key pair for the Microsoft SharePoint Online external content connector. Extract the public key as a DER-encoded binary X.509 format certificate for use in configuring API access for the connector in the Microsoft Entra admin center.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft SharePoint Online external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a public/private key pair for the Microsoft SharePoint Online external content connector

Generate a public/private key pair for the Microsoft SharePoint Online external content connector. Extract the public key as a DER-encoded binary X.509 format certificate for use in configuring API access for the connector in the Microsoft Entra admin center.

## Before you begin

You must have access to the Java keytool utility. For details on the keytool utility, see [https://docs.oracle.com/en/java/javase/21/docs/specs/man/keytool.html](https://docs.oracle.com/en/java/javase/21/docs/specs/man/keytool.html).

Role required: none

## About this task

The Microsoft SharePoint Online external content connector uses a public/private key pair to authenticate with an OAuth 2.0 app configured in the Microsoft Entra admin center. Key pair authentication allows the connector to access your Microsoft SharePoint Online data via the Microsoft Graph API.

To configure public/private key pair authentication for the connector, you need to create the following items:

1.  A public/private key pair in Java KeyStore \(JKS\) format.
    -   Your connector admin needs this JKS keystore file and its password when configuring settings for the Microsoft SharePoint Online external content connector.
    -   When the Microsoft SharePoint Online external content connector runs a crawl, it uses the private key from this JKS keystore file to sign the authentication request it sends to the OAuth 2.0 app defined in the Microsoft Entra admin center.
2.  A copy of the public key in DER-encoded binary X.509 certificate format.
    -   Your administrator needs to upload this certificate file to the OAuth 2.0 app defined in the Microsoft Entra admin center that grants API access to the Microsoft SharePoint Online external content connector.
    -   When the Microsoft SharePoint Online external content connector submits its authentication request to the OAuth 2.0 app defined in the Microsoft Entra admin center, the app uses the public key from this uploaded certificate to confirm that the authentication request was signed with the private key.

**Note:** If your organization has its own guidelines for generating public/private key pairs, follow those to generate a key pair and a public key certificate in the required formats.

## Procedure

1.  Generate a public/private key pair in JKS keystore format:

    1.  Run this keytool command, replacing `<alias>`, `<jks-file>`, and `<password>` with values of your choice:

        ```
        keytool -genkey -alias <alias> -keyalg RSA -keysize 2048 -keystore <jks-file>.jks -storepass "<password>" -storetype JKS -validity 360
        ```

        As an example, you might specify `ms-spo-connector-cert` as the key alias and the JKS repository filename, and enter a password:

        ```
        keytool -genkey -alias ms-spo-connector-cert -keyalg RSA -keysize 2048 -keystore ms-spo-connector-cert.jks -storepass "C?yuR4hrt2GU7g}3" -storetype JKS -validity 360
        ```

    2.  When prompted for your first and last name, enter the Common Name \(CN\) you want for the key pair, then press Enter.

        As an example, you might specify `Microsoft SharePoint Online external content connector` as the Common Name for the key pair.

    3.  At each of the remaining distinguished name prompts, enter the requested information and press Enter.

    4.  When prompted to confirm that the distinguished name is correct, enter `yes` and press Enter.

    5.  When prompted for a key password, press Enter to use the same password you specified for the keystore file.

        **Important:** The key must use the same password as the keystore. Record this password in a secure location. Your connector admin needs this password when configuring the Microsoft SharePoint Online external content connector.

    The keytool utility generates a new Java KeyStore \(.jks\) file containing your public/private key pair.

    **Important:** Ignore the keytool warning message about migrating your keystore to the PKCS12 format. The external content connector only supports the Java KeyStore format.

2.  Export your public key in DER-encoded binary X.509 certificate format by running the following keytool command, replacing `<cer-file>` with a filename of your choice and replacing `<alias>`, `<jks-file>`, and `<password>` with the same values you used in step [1](gen-cert-spo-ext-cont-connector.md#generate-keypair-jks):

    ```
    keytool -export -alias <alias> -file <cer-file>.cer -keystore <jks-file>.jks -storepass "<password>" -storetype JKS
    ```

    As an example, you might specify `ms-spo-connector-cert` as the filename for the DER-encoded binary X.509 format certificate:

    ```
    keytool -export -alias ms-spo-connector-cert -file ms-spo-connector-cert.cer -keystore ms-spo-connector-cert.jks -storepass "C?yuR4hrt2GU7g}3" -storetype JKS
    ```

    The keytool utility exports a copy of your public key as an DER-encoded binary X.509 format certificate file with your chosen filename.

    **Important:** Ignore the keytool warning message about migrating your keystore to the PKCS12 format. The external content connector only supports the Java KeyStore format.


## What to do next

Provide both of the files you generated to the admins who configure your Microsoft SharePoint Online instance and AI Search on your ServiceNow AI Platform® instance, as follows:

<table id="table_rr3_wd3_xdc"><thead><tr><th>

File

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DER-encoded binary X.509 format public key certificate file

</td><td>

Provide this certificate file to your Microsoft SharePoint Online administrator. They will need to upload the certificate to the Microsoft Entra admin center when configuring an OAuth 2.0 application for the Microsoft SharePoint Online external content connector. For more information on configuring an OAuth 2.0 application in the Microsoft Entra admin center for the Microsoft SharePoint Online external content connector, see [Configure Microsoft SharePoint Online for external content indexing](cfg-azure-spo-ext-cont-connector.md).

</td></tr><tr><td>

JKS keystore file and password

</td><td>

Provide this Java KeyStore file and its password to your ServiceNow AI Platform admins. They will need the file and password when configuring the Microsoft SharePoint Online external content connector. For details on creating and configuring the Microsoft SharePoint Online external content connector, see [Create a Microsoft SharePoint Online external content connector](create-ext-cont-connector-mspo.md).

</td></tr></tbody>
</table>**Parent Topic:**[Microsoft SharePoint Online external content connector](../concept/microsoft-sharepoint-online-external-content-connector.md)

