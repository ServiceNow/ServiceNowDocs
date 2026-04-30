---
title: RISKIQ SSL certificate lookups that return an exact match
description: RISKIQ SSL certificate lookup results for an exact match are displayed on the SSL Certificates tab on the security incident record. An exact match provides a valid certificate authority name, which helps a security incident analyst determine the validity of a website.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Verify expected results for RISKIQ SSL certificate lookups, RISKIQ and WHOISIQ integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# RISKIQ SSL certificate lookups that return an exact match

RISKIQ SSL certificate lookup results for an exact match are displayed on the **SSL Certificates** tab on the security incident record. An exact match provides a valid certificate authority name, which helps a security incident analyst determine the validity of a website.

## Exact match for a valid SSL certificate

The following example shows a valid issuer of an SSL certificate from an exact match in the lookup results. Follow the steps to view the results and raw data.

**Note:** The figures in the following examples are shown with the **Tabbed forms** setting active in the System Settings. If your screen does not match the view shown below, follow the steps to set tabbed forms.

1.  In the upper-right corner of the banner frame, click the Settings icon.
2.  In the **System Settings** dialog box that is displayed, click **Forms** and verify that **Tabbed forms** and **With the Form** are selected.

1.  In the security incident record, click the **SSL Certificates** tab.

    ![SSL Certificates tab on the Security Incident record.](../image/riskiq-ssl-cert-callout.png "SSL Certificates tab")

    Information about the certificate issuer’s name, the issuer's organization, and who the certificate is issued to \(Organization\) is displayed along with other data.

    18 items are displayed in the **Issuer Name** column. The second item \(`R3`\) provides a valid certificate authority name \(`Let's Encrypt`\) in the **Issuer Organization** column.

    No information in the **Issuer Organization** and **Issued to** columns is displayed for the second item \(`mail.dgtnetworks.com`\).

2.  Click the second item in the **Issuer name**column, which is \(**R3**\) to open the entry record. Alternatively, click the information icon next to the item followed by **Open record**.
3.  Select the **Raw Data** tab.

    ![Raw data tab.](../image/riskiq-valid-ssl.png "Raw Data tab")

    The SSL Certificate Entry record includes the observable in the **Raw Data** tab under the **Entity name** column, as well as other data.

    Note in the **Category** column, the `Subject`, and `Issuer` correspond to recognizable entities in the **Entity name** column. The issuer of this certificate is most likely valid and from a trusted public certificate authority. Also note, the `Subject`, and `Issuer` are different entities. These separate entities indicate that the certificate is not an internally signed certificate from an unknown certificate authority.


## Exact match for a self-signed SSL Certificate

The following example shows results for a self-signed SSL certificate from the lookup. Follow the steps to view the results and raw data.

1.  Navigate back to the security incident record. In the **Issuer Name** column, click the other item \(**mail.dgtnetworks.com**\).

    ![SSL Certificate Results tab.](../image/riskiq-ssl-cert-callout1.png "SSL Certificates tab")

2.  On the open record, select the **Raw Data** tab.

    ![SSL Raw Data tab.](../image/riskiq-selfsigned-ssl.png "Raw Data tab")

    The **Category** column indicates the `Issuer` \(`mail.dgtnetworks.com` and `dgtsbs.DGTNetworks.local`\) are not trusted public certificate authorities. Also note the `Issuer` and `Subject` are the same entity \(`dgtsbs.DGTNetworks.local`\), and each contains the name of the observable \(`dgtsbs`\). This certificate is possibly a self-signed certificate. Self-signed certificates may warrant further investigation, as these certificates are not issued by a known certificate authority.


**Parent Topic:**[Verify expected results for RISKIQ SSL certificate lookups](../task/verify-expected-rslts-for-riskiq.md)

