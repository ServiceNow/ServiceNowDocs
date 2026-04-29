---
title: Palo Alto Networks integration
description: Palo Alto Networks integration once configured enables the threat analyst to add malicious IP addresses, URLs, and domains to External Dynamic List \(EDL\) or remove these entries from EDL once confirmed as non-malicious or clean.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Firewall integration, TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Palo Alto Networks integration

Palo Alto Networks integration once configured enables the threat analyst to add malicious IP addresses, URLs, and domains to External Dynamic List \(EDL\) or remove these entries from EDL once confirmed as non-malicious or clean.

An EDL is a text file that is hosted on an external web server. For this integration, this web server is your ServiceNow AI Platform instance, which permits the Palo Alto Networks Firewall to import objects that are included in the list, IP addresses, URLs, and domains.

-   **[Create new EDL for Palo Alto Networks](../task/create-new-edl.md)**  
Create new External Dynamic List \(EDLs\) for Palo Alto Networks. Once you create EDLs, you can start creating entries for those EDLs.
-   **[Palo Alto EDL Approval Rules](../task/tisc-edl-approval-rules.md)**  
Approval rules allows the users to activate the approval work flow required to approve or reject the EDL entries.
-   **[Add Observables to EDL](../task/add-obsesrvables-edl.md)**  
Add observables such as IPs, domains, and hashes to External Dynamic List \(EDLs\).
-   **[Remove Observables from EDL](../task/remove-observables-edl.md)**  
Remove observables from EDL.
-   **[Approve EDL entries for Palo Alto Networks](../task/tisc-approve-edl-entries.md)**  
Approving External Dynamic List \(EDL\) entries is part of the pre configuration. You must approve the EDL entries before the entries are activated on EDLs for the firewall to retrieve the entry and apply the security policy.

**Parent Topic:**[Firewall integration](tisc-security-tools.md)

