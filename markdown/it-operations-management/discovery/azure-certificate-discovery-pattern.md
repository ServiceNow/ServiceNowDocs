---
title: Azure Key Vault certificate discovery
description: Cloud Discovery uses Patterns to discover Azure Key Vault certificates. Discovering this data requires installing and updating Discovery and Service Mapping Patterns and Certificate Inventory and Management.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Certificate Inventory and Management patterns, Certificate Inventory and Management reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Azure Key Vault certificate discovery

Cloud Discovery uses Patterns to discover Azure Key Vault certificates. Discovering this data requires installing and updating Discovery and Service Mapping Patterns and Certificate Inventory and Management.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify the configuration of an Azure account**

    For more information, see [Discovery for cloud environment](../concept/cloud-discovery-wizard.md)

-   **Verify the installation of the plugins**

    Certificate Inventory and Management \(sn\_disco\_certmgmt\), at least 3.4.0

    Discovery and Service Mapping Patterns \(sn\_itom\_pattern\), at least 1.12.0

-   **Verify the configuration of the system property**

    Verify that the **sn\_itom\_pattern.issuer\_certificate\_search\_by\_idn** set to **True** to configure Discovery to search issuers by issuer distinguished name only. Discovery can't calculate fingerprint for each certificate in the chain because Key Value Certificates PFX records don't contain certificate chains.

-   **Verify the MID Server requirements**

    The MID Server must have either **ALL** capability or **Azure** capability.

-   **Verify the configuration of Cloud Discovery schedule**

    For more information, see [Create a discovery schedule in Cloud Discovery Workspace](../task/cloud-operations-disco-create-schedule.md)


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Data collected by Discovery during horizontal discovery

The **Azure – Key Vault Certificates** pattern support the discovery of the following table and fields.

<table id="table_w2j_l53_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Unique Certificates \[cmdb\_ci\_certificate\] ​

</td></tr><tr><td>

Name

</td><td>

The host name/domain associated with the certificate.

 For example, *\*.service-now.com*

</td></tr><tr><td>

Serial Number

</td><td>

The serial number of the certificate. For example, *70 d8 c9 52 77 1c 2d 54 97 00 0e 21 05 84 dd 76 b5 e8 c1 73*

</td></tr><tr><td>

Subject common name

</td><td>

The host name/domain associated with the certificate. For example, *\*.service-now.com*

</td></tr><tr><td>

Subject distinguished name

</td><td>

The distinguished name of the entity that the certificate is issued to.​

 The subject distinguished name consists of the following

-   Common name \(CN\).
-   Organization \(O\)- The organization that owns the domain that the certificate is issued to.
-   organizational unit \(OU\)- The organizational unit that owns the domain that the certificate is issued to.

</td></tr><tr><td>

Issuer common name

</td><td>

The common name of the certificate issuer. For example, Entrust Certification Authority.

</td></tr><tr><td>

Issuer distinguished name

</td><td>

The distinguished name of the certificate issuer.

 The issuer distinguished name consists of the following

-   Common Name \(CN\)- the authority that issued the certificate. For example, *Entrust Certification Authority*.
-   Organization \(O\)- The organization that issued the certificate. For example, *"Entrust", Inc*.
-   Organizational Unit \(OU\)- The unit that has the legal rights to issue the certificate.

</td></tr><tr><td>

Renewal tracking

</td><td>

Indicates whether to create any priority 1 or priority 3 tasks for the expiring certificates.

 Discovery sets **Renewal tracking** to *priority3* when the system property *glide.discovery.certs.enable\_renewal\_task\_creation\_for\_discovered\_certificates* is set to **true**.

</td></tr><tr><td>

Valid From

</td><td>

The certificate is valid from this date \(UTC\). For example, *2023-09-25 10:43:03*

</td></tr><tr><td>

Valid To

</td><td>

The expiry date of the certificate \(UTC\). For example, 2024-09-24 10:43:03

</td></tr><tr><td>

Subject organization

</td><td>

The organization \(O\) that the certificate is issued to.

</td></tr><tr><td>

Subject organizational unit

</td><td>

The organizational unit \(OU\) that the certificate is issued to.

</td></tr><tr><td>

Subject country

</td><td>

The country \(C\) of the organization that the certificate is issued to. Populated in a two-letter country code.

</td></tr><tr><td>

Subject state

</td><td>

The region, state \(ST\), or province of the organization that the certificate is issued to. Populated with two-letter code.

</td></tr><tr><td>

Subject locality

</td><td>

The city, location \(L\) of the organization that the certificate is issued to.

</td></tr><tr><td>

Subject email

</td><td>

The email address of the organization that the certificate is issued to.

</td></tr><tr><td>

Issuer

</td><td>

A reference to the entity that signed and issued the certificate. The reference is available if the issued certificate is a part of the same payload.

</td></tr><tr><td>

Root Issuer

</td><td>

A reference to the root certificate. The reference is available if the issued certificate is a part of the same payload.

</td></tr><tr><td>

Subject alternative name

</td><td>

The name of the certificate domain record.

</td></tr></tbody>
</table>## CI relationships

The **Azure – Key Vault Certificates** pattern support the discovery of the following relationships:

|CI|Relationship|CI|
|---|------------|---|
|Unique Certificate​ \[cmdb\_ci\_certificate\]|Hosts::Hosted on|Azure Datacenter​ \[cmdb\_ci\_azure\_datacenter\]​|
|Unique Certificate ​\[cmdb\_ci\_certificate\]​|Hosts::Hosted on|Cloud Service Account​ \[cmdb\_ci\_cloud\_service\_account\]​|
|Key Value​ \[cmdb\_key\_value\]​|Reference​|Unique Certificate​ \[cmdb\_ci\_certificate\]​|

**Parent Topic:**[Certificate Inventory and Management patterns](cert-invt-mgmt-patterns.md)

