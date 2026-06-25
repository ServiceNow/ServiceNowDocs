---
title: System properties to send data
description: Review the system properties for TISC integrations to combine with SIRW. You can configure these properties to control how both applications manages the integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/tisc-integrations-system-properties.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Send data from SIR Workspace to TISC, TISC integration within SIR Workspace, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# System properties to send data

Review the system properties for TISC integrations to combine with SIRW. You can configure these properties to control how both applications manages the integrations.

## Key considerations

The system properties for TISC integrations provide advanced configuration options on how the application handles observables and enrichments.

1.  To set TISC integrations system properties within SIRW, navigate to the **System Properties** for Threat Intelligence and access the \[sys\_properties\] table.
2.  The system properties control and handles the behavior of each individual data push operation.
3.  When the property is enabled then the data is pushed automatically when the observables or enrichments data is generated in the SIR Workspace.
4.  If the property is disabled, then the data is pushed manually and allows the users to push data using the UI actions from the SIR Workspace.

The following lists shows the system properties for TISC - SIR integration:

-   Push observables data both automatically and manually from SIR: Enable sn\_ti.allow\_observable\_and\_enrichment\_records\_push property to push the data either automatically or manual. If disabled, this property will disable both automatic and manual mode for all the data push from SIR.
-   Push threat lookup results: Enable this sn\_ti.automatic\_push\_threat\_lookup\_results system property to push threat lookup data automatically to TISC. If disabled, security analysts can still push the threat lookup data manually.
-   Push sighting search results to TISC: Enable sn\_ti.automatic\_push\_sighting\_results\_to\_tisc this system property to push sighting search data automatically to TISC. If disabled, security analysts can still push the sighting search data manually.
-   Push observables: Enable sn\_ti.automatic\_push\_observable\_to\_tisc this system property to push observables data automatically to TISC. If disabled, security analysts can still push the observables data manually.
-   Push enrichment results: Enable sn\_ti.automatic\_push\_enichment\_results this system property to push enrichment results data automatically to TISC. If disabled, security analysts can still push the enrichment results data manually.

**Parent Topic:**[Send data from SIR Workspace to TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/send-sir-to-tisc.md)

**Related topics**  


[Add security incident to TISC case]()

[Add observables to TISC Case]()

[Send Observables to TISC]()

[Send Threat Lookup to TISC]()

[Send Sighting Search to TISC]()

[Send Observable Enrichment to TISC]()

