---
title: Manual flow for certificate requests
description: Certificate renewal requests and incidents are automatically created when certificates are about to expire or have expired. For added flexibility and control, you can also manually create requests using the Service Catalog.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-09-17"
reading_time_minutes: 1
breadcrumb: [Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Manual flow for certificate requests

Certificate renewal requests and incidents are automatically created when certificates are about to expire or have expired. For added flexibility and control, you can also manually create requests using the Service Catalog.

A scheduled job examines the Unique Certificates \[cmdb\_ci\_certificate\] table on a daily basis and triggers renewal certificate tasks when a certificate is either expired or nearing expiration.

Things to consider for renewal of certificates:

-   Tasks for certificate renewals are automatically generated 60 days prior to expiration. To modify the timeframe, update the [Discovery property](../reference/r_DiscoveryProperties.md): **glide.discovery.certs.days\_before\_expiration\_to\_create\_renewal\_task**.

    **Note:** It's enough to configure the **glide.discovery.certs.days\_before\_expiration\_to\_create\_renewal\_task system property** for the automatic creation of manual certificate tasks. You don’t need to custom configure the **CertificateNotifier** or other prefilters.

-   Certificate tasks are automatically assigned a Priority 3 - Moderate. Modify the priority by opening the task if necessary.
-   If a certificate task already exists for the current certificate, no additional tasks are created.
-   For renewal certificate tasks and incidents, various fields are automatically pre-populated based on the certificate CI.

    **Note:** The fields **assigned\_to** and **requested\_for** in the renewal task are derived from the **assigned\_to** field in the targeted certificate. Additionally, the **assignment\_group** is carried over from the certificate to the renewal task.

-   If a certificate expires and isn't replaced, a new incident is created. However, only one incident is generated for each expired certificate.
-   To view the certificate incidents list, navigate to **Service Desk** &gt; **Incidents**.

