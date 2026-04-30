---
title: Palo Alto Networks Next-Generation Firewall integration
description: Once installed and configured, the security incident analyst uses this integration to block malicious IP addresses, URLs, and domains using External Dynamic List \(EDL\) capabilities with the ServiceNow Security Incident Response \(SIR\) products. The security incident analyst creates entries for an EDL from observables determined to be malicious on ServiceNow SIR security incidents.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Palo Alto Networks Next-Generation Firewall integration

Once installed and configured, the security incident analyst uses this integration to block malicious IP addresses, URLs, and domains using External Dynamic List \(EDL\) capabilities with the ServiceNow Security Incident Response \(SIR\) products. The security incident analyst creates entries for an EDL from observables determined to be malicious on ServiceNow SIR security incidents.

An EDL is a text file that is hosted on an external web server. For this integration, this web server is your ServiceNow AI Platform instance, which permits the Palo Alto Networks Next-Generation Firewall to import objects that are included in the list, IP addresses, URLs, and domains, and to enforce policy.

To enforce policy on the EDL entries, the list is referenced in a policy rule or profile. As the EDL entries are modified, the firewall dynamically imports the list at the configured interval and enforces policy without a configuration change or a commit on the firewall. For this integration, ServiceNow AI Platform has created a table containing EDL entries that are retrieved by authorized Palo Alto Networks Next-Generation Firewall at the configured retrieval intervals.

The integration includes the following features:

-   Flexibility to create multiple EDLs that apply to different firewall deny or allow policies.
-   Detailed reporting on the types of sites being blocked \(phishing, malware, and allow listed sites\).
-   Tagging of ServiceNow AI Platform security incidents with EDL entries by the observable type \(URL, domain, IP address\).
-   Configuring EDL expiration periods to maintain EDL list size by automatically expiring or removing older entries.
-   Searching, deleting, or migrating EDL entries between EDL lists.
-   Linking EDL entries to observable records and security incidents that include threat intelligence results and details about why an entry is blocked.

The integration requires that the \(com.snc.security\_incident\) and \(com.snc.secops.orchestration\) plugins from the Security Incident Response product are activated.

This integration only supports Palo Alto Networks \(PAN-OS 8.x\). Earlier versions are not supported.

**Note:** The following topics are numbered. For a smooth installation, configuration, and verification of expected results, follow the topics in the order they are presented.

1.  [Create a certificate profile for the Palo Alto Networks Next-Generation Firewall](paloalto-create-cert-profile.md)  
The integration requires a certificate profile to validate and authenticate the secure connection between the ServiceNow AI Platform® server and the Palo Alto Networks Next-Generation Firewall server.
2.  [Set up and install Palo Alto Networks Next-Generation Firewall](../task/paloalto_install.md)  
Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation.
3.  [Create the API account role for Palo Alto Networks Next-Generation Firewall](../task/paloalto-create-snrole.md)  
An API account role is required in your ServiceNow AI Platform® instance for this integration. The Username and Password associated with this account are created in the ServiceNow AI Platform® and entered in Palo Alto Networks so the Palo Alto Networks Next-Generation Firewall authenticates with the ServiceNow AI Platform® when retrieving EDL entries.
4.  [Supported External Dynamic Lists for Palo Alto Networks Next-Generation Firewall](../reference/paloalto_supported_edls.md)  
The ServiceNow Palo Alto Networks Next-Generation Firewall integration supports External Dynamic Lists \(EDLs\) that accept IP, URL, and domain observables.
5.  [Create an EDL for Palo Alto Networks Next-Generation Firewall](../task/palo_alto_config_edl.md)  
Create an External Dynamic List \(EDL\) in your ServiceNow AI Platform instance. Once approved and activated, you can create entries for EDLs from observables determined to be malicious on ServiceNow AI Platform Security Incident Response \(SIR\) incidents and request approval to block them.
6.  [Activate an EDL for Palo Alto Networks Next-Generation Firewall](../task/paloalto-activate-edl.md)  
After the External Dynamic List \(EDL\) has been created in your ServiceNow AI Platform® and the URL is available, the Palo Alto Networks firewall administrator configures the EDL in the Palo Alto Networks Next-Generation Firewall. The retrieval URL is used by the Palo Alto Networks firewall administrator to configure the EDL in the Palo Alto Networks Next-Generation Firewall server. Before it can accept EDL entries, the EDL must be configured in Palo Alto Networks and activated in the ServiceNow AI Platform®.
7.  [Submit EDL entries from a security incident record for Palo Alto Networks Next-Generation Firewall](../task/paloalto-submit-edl-snsi.md)  
Observables attached to a security incident record are submitted for approval as External Dynamic List \(EDL\) entries to EDLs. An approval process for EDL entries is part of the preconfigured workflow. The firewall imports EDL entries — IP addresses, URLs, domains — that are included in EDL lists and enforces policy.
8.  [Submit EDL entries from the blocklist for Palo Alto Networks Next-Generation Firewall](../task/paloalto-submit-entry-fm-blklist.md)  
For observables determined to be malicious, and not associated with a specific ServiceNow AI Platform security incident, you submit External Dynamic List \(EDL\) entries from the blocklist.
9.  [Approve EDL entries for Palo Alto Networks Next-Generation Firewall](../task/paloalto-apprv-edl-entries-sncr.md)  
An approval process for External Dynamic List \(EDL\) entries is part of the preconfigured workflow. You approve EDL entries before the entries are activated on EDLs. One you approve the EDL entry, the firewall retrieves the entry, and your observable is blocked from that point forward.
10. [EDL entry exceptions for Palo Alto Networks Next-Generation Firewall](../reference/paloalto-edl-execptions.md)  
There are restrictions for adding External Dynamic List \(EDL\) entries to EDLs. If duplicate, compatibility, or CIDR \(Classless Inter-Domain Routing\) conflicts exist when you try to add EDL entries to EDLs, error messages are displayed that help you resolve these errors.
11. [\(Optional\) Edit the security tag name for Palo Alto Networks Next-Generation Firewall](../task/paloalto_edit_sectag_name.md)  
If the **Display tag** check box is selected when you create the External Dynamic List \(EDL\) record, you can edit the tag names and colors of the security tags. Security tags help you track observables that are already blocked.
12. [Uninstall](../task/paloalto-unistall.md)  
If you want to uninstall Palo Alto Networks Next-Generation Firewall from your ServiceNow AI Platform instance and remove all remnants from the integration, refer to the ServiceNow documentation site for instructions on uninstalling applications.

**Parent Topic:**[Security Incident Response integrations](../../security-incident-response/concept/sir_integrations.md)

