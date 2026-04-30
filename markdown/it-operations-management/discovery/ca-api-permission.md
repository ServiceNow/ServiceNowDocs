---
title: Certificate authorities pattern API elements and permissions
description: Explore the Certificate Authorities \(CA\) pattern API elements and permissions for comprehensive insights into the associated functionalities and authorization requirements.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Certificate Inventory and Management reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate authorities pattern API elements and permissions

Explore the Certificate Authorities \(CA\) pattern API elements and permissions for comprehensive insights into the associated functionalities and authorization requirements.

<table id="table_m4p_ftg_j1c"><thead><tr><th>

Certificate Authorities

</th><th>

API element

</th></tr></thead><tbody><tr><td>

GoDaddy

</td><td>

-   \* /v1/certificates
-   \* /v1/certificates/\{certificate\_id\}/download

</td></tr><tr><td>

DigiCert

</td><td>

-   \* /services/v2/order/certificate
-   \* /services/v2/certificate/\{certificate\_id\}/chain

</td></tr><tr><td>

Entrust

</td><td>

-   \* / v2/certificates
-   \* / v2/certificates/\{certificate\_id\}

</td></tr><tr><td>

Sectigo

</td><td>

-   \* /cert-manager/api/ssl/v1
-   \* /cert-manager/api/ssl/v1/collect/\{certificate\_id\}/pem

</td></tr></tbody>
</table>The patterns available with Certificate Inventory and Management Version 1.1.7 are:

-   GoDaddy
-   DigitCert

The patterns available with Certificate Inventory and Management Version 1.2.0 are:

-   Entrust
-   Sectigo

**Parent Topic:**[Certificate Inventory and Management reference](cert-invt-mgmt-references.md)

