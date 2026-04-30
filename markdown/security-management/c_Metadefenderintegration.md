---
title: OPSWAT Metadefender integration overview
description: OPSWAT Metadefender is a security solution that provides access to multiple anti-malware machines and easily integrates with Security Operations.The Threat Lookup - OPSWAT Metadefender flow performs a lookup on selected observables. If the observables are of a type recognized by OPSWAT Metadefender, the observables are scanned for malware, and the results are returned.Before you can use the OPSWAT Metadefender integration, you must download it from the ServiceNow Store.If you require an SSL connection for the integration, there are circumstances when the certificate provided by the third-party vendor is either not yet trusted in ServiceNow or has expired. This task is optional.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [OPSWAT Metadefender Integration, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# OPSWAT Metadefender integration overview

OPSWAT Metadefender is a security solution that provides access to multiple anti-malware machines and easily integrates with Security Operations.

Before you can use the OPSWAT Metadefender integration, you must activate the plugin and configure the integration. If necessary, you can also update your X509 SSL certification.

## Threat Lookup - OPSWAT Metadefender flow

The Threat Lookup - OPSWAT Metadefender flow performs a lookup on selected observables. If the observables are of a type recognized by OPSWAT Metadefender, the observables are scanned for malware, and the results are returned.

This flow is triggered by the [Security Operations Integration - Threat Lookup capability](../../../security-operations-common/concept/sec-ops-threat-lookups-capability.md) when you perform a threat lookup on one or more observables, and the OPSWAT Metadefender implementation is selected. For more information, see [Perform lookups on observables](../../../threat-intelligence/task/perform-lookups-on-observables.md).

Role required: sn\_si.admin

![Threat Lookup - OPSWAT Metadefender flow](../image/flows-metadefender.png "Threat Lookup - OPSWAT Metadefender flow")

For information on the activities used by this flow, see [Common Security Operations integration flows and orchestration activities](../../../security-operations-common/concept/common-wf-activities.md).

## Activate and configure the OPSWAT Metadefender integration

Before you can use the OPSWAT Metadefender integration, you must download it from the ServiceNow Store.

### Before you begin

Role required: admin

### Procedure

1.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the integration is complete, access the OPSWAT portal and obtain the Metadefender Cloud API Key

3.  In your instance, navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configuration**.

    The available security integrations appear as a series of cards.

4.  In the OPSWAT Metadefender card, click **Configure**.

5.  Enter \(or paste\) the **API Key** you acquired from the OPSWAT portal.

6.  Click **Submit**.


### Result

After it is configured, OPSWAT Metadefender can be selected for performing lookups on observables in Threat Intelligence and on observables in security incidents.

**Related topics**  


[Perform lookups on observables](../../../threat-intelligence/task/perform-lookups-on-observables.md)

## Update your X.509 certificate

If you require an SSL connection for the integration, there are circumstances when the certificate provided by the third-party vendor is either not yet trusted in ServiceNow or has expired. This task is optional.

### Before you begin

Role required: admin

### Procedure

1.  Acquire the SSL certificate from the third-party vendor.

    For example, you can import an X.509 Certificate \(PEM\) from an SSL endpoint in the Firefox browser, as follows.

    1.  Enter the endpoint URL into the browser address bar.

        For example: `https://<3rdparty>/`.

    2.  Click the lock icon in the address line.

    3.  Click **More Information** and click the **Security** tab.

    4.  Click **View Certificate** and click the **Detail** tab.

    5.  Click **Export** to save the PEM into your local file system.

    6.  Open the saved file in any text editor tool and copy the content to the clipboard.

        It must begin with `-----BEGIN CERTIFICATE-----` and end with `-----END CERTIFICATE-----`.

2.  Navigate to **System Definition** &gt; **Certificates**.

3.  Click **New** and [create a new record](https://www.servicenow.com/docs/access?context=t_UploadACertificateToAnInstance&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for the integration.

4.  In **PEM Certificate**, paste in the certificate you downloaded and copied into the clipboard earlier.

5.  Add the certificate to the Identity Provider record.

    1.  Navigate to **Multi-Provider SSO** &gt; **Identity Providers**.

    2.  Select the active default identity provider for which you created the new certificate.

    3.  Scroll down to **X.509 certificates** related list, and click **Edit**.

    4.  Move the newly created certificate to the **Selected** column.

6.  Click **Save**.

    The other fields in the record are generated automatically.

    **Note:** If you have a certificate that has expired, you need to remove it. For information on how to remove the expired certificate, refer to [KB0691439 Replacing an expiring SAML certificate](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0691439).


