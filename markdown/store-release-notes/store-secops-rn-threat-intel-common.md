---
title: Threat Intelligence Support Common release notes
description: Version history for the Security Operations Threat Intelligence Support Common application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-threat-intel-common.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Threat Intelligence Support Common release notes

Version history for the Security Operations Threat Intelligence Support Common application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 13.6.4 - June 2026**
    -   New: Introduced a precedence mode in observable finding mode to control finding upgrades and downgrades.
    -   Fixed: Performance issues caused by inefficient query patterns during MITRE ATT&amp;CK operations have been resolved.
-   **Version 13.6.1 - April 2026**

    New: MITRE DEFEND integration with ServiceNow.

-   **Version 13.6.0 - March 2026**

    New: MITRE DEFEND integration with ServiceNow.

-   **Version 13.5.6 - January 2026**
    -   New:
        -   MITRE DEFEND Framework Integration
            -   Automated ingestion of MITRE DEFEND framework data with normalized and validated database schema.
            -   Interactive graphical visualization of DEFEND techniques, threat entities, and defensive relationships within the SIR Workspace.
-   **Version 13.5.2 - December 2025**

    Fixed: Resolved Null pointer exception appearing in logs when the SIR record is not found. Addressed SIR-TI MITRE ingestion failure by providing proper error messaging when maximum attachment size is set to a lower value and handling missing clean up for MITRE ingestion attachments.

-   **Version 13.5.0 - August 2025**

    Fixed: Sighting count is getting increased when duplicate observables are adding through "Associate Observables".

-   **Version 13.3.2 - May 2025**
    -   Fixed:
        -   Remove Run Orchestration UI Action from task observable table.
        -   TISC Sighting Result column is missing in Sightings Search Result table.
        -   Fixed few issues related to WF to FD migration.
-   **Version 13.3.1 - February 2025**

    Changed: Migrated base system workflows to Flow Designer flows.

-   **Version 13.3.0 - November 2024**

    Fixed a few security bugs.

-   **Version 13.2.2 - August 2024**

    Changed: Supports migration of Workflow to Flow Designer.

-   **Version 13.1.13 - February 2024**

    Fixed: \[Read Replica\] the system property 'last\_run\_to\_compute\_cve\_vit\_count' is removed and find/create a suitable table to store and access the required value.

-   **Version 13.1.12 - December 2023**

    Fixed: Addressed the misconfiguration of table/field ACLs within the com.snc.threat plugin.

-   **Version 13.1.9 - November 2023**
    -   Fixed:
        -   The "Sandbox submission failed" message appears before the submission is processed.
        -   Added a global variable for the script, including MITREAutoExtraction to improve performance.
        -   Over Permissive PWD2 Protection - com\_glide\_web\_service\_consumer\_glideencrypt for TAXII profiles.
-   **Version 13.1.3 - August 2023**
    -   Fixed:
        -   The Observable parser was not working correctly for URLs with IP addresses.
        -   Sandbox submission failed message was prompted before the sandbox submission was processed.
-   **Version 13.1.1 - May 2023**
    -   Fixed:
        -   Threat lookup V2 flows don't support filtering the Block from sharing tagged observables.
        -   Table External References \(sn\_ti\_stix2\_external\_reference\) grows rapidly.
-   **Version 13.0.13 - April 2023**

    Changed: Updated to support this application on the Security Incident Response workspace.

-   **Version 13.0.10 - February 2023**
    -   New: Added changes to support the Security Incident Response workspace.
    -   Fixed: Character limitation on fields like 'Source\_ip,' 'Dest\_ip,' 'Action' for the table Splunk Sighting Search 'sn\_ti\_sighting\_details.'
-   **Version 13.0.9 - December 2022**
    -   Changed:
        -   Added report view ACLs for the following tables:
            -   sn\_ti\_m2m\_indicator\_attack\_mode
            -   sn\_ti\_mitre\_coverage\_mapping
            -   sn\_ti\_mitre\_mitigation\_coverage\_mapping
            -   sn\_ti\_scan
            -   sn\_ti\_stix2\_m2m\_incident\_attack
            -   sn\_ti\_stix2\_m2m\_object
