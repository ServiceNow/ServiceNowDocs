---
title: Certificate management with CyberArk Certificate Manager SaaS
description: The ServiceNow Certificate Inventory and Management application has been integrated with CyberArk Certificate Manager SaaS for automated certificate life-cycle management, providing centralized certificate provisioning, renewal, and revocation capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/cim-cyberark-venafi-integration.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-12-19"
reading_time_minutes: 2
keywords: [CyberArk Certificate Manager SaaS integration]
breadcrumb: [Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate management with CyberArk Certificate Manager SaaS

The ServiceNow Certificate Inventory and Management application has been integrated with CyberArk Certificate Manager SaaS for automated certificate life-cycle management, providing centralized certificate provisioning, renewal, and revocation capabilities.

## Integration overview

The integration connects Certificate Inventory and Management with CyberArk Certificate Manager SaaS to automate certificate operations so you can use the certificate management capabilities of CyberArk while maintaining centralized visibility and control through Certificate Inventory and Management.

Automated certificate requests, renewals, and revocations are handled through routing policies that direct certificate operations to the appropriate CyberArk certificate authority. Certificate life-cycle events are tracked and managed within Certificate Inventory and Management.

**Note:** Automated certificate renewal for CyberArk is managed by the CyberArk Certificate Manager SaaS platform. Certificate Inventory and Management does not trigger auto-renewal for CyberArk-managed certificates from your instance.

## Key benefits

-   Centralized certificate life-cycle management: Request, renew, and revoke certificates managed by CyberArk directly from Certificate Inventory and Management, without switching between platforms for certificate operations.
-   Automated certificate provisioning: Automate certificate request and renewal workflows through routing policies, reducing manual effort and the risk of expired certificates causing service outages.
-   Secure private key handling: CyberArk manages private key storage, so private keys aren't transferred to or stored in Certificate Inventory and Management.
-   Change management governance: Certificate operations automatically generate change requests in Certificate Inventory and Management, providing audit trails and compliance documentation for certificate life-cycle events.
-   Centralized visibility: Monitor all CyberArk managed certificates alongside certificates from other providers in the **Certificate Management** workspace.

## Certificate management workflow

Certificate operations follow this process:

1.  Configure CyberArk credentials in Certificate Inventory and Management. For more information, see [Configure CyberArk Certificate Manager SaaS credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/configure-cyberark-venafi-creds.md).
2.  Create routing policies to direct certificate requests to CyberArk. For more information, see [Create routing policies for CyberArk Certificate Manager SaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/create-routing-policy-cyberark.md).
3.  Submit certificate requests and monitor certificate life-cycle events through automated flows:
    -   [Request certificates through CyberArk Certificate Manager SaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/request-cert-cyberark-venafi.md)
    -   [Renew certificates through CyberArk Certificate Manager SaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/renew-cert-cyberark-venafi.md)
    -   [Revoke certificates through CyberArk Certificate Manager SaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/revoke-cert-cyberark-venafi.md)

