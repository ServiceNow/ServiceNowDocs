---
title: Use automated flow for certificate management
description: Certificate and Management streamlines your TLS certificate processes, offering benefits such as improved efficiency and enhanced security. Automating certificate management ensures timely renewal of certificates, which minimizes the risk of expired certificates.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Automated certificate management for TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Use automated flow for certificate management

Certificate and Management streamlines your TLS certificate processes, offering benefits such as improved efficiency and enhanced security. Automating certificate management ensures timely renewal of certificates, which minimizes the risk of expired certificates.

## Before you begin

To use the Microsoft Certificate Authority automated flow, you must install the **ServiceNow IntegrationHub Action Step - PowerShell** plugin and must have an Integration Hub subscription. See [Integration Hub usage and subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/subscription-usage.md) for more information.

Role required: pki\_admin or admin

## Procedure

1.  Set the system property **sn\_disco\_certmgmt.cert\_task\_default\_approval\_group** to the default Approval Group name.

    If the certificate request moves into manual mode, the approval group name is the default group used. For instance, the default group is used if there's no matching policy or more than two matching policies. You can add more than one approval group, separated by commas. The first group on the list, which belongs to the task domain, is used for approval. If no domain-specific group is found, the first name in the global domain list is used.

2.  To set the validity period of the certificate order, update the system property **sn\_disco\_certmgmt.default\_cert\_order\_validity\_period**.

    The default is 730 days \(2 years\).

3.  Add the IP of the Microsoft CA Server.

    -   Add the **ca\_host\_ip** field of the routing policy.
    -   Add the IP of an intermediate server in **ca\_host\_ip** field of the routing policy.
    The intermediate server can be any Windows server in the same domain as the Microsoft CA Server, and has access to the certutil and certreq commands available on Powershell. When an intermediate server is used, the MID Server executes a Powershell script on the intermediate server using Invoke-Command. This command uses a Remote Procedure Call \(RPC\) to run the certutil and certreq commands on the CA Server.

4.  Create the certificate credential and map it to the credential alias.

    Each credential should map using a unique credential alias. For more information, see [Credential alias for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/discovery-credential-alias.md).

5.  Confirm the Certificate and Certificate URL information are in the Certificate Authority \[sn\_disco\_certmgmt\_ca\] and Certificate Authority API URL \[sn\_disco\_certmgmt\_ca\_api\_url\] tables.

    The default URL for DigiCert and Entrust CA Gateway provide all validation type URLs. You can also add additional URLs.

6.  Set the task priority.

    The change requests priority and type are mapped based on the priority of the task. Change requests have the same priority as a task priority, except a change request doesn’t have P5 so in this case it's mapped to P4.

    To change the type of change requests, the change management property **com.snc.change\_management.change\_model.type\_compatibility** must be set to true. The default is False.

    1.  If needed, set the task and change the system property **sn\_disco\_certmgmt.default\_cert\_task\_priority** to configure New and Renew task priorities.

        The priority defaults to P3. The possible values are 1, 2, 3, 4, 5. If the value is 1, the priority sets to P1, and so on. If any invalid value is provided, the priority resets to the default of P3.

    2.  If needed, set the task and change the system property **sn\_disco\_certmgmt.default\_revoke\_cert\_task\_priority** to configure Revoke task priorities.

        The priority defaults to P1. The possible values are 1, 2, 3, 4, 5. If the value is 1, the priority sets to P1 and so on. If any invalid value is provided, the priority resets to the default of P1.

7.  Install the Integration hub plugin \[com.glide.hub.integrations\].

    The \[com.glide.hub.integrations\] plugin isn't required for requesting the DigiCert or Entrust CA Gateway Certificate and tracking the certificate order status. However, if you want to debug the certificate subflow actions or add your own customization flow for DigiCert or Entrust CA Gateway, install this plugin.


