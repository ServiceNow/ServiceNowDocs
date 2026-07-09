---
title: HL7 v2.x Integration release notes
description: Version history for the ServiceNow HL7 v2.x Integration application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-hcls-hl7-v2.x-int.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# HL7 v2.x Integration release notes

Version history for the ServiceNow® HL7 v2.x Integration application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.0.1 - July 2026**
    -   Hospital integration teams rely on HL7 v2.x messaging to keep ADT \(admit, discharge, transfer\) events flowing between EMRs, integration engines, and downstream systems — but connecting that traffic to ServiceNow has traditionally required custom scripting and message parsing built by hand.
    -   HL7 v2.x Integration gives ServiceNow a standards-compliant REST endpoint that accepts raw ER7 HL7 v2.x messages directly from your integration engine \(such as Mirth\), returning standard ACK/NACK responses so your existing retry and monitoring logic keeps working without changes. Every message is logged with queryable metadata extracted from the MSH segment, and a built-in parser engine converts raw messages into structured data pills usable in any Flow Designer flow — no scripting required.
    -   Out-of-the-box parser configs cover the most common ADT events — Admit \(A01\), Transfer \(A02\), Discharge \(A03\), and Update \(A08\) — so operational workflows like room turnover, bed status updates, and care team notifications can be triggered directly from EMR events. Administrators can clone and customize any OOB config for their EMR's specific HL7 variations while ServiceNow maintains an upgradable baseline, and the entire setup and monitoring experience is no-code, built for administrators who think in HL7 terms.

**Parent Topic:**[ServiceNow Store - Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-healthcare-highlights.md)

