---
title: Pre-discovery phase
description: The pre-discovery phase involves preparatory steps, such as defining scanning parameters and configuring credential details, to ensure a smooth initiation of the certificate discovery process.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Certificate Inventory and Management process flow, Exploring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Pre-discovery phase

The pre-discovery phase involves preparatory steps, such as defining scanning parameters and configuring credential details, to ensure a smooth initiation of the certificate discovery process.

## Discovery via Ports

The port probe \[tls\_ssl\_certs\] automatically scans 14 default preauthorized ports. The port probe \[tls\_ssl\_certs\] automatically scans 14 default preauthorized ports.

-   Typical ports for SSL: 443, 8443, 9443, 636 \(ldaps\), 993 \(imaps\), 995 \(popssl\), 989, 990
-   StartTLS ports: 25 \(smtp\), 110, 143, 389, 21, 587 \(smtp\)

As part of the CI Discovery process during Shazzam, the MID Server uses scanners to gather certificate chain information from the IP port number, capturing diverse attributes, including the certificate hierarchy. The MID Server then transforms these certificates into an XML payload, sharing it with the instance. The Shazzam sensor, in turn, detects the ECC queue entry and inserts a new record into the Discovered Certificate table \[sn\_disco\_certmgmt\_certificate\_history\].

The following fields are pulled from the XML payload and verified in java code from the Shazzam TLS port probe for discovered certificates: certificate id, revocation\_status, subject, issuer, sans/, is\_self\_signed, is\_ca, valid\_from, valid\_to, signature\_algorithm, fingerprint\_algorithm, key\_size, serial\_number, and version.

## Discovery via URL

The Certificate URL \[sn\_disco\_certmgmt\_cert\_url\] table holds a list of URLs to target for certificate discovery. Each record also has an optional reference to the Unique Certificate \[cmdb\_ci\_certificate\] table, to see what certificate is related to the given URL definition. The necessary parameters from the Discovery Schedule are combined to create and initialize the Discovery status. The \[CertificateDiscoveryFromURLScan\] probe discovers the certificate chain for each of the URLs in the batch and outputs an XML payload that contains the certificate chain for each certificate. It also adds a new record into the Discovered Certificate \[sn\_disco\_certmgmt\_certificate\_history\] table.

## Discovery via Import Certificates \(Version 1.1.7 Certificate Inventory and Management\)

The Import certificates are discovered through the Import SSL Certificate pattern, which relies on the following parameters.

-   Host name/IP where the certificates are hosted
-   Folder where certificates are located
-   TLS\_keepOriginalCertificate: Setting this parameter to true may lead to increased payload size, potentially causing out-of-memory issues.
-   Mid\_temp\_folder: The temporary folder on the MID Server where files will be temporarily copied.

**Note:** Auto-select MID Server option is NOT supported for Windows and Linux mid combinations. If the MID Server is used for storing the original certificates files, then Host name/IP should be set to blank or localhost and the particular MID Server should be selected for the Discovery schedule.

## Discovery via CA authority \(Version 1.1.7 Certificate Inventory and Management\)

Once the Certificate Inventory and Management credential is set up with either GoDaddy, DigiCert, Entrust, or Sectigo Certificate Authority and the Discovery schedule runs, the specific CA pattern makes REST API calls to \(GoDaddy, DigiCert, Entrust, or Sectigo\), collects certificate information, retrieves the list of certificates, and stores it in the \[cmdb\_ci\_certificate\], \[certificate\_domain\], and \[sys\_attachment\] tables.

ca\_api\_url and ca\_api\_version are optional parameters. If these parameters are left empty inside pattern parameters, default values will be used. The default values include:

-   DigiCert - Certificate Management \(ca\_api\_version = v2, ca\_api\_url = https://www.digicert.com/services/\)
-   Entrust - Certificate Management \(ca\_api\_version = v2, ca\_api\_url = https://api.entrust.net/enterprise/\)
-   GoDaddy - Certificate Management \(ca\_api\_version = v1, ca\_api\_url = https://api.godaddy.com/\)
-   Sectigo - Certificate Management \(ca\_api\_version = v1, ca\_api\_url = https://cert-manager.com/api/ssl/\)

The arguments for GoDaddy, DigiCert, Entrust, and Sectigo patterns are as follows. Starting from Version 1.2.0, you have the capability to scan Sectigo and Entrust Certificate Authorities \(CAs\).

-   Start\_offset: The offset position for reading certificates from CA authorities, with a default value of 0.
-   Limit: The number of certificates to be read from the start\_offset, with a default value of 1500.
-   CredentialAlias: The name of the Credential Alias or Tag linked to the CA credentials, added in the serverless execution pattern configuration.

    If the TLS\_keepOriginalCertificate parameter is set to true, the certificate file is attached to the Certificate CI. This may increase payload size, potentially causing out-of-memory issues.

-   IncludeCertStatus: A parameter for specifying additional certificate states to discover, in addition to the defaults.

<table id="table_oxz_j2d_j1c"><thead><tr><th>

Certificate Authority

</th><th>

Default States Discovered

</th></tr></thead><tbody><tr><td>

Sectigo

</td><td>

-   Issued
-   Expired


</td></tr><tr><td>

DigiCert and GoDaddy

</td><td>

-   Active
-   Expired
-   Revoked
-   Canceled


</td></tr><tr><td>

Entrust

</td><td>

-   Active
-   Expired
-   Revoked


</td></tr></tbody>
</table>    You can include multiple certificate statuses by separating each with commas.


**Note:** The **state** field in the Unique Certificate \[cmdb\_ci\_certificate\] table denotes the life cycle state of the certificate, not the raw state from the API. If the API returns states such as issued, valid, expired, or canceled, they are stored as "issued" in the Unique Certificate \[cmdb\_ci\_certificate\] table.

Once the pre-discovery phase is completed, move on to the [post-discovery phase](cert-inventory-mgmt-process-post-discovery.md).

