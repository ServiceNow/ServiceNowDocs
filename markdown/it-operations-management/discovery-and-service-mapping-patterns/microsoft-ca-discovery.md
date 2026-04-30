---
title: Microsoft Certificate Authority \(CA\) certificates discovery
description: The ServiceNow Discovery application can discover Microsoft Certificate Authority \(CA\) certificates using the Microsoft CA - Certificate Management pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-04-10"
reading_time_minutes: 3
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Microsoft Certificate Authority \(CA\) certificates discovery

The ServiceNow Discovery application can discover Microsoft Certificate Authority \(CA\) certificates using the Microsoft CA - Certificate Management pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Starting with version 1.27.0, Discovery and Service Mapping Patterns supports discovering the subject alternative name \(SAN\) for both the all request IDs and the template ID discovery methods.

## Prerequisites

-   **Verify the following applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
-   **Verify the certificate Authority process**

    Ensure that the CA process is up and running on the host machine.

-   **Verify previous Windows discovery**

    Verify a Windows host was discovered during a previous horizontal discovery. For more information, see [Windows discovery](../../discovery/reference/r_DataCollDiscoWindowsComputers.md).

-   **Create a serverless discovery schedule**

    Create a discovery schedule to perform targeted discovery of Microsoft CA certificates using the host on which the CA process is running. For more information, see [Create a serverless schedule for Microsoft Certificate Authority \(CA\) discovery](../task/create-serverless-schedule-ms-ca.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Microsoft CA - Certificate Management pattern.

<table id="table_xqd_syx_r2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fingerprint \[fingerprint\]

</td><td>

Hash value of the certificate.

</td></tr><tr><td>

Fingerprint algorithm \[fingerprint\_algorithm\]

</td><td>

Algorithm used to hash the certificate​.

</td></tr><tr><td>

Subject common name \[subject\_common\_name\]

</td><td>

Identifies the host name/domain associated with the certificate, listed in the certificate's **Subject​** field.

</td></tr><tr><td>

Subject distinguished name \[subject\_distinguished\_name\]

</td><td>

Identifying information of the subject listed in the certificate's **Subject​** field.​

</td></tr><tr><td>

Issuer distinguished name \[issuer\_distinguished\_name\]

</td><td>

Distinguished name of the issuer​.

</td></tr><tr><td>

Comments \[comments\]

</td><td>

Includes a readable description for users.

</td></tr><tr><td>

Renewal tracking \[renewal\_tracking\]

</td><td>

Indicates whether to create any priority 1 or priority 3 tasks for the expiring certificates.​

</td></tr><tr><td>

Certificate Template \[cert\_template\]

</td><td>

Certificate template that defines the policies and rules that a CA uses when a request for a certificate is received.

</td></tr><tr><td>

Certificate ThumbPrint \[thumb\_print\]​

</td><td>

Unique identifier for certificates in applications when making trust decisions, in configuration files, and when displayed in interfaces.

</td></tr><tr><td>

Issuer common name \[issuer\_common\_name\]

</td><td>

Common name of the issuer​.

</td></tr><tr><td>

Valid from \[valid\_from\]

</td><td>

Validity start period of the certificate.

</td></tr><tr><td>

Serial Number \[serial\_number\]

</td><td>

Serial number of the certificate.

</td></tr><tr><td>

Subject country \[subject\_country\]

</td><td>

Two-letter country code in the certificate's **Subject​** field.

</td></tr><tr><td>

Subject organization \[subject\_organization\]

</td><td>

Organization listed in the certificate's **Subject​** field.

</td></tr><tr><td>

Issuer \[issuer\]

</td><td>

Entity that signed and issued the certificate.​

</td></tr><tr><td>

Subject organizational unit \[subject\_organizational\_unit\]

</td><td>

Organizational unit listed in the certificate's **Subject​** field..​

</td></tr><tr><td>

Subject alternative name \[subject\_alternative\_name\]

</td><td>

List of fully qualified domain names secured by the certificate​, listed in the certificate's **Subject​** field.

</td></tr><tr><td>

Valid to \[valid\_to\]

</td><td>

Validity end period of the certificate.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the CI.

</td></tr><tr><td>

State \[state\]

</td><td>

Life-cycle state of the certificate​.For example: Installed, Issued, or Revoked.

</td></tr><tr><td>

Root issuer \[root\_issuer\]

</td><td>

Root entity that signed and issued the immediate certificate.

</td></tr><tr><td>

Subject locality \[subject\_locality\]

</td><td>

Locality listed in the certificate's **Subject​** field.

</td></tr><tr><td>

Subject state \[subject\_state\]

</td><td>

State listed in the certificate's **Subject​** field.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Indicates whether the certificate is valid or was revoked. Possible values are:

-   **Operational**: Valid certificate
-   **Non-Operational**: Revoked certificate

</td></tr><tr><td>

Signature algorithm \[signature\_algorithm\]

</td><td>

Signature algorithm of the certificate. For example: SHA-256, sha256RSA, or SHA1withRSA.

</td></tr><tr><td>

Request Type \[request\_type\]

</td><td>

Format used for requesting the certificate.

</td></tr><tr><td>

Request Submission Date \[request\_submission\_date\]

</td><td>

Date that the certificate request was submitted.

</td></tr><tr><td>

Request Resolution Date \[request\_resolution\_date\]

</td><td>

Date that the certificate request was resolved by the CA.

</td></tr><tr><td>

Request Revocation Date \[request\_revocation\_date\]

</td><td>

Date that the certificate was revoked. This field is populated only for revoked certificates.

</td></tr><tr><td>

Effective Revocation Date \[effective\_revocation\_date\]

</td><td>

Date that the certificate was effectively revoked by being added to the Certificate Revocation List \(CRL\). This field is populated only for revoked certificates.

</td></tr><tr><td>

Revocation Reason \[revocation\_reason\]

</td><td>

Reason for the certificate’s revocation. This field is populated only for revoked certificates.

</td></tr><tr><td>

Requester Name \[requester\_name\]

</td><td>

Name of the person who requested the certificate.

</td></tr><tr><td>

Template Enrollment Flags \[template\_enrollment\_flags\]

</td><td>

Information about the certificate that needs to be acted on by the CA or the certificate’s owner. For more information, search for the error code in [the official Microsoft documentation site](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-crtd/ec71fd43-61c2-407b-83c9-b52272dec8a1).

</td></tr></tbody>
</table>## CI relationships

The Microsoft CA - Certificate Management pattern doesn’t create any CI relationships.

-   **[Create a serverless schedule for Microsoft Certificate Authority \(CA\) discovery](../task/create-serverless-schedule-ms-ca.md)**  
Create a serverless discovery schedule to discover Microsoft Certificate Authority \(CA\) certificates.

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

