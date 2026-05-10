---
title: Java KeyStore and Windows Certificate Store discovery
description: Discovery uses the Collect Certificates extension section of the Linux Server and Windows OS – Servers patterns to discover certificates stored in the Java KeyStore or Windows Certificate Store. Discovering the certificate information requires installing and updating Discovery and Service Mapping Patterns and Certificate Inventory and Management.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Certificate Inventory and Management patterns, Certificate Inventory and Management reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Java KeyStore and Windows Certificate Store discovery

Discovery uses the **Collect Certificates** extension section of the **Linux Server** and **Windows OS – Servers** patterns to discover certificates stored in the Java KeyStore or Windows Certificate Store. Discovering the certificate information requires installing and updating Discovery and Service Mapping Patterns and Certificate Inventory and Management.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the following plugins are up to date**
    -   Discovery and Service Mapping Patterns \(sn\_itom\_pattern\), at least 1.12.0
    -   Certificate Inventory and Management \(sn\_disco\_certmgmt\), at least 3.4.0
-   **Verify that the pattern is enabled**

    The **Collect Certificates** pattern extension is disabled by default. On the **Discovery Patterns** list, verify that the **Collect Certificates** pattern extension has the **Active** field set to **true**.

-   **Verify the configuration of the Java KeyStore credentials**

    In the **Discovery Credentials** module, select **jks credentials**. Make sure you configured the Discovery IP Affinity. In the **Type** field, insert `java_keystore`. For more information, see [Get started with credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/credentials-getting-started.md)

-   **Verify the configuration of the Discovery schedule**

    For more information, see [Running discoveries in your network](../../discovery/concept/running-discoveries.md)


## Data collected by Discovery during horizontal discovery

The **Collect Certificates** extension section of the **Linux Server** and **Windows OS – Servers** patterns support discovery of the following table and fields.

<table id="table_w2j_l53_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Unique Certificates \[cmdb\_ci\_certificate\] ​

</td></tr><tr><td>

Fingerprint \[fingerprint\]

</td><td>

The certificate fingerprint number.

</td></tr><tr><td>

Serial Number \[serial\_number\]

</td><td>

The serial number of the certificate.

</td></tr><tr><td>

Signature Algorithm \[signature\_algorithm\]

</td><td>

The signature algorithm of the certificate.

</td></tr><tr><td>

Fingerprint Algorithm \[fingerprint\_algorithm\]

</td><td>

The fingerprint algorithm of the certificate.

</td></tr><tr><td>

Issuer distinguished name \[issuer\_distinguished\_name\]

</td><td>

The distinguished name of the certificate issuer.

 The issuer distinguished name consists of the following

-   Common Name \(CN\)- the authority that issued the certificate. For example, *Entrust Certification Authority*.
-   Organization \(O\)- The organization that issued the certificate. For example, *"Entrust", Inc*.
-   Organizational Unit \(OU\)- The unit that has the legal rights to issue the certificate.

</td></tr><tr><td>

Subject distinguished name \[subject\_distinguished\_name\]

</td><td>

The distinguished name of the entity that the certificate is issued to.​

 The subject distinguished name consists of the following

-   Common name \(CN\).
-   Organization \(O\)- The organization that owns the domain that the certificate is issued to.
-   organizational unit \(OU\)- The organizational unit that owns the domain that the certificate is issued to.

</td></tr><tr><td>

Subject common name \[subject\_common\_name\]

</td><td>

The host name or domain associated with the certificate.

</td></tr><tr><td>

Subject country \[subject\_country\]

</td><td>

The country \(C\) of the organization that the certificate is issued to. Populated in a two-letter country code.

</td></tr><tr><td>

Subject State \[subject\_state\]

</td><td>

The region, state \(ST\), or province of the organization that the certificate is issued for. This data is populated with two-letter code.

</td></tr><tr><td>

Subject locality \[subject\_locality\]

</td><td>

The city, location \(L\) of the organization that the certificate is issued for.

</td></tr><tr><td>

Subject organizational unit \[subject\_organizational\_unit\]

</td><td>

The organizational unit \(OU\) that the certificate is issued for.

</td></tr><tr><td>

Subject organization \[subject\_organization\]

</td><td>

The organization \(O\) that the certificate is issued for.

</td></tr><tr><td>

Subject email \[subject\_email\]

</td><td>

The email address of the organization that the certificate is issued for.

</td></tr><tr><td>

Valid From \[valid\_from\]

</td><td>

The certificate is valid from this date \(Displayed in your time zone.\). For example, *2023-09-25 10:43:03*

</td></tr><tr><td>

Valid To \[valid\_to\]

</td><td>

The expiry date of the certificate \(Displayed in your time zone.\). For example, 2024-09-24 10:43:03

</td></tr><tr><td>

State \[state\]

</td><td>

When Discovery collects the certificate the field indicates **installed**

</td></tr><tr><td>

Subject Alternative Name \[subject\_alternative\_name\]

</td><td>

A list of references to alternative host names used by the server.

</td></tr><tr><td>

Issuer \[issuer\]

</td><td>

In this field, there’s a reference to the certificate record. The issuer is the entity that signed and issued the certificate. The reference is available if the issued certificate is a part of the same payload.

</td></tr><tr><td colspan="2">

Installed Certificate \[sn\_disco\_certmgmt\_cmdb\_installed\_certificate\]

</td></tr><tr><td>

Discovery Method \[discovery\_method\]

</td><td>

If a pattern discovered this installed certificate, the field indicates **Pattern**.

</td></tr><tr><td>

Source \[source\]

</td><td>

The IP address of the host server on which discovery is run.

</td></tr><tr><td>

Server \[server\]

</td><td>

The Java-based web server or Windows based web server that store the certificate in java KeyStores on the host machine.

</td></tr><tr><td>

Root Issuer \[root\_issuer\]

</td><td>

A reference to the root certificate record. The reference is available if the issued certificate is a part of the same payload.

</td></tr></tbody>
</table>**Parent Topic:**[Certificate Inventory and Management patterns](../../discovery/reference/cert-invt-mgmt-patterns.md)