-   **Version 13.0.8 - November 2022**
    -   New:
        -   Introducing a filter that allows running automated threat lookup on an observable only once within a configured duration. Any re-runs for the same observable will be skipped until the configured duration/period has passed.
        -   Introducing a threat lookup finding calculator, which calculates the findings based on the responses received. For third-party integrations that provide the computed results, the threat lookup finding calculator maps the results to supported findings in the system.
        -   Updated observable finding calculations based on recent threat lookup results.
    -   Fixed:
        -   Threat Lookup results created to the wrong domain.
        -   Raw JSON payload is missing when a single sighting result is found.
        -   Issue with observable type classification.
-   **Version 13.0.5 - June 2022**
    -   Fixed:
        -   The payload for ICS/Enterprise attack from MITRE is updated. The fix is to accommodate the payload change.
        -   Follow best practices while updating records.
        -   Cosmetic issues in MITRE-ATTCK card fixed.
        -   Stored Cross-Site Scripting \(XSS\) issue.
        -   Deleted the OOB records shipped for Zeustracker-related Threat sources.
        -   Modify the "Requests per minute \(capability-based\)" rate limit checking script to fix sighting search issues.
-   **Version 13.0.4 - February 2022**
    -   New: Added new Observable category and type
        -   Observable type category: User
        -   Observable type: Username
-   **Version 13.0.3 - January 2022**
    -   Changed:
        -   Submission to Sandbox pop-up window title name is updated.
        -   Added a new Description field to the Sandbox configuration.
-   **Version 13.0.1 - December 2021**
    -   New: Introduced new features related to MITRE ATT&amp;CK framework which improves the ServiceNow AI Platform SOAR capabilities that enable proactive analysis, response, and reporting on threats across the security infrastructure.
    -   Changed: Updated some of the existing features related to MITRE ATT&amp;CK.
-   **Version 12.0.7 - June 2021**
    -   Fixed:
        -   The hash lookup on observables is now working for the Metadefender integration.
        -   The integration run errors for TAXII profiles for large data imports from the MITRE server have been fixed.
        -   Capability framework abstract flows pointing to the wrong observable has been fixed.
        -   Added support for MD5 Observables for Sandbox submissions.
-   **Version 12.0.3 - March 2021**

    Fixed: TAXII end point is updated to MITRE GitHub to optimize the load on MITRE servers. MITRE collections are now pre-populated with the Threat Intelligence Core app.

-   **Version 12.0.0 - December 2020**
    -   New: Introduced the MITRE ATT&amp;CK framework which improves the ServiceNow AI Platform SOAR capabilities that enable proactive analysis, response, and reporting on threats across the security infrastructure.
    -   Changed: As part of the inclusive language initiative, allow list and deny list tags have been replaced with allow list and deny list respectively.
-   **Version 11.0.3 - November 2020**

    New: Enabled report\_view ACLs for sensitive tables and fields.

-   **Version 11.0.1 - September 2020**
    -   New:
        -   Updated Threat Intelligence to support STIX 2.0, STIX 2.1 standards
        -   Visualizer for STIX 2.0, STIX 2.1 objects and relationships
-   **Version 10.3.1 - June 2020**
    -   Fixed:
        -   Bug fix for WHOIS Integration configuration tile to support special characters.
        -   Bug fix for report\_view ACL.
-   **Version 10.0.0 - March 2020**

    New \(in v10.0.0\) Capability flows for Integration capability framework v2.0.

-   **Version 9.1.0 - January 2020**
    -   Fixed:
        -   Nodes no longer run out of memory when the TAXII integration \(STIXParser\) parses a large XML file
        -   Manual threat lookup for observables when the Security Incident Response UI app is not installed
-   **Version 8.0.10 - September 2019**
    -   Fixed:
        -   Nodes running out of memory when the TAXII integration \(STIXParser\) parses a large XML file
        -   Manual threat lookup for observables when Security Incident Response UI app is not installed
-   **Version 8.0.9 - June 2019**

    Refer to Security Incident Response release notes for product changes and updates in the Madrid release.


