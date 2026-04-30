---
title: Transport Layer Security \(TLS\) extension classes
description: The CMDB CI Class Models store app adds or updates a class for TLS certificates.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Transport Layer Security \(TLS\) extension classes

The CMDB CI Class Models store app adds or updates a class for TLS certificates.

The app adds class models that extend the CMDB class hierarchy. You can use the added classes as any other CMDB class. Applications such as Discovery and Service Mapping patterns can use these class extensions to populate CIs and discover various technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Transport Layer Security \(TLS\)

TLS is a cryptographic protocol designed to provide communications security over a computer network. The TLS protocol provides privacy and data integrity between communicating computer applications. Once the client and the server have agreed to use TLS, they negotiate a stateful connection by using a handshaking procedure. The server usually provides identification in the form of a digital certificate. The certificate contains the server name, the trusted certificate authority \(CA\) that vouches for the authenticity of the certificate, and the server's public encryption key. The client confirms the validity of the certificate before proceeding. When the handshake is completed, a secured connection is established.

![TLS certificate classes integrated with the CMDB class hierarchy.](../image/CMDBCIClassModels-tls.png "TLS certificate classes integrated with the CMDB class hierarchy")

## Scoped apps certification class

The scoped apps certification class supports TLS certificates. With this class you can proactively manage certificates by keeping stakeholders informed about any impending expiries. Use this extension class to ensure that certificates are monitored and renewed before they expire, to prevent severe outage of production systems.

## Classes

This section lists the relevant classes that the CMDB CI Class Models store app adds or updates. See the class columns table for further details about the columns added for each class.

The CMDB CI Class Models: Release 1.4.0 updates the following class:

|Class|Extends|Description|
|-----|-------|-----------|
|Unique Certificate \[cmdb\_ci\_certificate\]|Configuration Item \[cmdb\_ci\]|A public key certificate in X.509 standard format.|

The CMDB CI Class Models store app changes the Unique Certificate \[cmdb\_ci\_certificate\] class as follows:

-   The **assigned\_to** attribute now depends on the **assignment\_group** attribute so that users in the **assigned\_to** attribute are filtered based on the specified **assignment\_group**.
-   The [Certificate Inventory and Management](https://www.servicenow.com/docs/access?context=cert-inventory-mgmt&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) store app populates the Unique Certificate \[cmdb\_ci\_certificate\] table. The list view for that class does not have a **New** button and you can no longer add new records to the table. This is because there are certain fields that are extracted from binary encoded parameters in the certificate which users may not be able to provide. Also, certificates have to be discovered rather uploaded.
-   You can no longer add or delete attachments in the **Certificate file** attribute.

The CMDB CI Class Models: Release 1.3.0 adds the following classes. For the list of CMDB classes in a base system, including ones that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

|Class|Extends|Description|
|-----|-------|-----------|
|Unique Certificate \[cmdb\_ci\_certificate\]|Configuration Item \[cmdb\_ci\]|N/A|
|Certificate Domain \[certificate\_domain\]|N/A|Fully qualified domain name.|

## Class columns

CMDB CI Class Models: Release 1.4.0 adds the following columns to the respective classes.

<table id="table_kkl_1zm_m3b"><thead><tr><th>

Added columns

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Certificate file

</td><td>

Certificate in an encoded form.

</td></tr><tr><td>

Fingerprint

</td><td>

Hash value of the certificate.

</td></tr><tr><td>

Fingerprint algorithm

</td><td>

Algorithm used to hash the certificate.

</td></tr><tr><td>

Is certificate authority

</td><td>

Indicates whether a certificate is a Certificate Authority \(CA\) or not.

</td></tr><tr><td>

Is selfsigned

</td><td>

Indicates whether the certificate is self-signed or not.

</td></tr><tr><td>

Issuer

</td><td>

Entity that has signed and issued the certificate.Reference: Unique Certificate \[cmdb\_ci\_certificate\]

</td></tr><tr><td>

Issuer common name

</td><td>

Common name of the issuer.

</td></tr><tr><td>

Issuer distinguished name

</td><td>

Distinguished name of the issuer.

</td></tr><tr><td>

Key size

</td><td>

Size of the key used by the signing algorithm.Choices:

-   Create priority 1 tasks
-   Create priority 3 tasks
-   Do not create renewal tasks

</td></tr><tr><td>

Renewal tracking

</td><td>

Indicates whether to create any priority 1 or priority 3 tasks for the expiring certificates.

</td></tr><tr><td>

Root issuer

</td><td>

Root entity that has signed and issued the intermediate certificate.Choices:

-   External
-   Internal

 Reference: Unique Certificate \[cmdb\_ci\_certificate\]

</td></tr><tr><td>

Service type

</td><td>

Indicates whether the certificate is used for external or internal services.

</td></tr><tr><td>

Signature algorithm

</td><td>

The cryptographic algorithm used to sign the certificate.Choices:

-   Issued
-   Installed
-   Revoked
-   Retired

</td></tr><tr><td>

State

</td><td>

Lifecycle states of the certificate.

</td></tr><tr><td>

Subject alternative name

</td><td>

List of fully qualified domain names secured by the certificate.

 Reference: Certificate Domain \[certificate\_domain\]

</td></tr><tr><td>

Subject common name

</td><td>

Identifies the hostname/domain associated with the certificate.

</td></tr><tr><td>

Subject country

</td><td>

Subject's two letter country code.

</td></tr><tr><td>

Subject distinguished name

</td><td>

Identifying information of the subject.

</td></tr><tr><td>

Subject email

</td><td>

Subject's email.

</td></tr><tr><td>

Subject locality

</td><td>

Subject's locality.

</td></tr><tr><td>

Subject organization

</td><td>

Subject's organization.

</td></tr><tr><td>

Subject organizational unit

</td><td>

Subject's organizational unit.

</td></tr><tr><td>

Subject state

</td><td>

Subject's state.

</td></tr><tr><td>

Valid from

</td><td>

Validity start period of the certificate.

</td></tr><tr><td>

Valid to

</td><td>

Validity end period of the certificate.

</td></tr><tr><td>

Version

</td><td>

X.509 version of the certificate.

</td></tr></tbody>
</table>|Added columns|Description|
|-------------|-----------|
|Domain|Fully qualified domain name.|

CMDB CI Class Models: Release 1.3.0 adds no columns.

**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

