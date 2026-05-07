---
title: Palo Alto Networks integration
description: Palo Alto Networks integration after configuration enables the threat analysts to add malicious IP addresses, URLs, and domains to External Dynamic List \(EDL\) or remove these entries from EDL after confirmation as non-malicious or clean.
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

Palo Alto Networks integration after configuration enables the threat analysts to add malicious IP addresses, URLs, and domains to External Dynamic List \(EDL\) or remove these entries from EDL after confirmation as non-malicious or clean.

An EDL is a text file that is hosted on an external web server. For this integration, this web server is your ServiceNow AI Platform instance, which enables the Palo Alto Networks - Firewall to import objects that are included in the list such as IP addresses, URLs, and domains.

-   **[Create EDL for Palo Alto Networks](../task/create-new-edl.md)**  
Create External Dynamic List \(EDLs\) for Palo Alto Networks. After you create EDLs, you can start creating entries for those EDLs.
-   **[Define Palo Alto Networks Approval Rules](../task/tisc-edl-approval-rules.md)**  
Activate approval workflows to require approval or rejection of EDL entries before they take effect.
-   **[Add Observables to EDLs](../task/add-obsesrvables-edl.md)**  
Add observables such as IP addresses, domains, and hashes to External Dynamic Lists \(EDLs\) to automatically update threat intelligence feeds in your security infrastructure.
-   **[Remove Observables from EDL](../task/remove-observables-edl.md)**  
Remove observables from an External Dynamic List \(EDL\) to stop blocking or monitoring specific observables. Use this when observables are no longer relevant or incorrectly categorized.
-   **[Approve EDL entries for Palo Alto Networks](../task/tisc-approve-edl-entries.md)**  
Approving External Dynamic List \(EDL\) entries is part of the pre configuration. You must approve the EDL entries before the entries are activated on EDLs for the firewall to retrieve the entry and apply the security policy.

**Parent Topic:**[Firewall integration](tisc-security-tools.md)

