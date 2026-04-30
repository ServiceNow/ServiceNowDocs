---
title: Create a Microsoft SharePoint Online external content connector
description: Create an external content connector to retrieve searchable content and security principals from your Microsoft SharePoint Online source system.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-06-26"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Creating external content connectors, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a Microsoft SharePoint Online external content connector

Create an external content connector to retrieve searchable content and security principals from your Microsoft SharePoint Online source system.

## Before you begin

A source system administrator must have already configured your Microsoft SharePoint Online source system to allow access by the Microsoft SharePoint Online external content connector. For details on configuring these settings in the source system, see [Create a public/private key pair for the Microsoft SharePoint Online external content connector](gen-cert-spo-ext-cont-connector.md) and [Configure Microsoft SharePoint Online for external content indexing](cfg-azure-spo-ext-cont-connector.md).

If your Microsoft SharePoint Online tenant is in the Microsoft 365 GCC or GCC High cloud or the Microsoft 365 DoD cloud, you must have already configured the Microsoft cloud service endpoint URL. For instructions on configuring this setting, see [Configure the Microsoft cloud service endpoint URL](configure-ms-cloud-service-endpoint-url.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **SharePoint Online** tile, then select **Next**.

5.  On the Connector details page, fill in the required connection settings.

<table id="table_bvk_jcd_t2c"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this Microsoft SharePoint Online external content connector.

</td></tr><tr><td>

Application \(client\) ID

</td><td>

Application \(client\) ID for the OAuth 2.0 application defined in the Microsoft Entra admin center that grants access to your Microsoft SharePoint Online source system.

 If you have access to the OAuth 2.0 application's registration record in the Microsoft Entra admin center, you can navigate to **Overview** and copy this ID from the **Application \(client\) ID** field in the Essentials section.

 If you can't access the OAuth 2.0 application's registration record in the Microsoft Entra admin center, ask your Microsoft Entra administrator for the application's **Application \(client\) ID** value.

</td></tr><tr><td>

Directory \(tenant\) ID

</td><td>

Directory \(tenant\) ID for the OAuth 2.0 application defined in the Microsoft Entra admin center that grants access to your Microsoft SharePoint Online source system.

 If you have access to the OAuth 2.0 application's registration record in the Microsoft Entra admin center, you can navigate to **Overview** and copy this ID from the **Directory \(tenant\) ID** field in the Essentials section.

 If you can't access the OAuth 2.0 application's registration record in the Microsoft Entra admin center, ask your Microsoft Entra administrator for the application's **Directory \(tenant\) ID** value.

</td></tr><tr><td>

JKS Certificate

</td><td>

Java KeyStore \(JKS\) file containing a public/private key pair generated with the Java keytool utility. These keys must match the public key from the DER-encoded binary X.509 format certificate uploaded to the OAuth 2.0 application defined in the Microsoft Entra admin center that allows the Microsoft SharePoint Online external content connector to access your source system data.

 If you don't have a copy of the JKS file, ask your security administrator for it. You can't download the JKS file from the OAuth 2.0 application's registration record in the Microsoft Entra portal.

</td></tr><tr><td>

JKS certificate password

</td><td>

Password for the Java KeyStore \(JKS\) file specified in **JKS Certificate**.

 If you don't have the password for the JKS file, ask your security administrator for it. You can't retrieve the JKS certificate password from the registration record for the OAuth 2.0 application defined in the Microsoft Entra admin center that allows the Microsoft SharePoint Online external content connector to access your source system data.

</td></tr><tr><td>

JKS certificate thumbprint \(Base 64\)

</td><td>

Base64-encoded thumbprint SHA1 hash for the DER-encoded binary X.509 format public key certificate uploaded to the OAuth 2.0 application defined in the Microsoft Entra admin center that allows the Microsoft SharePoint Online external content connector to access your source system data.

 If you don't have this value, ask your Microsoft Entra administrator for the base64-encoded thumbprint SHA1 hash for the application's DER-encoded binary X.509 format public key certificate.

</td></tr></tbody>
</table>6.  Select **Save and validate**.

    **Note:** If validation fails, an error message appears. Double-check your connection settings to ensure they're correct.


## Result

Your new Microsoft SharePoint Online external content connector appears in the Connectors section.

## What to do next

You can optionally define crawl settings for your new Microsoft SharePoint Online external content connector. Using these settings, you can limit the set of sites you want the connector to crawl, or define the file extensions for documents you want the connector's crawls to include or exclude. To learn how to configure the connector's crawl settings, see [Configure crawl settings for the Microsoft SharePoint Online external content connector](configure-crawl-settings-spo-ext-cont-connector.md).

If you want the connector to crawl everything in the source system, and don't want to apply file-extension inclusion or exclusion filters, you can skip definition of crawl settings and go straight on to define a crawl schedule for your new connector or run one-time crawls for it. For details on defining a crawl schedule, see [Define a crawl schedule for an external content connector](define-schedule-ext-cont-connector.md). To learn about running one-time crawls, see [Run a one-time full or partial document crawl for an external content connector](run-doc-crawl-ext-cont-connector.md) and [Run a one-time user mapping crawl for an external content connector](run-umap-crawl-ext-cont-connector.md).

You can create search sources for the connector's indexed source and link them to your search profiles. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources and linking them to search profiles, see [Search sources in AI Search](../concept/search-sources-ais.md).

**Parent Topic:**[Creating external content connectors](creating-ext-cont-connectors.md)

