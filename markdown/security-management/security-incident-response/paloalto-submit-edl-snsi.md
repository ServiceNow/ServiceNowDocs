---
title: Submit EDL entries from a security incident record for Palo Alto Networks Next-Generation Firewall
description: Observables attached to a security incident record are submitted for approval as External Dynamic List \(EDL\) entries to EDLs. An approval process for EDL entries is part of the preconfigured workflow. The firewall imports EDL entries — IP addresses, URLs, domains — that are included in EDL lists and enforces policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/paloalto-submit-edl-snsi.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit EDL entries from a security incident record for Palo Alto Networks Next-Generation Firewall

Observables attached to a security incident record are submitted for approval as External Dynamic List \(EDL\) entries to EDLs. An approval process for EDL entries is part of the preconfigured workflow. The firewall imports EDL entries — IP addresses, URLs, domains — that are included in EDL lists and enforces policy.

## Before you begin

Role required: sn\_si.analyst for submitting EDL entries. To approve EDL entries: Approval is assigned to sn\_si.admin by default, but this authority can be assigned as required by your organization.

## About this task

Users with the sn\_si.analyst role submit EDL entries by requesting a block on observables attached to a security incident record. Once submitted, an EDL entry with a status of Pending is generated and sent for approval. The following example shows a block request for a URL observable.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**, and select a security incident record to open it.

2.  Select the **Show IoC** related link.

3.  In the Observables related list, select the observables you want to block and from the **Actions on selected rows** list, select **Block Request**.

4.  In the dialog box that is displayed, select the search icon \(\[Omitted image "SearchIcon.png"\] Alt text: Search icon\).

5.  From the list that is displayed, select the EDL you want to attach this entry to.

6.  In the Block Request dialog box with the EDL name displayed in the **Implementation** field, select **Block**.

7.  Navigate to **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Entries** and select **Firewall EDL Entries**.

8.  In the Palo Alto Networks Firewall External Dynamic List Entries list, select your observable in the **Entry value** column to open the record.

    The status is Pending, the Active check box is cleared, and the work notes show that there is a request to add the observable. This EDL Entry request is ready for approval.

    The Entry value and Observable fields show different formats for the URL observable.

    The icon next to the `Observable` field is a link to the ServiceNow AI Platform® Observable table.

    The value in the `Observable` field \(`http://mail.dgtnetworks.com`\) links to the Observable table, and it matches the format that was brought over from the Security Incident Response incident-triggering event.

    The ServiceNow AI Platform® may automatically modify EDL entries so that they are compatible with the Palo Alto Networks EDL URL format.

    In this example, the observable was created with the http:// protocol \(`http://mail.dgtnetworks.com`\), and this format is displayed in the Observable field. The http:// protocol is stripped off automatically from the observable by the ServiceNow AI Platform® so it is compatible with Palo Alto Networks and can be retrieved. As a result, `mail.dgtnetworks.com` is displayed in the `Entry value` field.


## What to do next

Approve EDL entries.

**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto_integration.md)

**Previous topic:**[Activate an EDL for Palo Alto Networks Next-Generation Firewall with a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto_sncr_edl.md)

**Next topic:**[Submit EDL entries from the blocklist for Palo Alto Networks Next-Generation Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto-submit-entry-fm-blklist.md)

**Related topics**  


[EDL entry exceptions for Palo Alto Networks Next-Generation Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto-edl-execptions.md)

