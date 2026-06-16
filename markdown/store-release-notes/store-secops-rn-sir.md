---
title: Security Incident Response release notes
description: Version history for the Security Operations Security Incident Response on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 13
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Incident Response release notes

Version history for the Security Operations Security Incident Response on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.1.0 - June 2026**
    -   New:
        -   Added granular read and write roles for TISC users.
        -   Added read role for GRC users to access related security incidents
    -   Changed:
        -   Added ITSM AI Native SKU packaging on access to Problem, Change Management, and On-call schedule features.
        -   Removed the inventory\_user role from sn\_si.basic
    -   Fixed:
        -   Fixed an issue where 'Create Security Incident' UI action was visible to ITIL users but were not able to create SIRs.
        -   Fixed inconsistent spacing around the Presence component in the Security Incident record header in SIR Workspace.
        -   Fixed sn\_si\_incident state field dropdown displaying blank labels in non-English locales when locale-specific choice list rows are inactive.
        -   Fixed security tag colors not rendering correctly in SIR Workspace due to missing CSS class definitions for black and blue colors, causing tags to fall back to grey regardless of the configured color.
        -   Created a new role and ACLs for AI Security and Privacy Incidents in SIR scope.
        -   Fixed issues with KMF policy shipped OOB in SIR.
        -   Added form and list view for sn\_si\_ci\_service\_cache in SIR.
        -   Fixed issue where Phishing email was not appearing as a File-type observable in the created SIR.
        -   Fixed installation error logs found while installing the - Security Incident Response store.
        -   Fixed issue where SIR tasks in "Closed Complete" state were incorrectly changed to "Cancelled" when parent SIR is closed.
-   **Version 14.0.1 - March 2026**
    -   New:
        -   Added UI action 'Link as Children' to add similar Security incidents as child to parent security incident
        -   Added capability to support Unmatched Affected User for missing sys\_user records
        -   Capability to allow external users\(of SITs\) to access security incident
    -   Changed:
        -   Restricted removal of manually added security tags
        -   Added support for Groups in Post Incident Review – Assessment Setup User Assignment Rules
    -   Fixed:
        -   Unable to view PIR report with sn\_si.analyst role
        -   "Submit to Sandbox - ESCM Activity" subflow cannot be opened or triggered
        -   Valid URL observable is being incorrectly classified as "Unknown"
        -   'Create Knowledge Article' Checkbox not working correctly when closing security incident in security incident workspace
        -   When "Enforce Restriction" is enabled then the playbook section is not getting auto refreshed after completion of a step/activity
        -   Unable to see the definition field value from workspace on list unless we double click
-   **Version 13.9.33 - February 2026**

    Fixed: Fixed an issue where the System admin was not able to manage the non-security groups without having user\_admin role.

-   **Version 13.9.23 - December 2025**
    -   Fixed:
        -   Linked items cannot be added when choosing all.
        -   When Observable type is changed to File, no error or informative message is populated as attachment is mandatory.
        -   Color contrast issue on the MITRE heatmap.
        -   Urgency is missing from Create Security Incident Response for an incident.
        -   The SIR Observable Type Identification script did not recognize file paths that used a forward slash '/'.
        -   Not able to close informative alert message under Observable Creation for File Type.
        -   Attachments under .eml was not getting created as observables.
        -   Unable to create a new record directly from the table "sn\_si\_m2m\_task\_affected\_user" with an analyst role.
        -   Remove the ATF test cases, which were referring to the workflow templates.
        -   Work notes propagation between an incident to a security incident is not happening.
        -   ACL\(sn\_si\_incident.work\_notes\) description was incorrect.
        -   Privilege Escalation to Global Admin \| Security Incident Response.
    -   Changed:
        -   Clicking widgets on Security Incident Manager overview dashboard displayed an error for sn\_si.manager.
        -   Restrict attachment modifications after security incident closure.
        -   Enhance SIR with native support for third-party risk scoring, integration and prioritization.
        -   Simplify and democratize category management in security incident response.
        -   Enhance user-reported phishing workflow with pattern-based allow/deny rules.
        -   Implement NIST-based incident prioritization in security incident response.
        -   Prevent duplicate escalations from IT Incidents to Security Incidents with confirmation mechanism.
        -   Ability to link multiple problem and change request records to SIR record.
        -   Enable in-line editing of associated observables and findings in SIR Workspace.
        -   Enable flexible creation of multiple linked ITSM records \(INC, CHG, PRB\) from the SIR Workspace.
        -   Flow to PAD conversion: Wrapper Process Generator is not shown with state lanes when we selecting "Generate Process."
        -   Improper use of current.update in BR\(s\) from the Security Support Common product.
        -   Granular Admin Roles - Cobalt Wren - SIR.
        -   Security \[Directive\] Read Only field Security.
        -   Dot-Walk Scoping Bypass - SIR Core.
-   **Version 13.9.21 - September 2025**
    -   Fixed:
        -   On table sn\_ti\_m2m\_task\_observable, the positions are the same for two elements.
        -   MITRE ATT&amp;CK Mappings table \[sn\_ti\_alert\_rules\_mitre\_attack\_technique\_mapping\]
        -   SLA definitions for security incident called '15 minute' and '60 minute' that are supposed to be just part of demo data can get loaded during upgrades.
        -   When viewing an SIR record in any language other than English, the state field reverts back to English.
-   **Version 13.9.0 - August 2025**
    -   New:
        -   Bulk Closure UI and Backend Implementation
        -   Shift Handover start and end date, dynamic record mention and count feature functionality
    -   Changed: Ability to Link Multiple ITSM Records to SIR Record
    -   Fixed:
        -   Implement User Presence feature in ServiceNow Security Incident Response SIR/SIT/SR in SIR Workspace.
        -   Security Incident intermittently fails to load related records in BSM.
        -   When submit Security Incident Catalogs that used variable set:sn\_si.variable\_set in other languages except English, the category of security incident stores a choice label instead of choice value incorrectly.
        -   The regex to detect a link in a phishing email doesn't work.
        -   SIR tickets risk score recalculates on inserting comments.
        -   Child Security Incident Cancelled Instead of Closed.
        -   In dark mode the contrast of the text rendered is too low.
        -   OOTB all the PAD flows were in active state which is not expected.
        -   SIRs are not created from SIEM ingestion due to "Secure Notes" access issue to Crypto module since Yokohama upgrade.
        -   Change integration\_source field type from reference to glide\_list in sn\_si\_incident table.
        -   Security Fixes
-   **Version 13.6.7 - June 2025**
    -   Fixed:
        -   Playbook email has skip feature but cannot skip send email action due to mandatory fields.
        -   Configuration Item \(CI\) not copied to SIR Task from parent Security Incident and CI field not visible in active states.
        -   Compose email in SIR Workspace is having incorrect body/email template.
        -   Automated Phishing Playbook flow which is not checking for work note mandatory configuration while changing the state to closed.
        -   Missing the "Add Observables" Option in Security Incident Workspace in French.
        -   Service Operations Workspace Playbook is overwritten when SIR plugin is installed.
        -   Message "This form has not been configured for Workspace" in Security Incident Response Workspace when previewing a security incident.
-   **Version 13.6.6 - May 2025**
    -   New: Added a new field \(date and time\) to store incident detection time. Tag does not get removed on SIR requests.
    -   Fixed:
        -   kb\_publish\_flow and kb\_retire\_flow field value added for retired kb's related to workflows.
        -   Automatic Threat lookup is working after upgrading the SIR related plugins to latest version and not upgrading the Palo Alto integrations.
        -   Security Incident Response Workspace is available from the Now Experience Search drop-down for analyst persona.
        -   Clean up Security Incident Encryption Context from com.snc.security\_incident plugin.
        -   Remove Run Orchestration UI Action from security incident table.
        -   SIR demo data references the Legacy HR Group Type named "human\_resources" instead of the scoped HR one.
        -   Sighting Search parent flow is not honoring input parameter wait and is running asynchronously.
        -   ACL Bypass via "Create CSM Case Record" Data Broker \| Security Incident Response Workspace.
        -   ACL Bypass due to the usage of GlideRecord.
-   **Version 13.6.5 - March 2025**

    Changed: Supporting changes for generative AI feature, Close Security Incident which is part of Now Assist for the Security Incident Response \(SIR\) application.

-   **Version 13.6.4 - February 2025**
    -   New:
        -   Supporting changes for:
            -   Conference call capability for SIR through Teams/ Zoom/ WebEx for team members and also affected user
            -   Daily Status reporting functionality within SIR via mobile friendly email attachment
    -   Changed:
        -   Supporting changes for migration from workflows to Flow Designer were added for few integrations:
        -   -   McAfee ePO
-   Palo Alto Networks WildFire
-   Store SIR Threat Core
-   Microsoft Exchange On-Premises
-   **Version 13.6.2 - November 2024**
    -   New: Supporting changes for "Now Assist for Security - Post Incident Analysis" using Generative AI.
    -   Changed: Supporting changes for migration from workflows to flows using Flow Designer were added for the following:
        -   Crowdstrike Falcon Insight Integration
        -   CarbonBlack Integration
        -   Splunk Sighting Search Integration
        -   MISP integration
        -   CheckPoint INtegration
        -   Elastic Search integration
        -   Microsoft Defender
        -   Fire Eye HX
        -   Arcisght logger
        -   Palo Alto NGFW
        -   Create IoC Lookup request activity workflow migration
    -   Fixed:
        -   When sending a 'POST' REST payload into ServiceNow to insert an incident record, The response will error with '500 Internal Server Error.
        -   AI search on SI records was failing due to field level ACLs.
        -   Scheduled job - Build cache of critical services CI was failing when use\_cache is activated.
        -   The Security Incident Form on the SIR Workspace was taking 25 to 30 seconds to load the widgets.
        -   Run Additional Triage" sub-flow was unable to add work notes in the parent SIR
        -   Security Incident Response \(SIR\) Parent/Child Relationship Allows Child Incident to be Parent to its Parent Incident, resulting in recursive updates.
        -   Long running job "Lookup Security Incident Observables"
-   **Version 13.5.2 - September 2024**

    Fixed: Block Request is now working on Zscaler.

-   **Version 13.5.1 - August 2024**

    Changed: Migration of workflows to flow designer.

-   **Version 13.4.5 - June 2024**
    -   New: Added Security Incident Response Workspace\(sn\_si\_aw:1.5.1\) as a dependency for Security Incident Response \(sn\_si:13.4.5\).
    -   Fixed: View rules option is now working.
-   **Version 13.4.3 - May 2024**
    -   Fixed:
        -   The 'Secure Attachment' table does not support or consider the file extension property.
        -   Duplication rules updated inactive or closed security incident records when ingesting emails from an email parser.
-   **Version 13.3.6 - March 2024**
    -   Fixed:
        -   Security Incident form gets stuck after changing the configuration item when the "Calculate Severity" business rule is enabled
        -   An error occurs while evaluating the "si\_response\_tasks' template script and when you try to close the security incident
        -   Improved performance of the Critical service-affected security calculator when the "Refresh Impacted Services on CI Change" business rule is enabled
        -   On the Run Additional Actions modal, now the Comment field is set as a mandatory field \(to support Microsoft Defender for Endpoint\)
-   **Version 13.3.4 - February 2024**
    -   Changed: You can now create "Encrypted Field Configurations" records for both secure\_notes and Attachment.
    -   Fixed:
        -   The new task form is now editable for the role "sn\_si.basic".
        -   The Post-Incident Review tab now displays correctly when an assessment is canceled.
        -   The Heisenberg styles no longer distort pages in the Next Experience UI.
        -   The sn\_si\_incident\_import OOTB mapped vulnerability field is now included on the sn\_si\_incident record, preventing errors on the first data load.
        -   Code signing: KMF Signature records are now generated for records of sn\_sec\_core\_integration\_item.
        -   Emails no longer include an extra email address with the recipients of the email.
-   **Version 13.3.2 - December 2023**
    -   New: Added definition metrics for security incident MTTR.
    -   Fixed: Misconfiguration of table/field ACLs within the 'com.snc.security\_incident' plugin.
-   **Version 13.3.0 - November 2023**
    -   Changed:
        -   Added a configurable property to enable or disable the "Post Incident Review" report generation for child security incidents.
        -   Replaced the Knowledge V3 reference with a service portal navigation link.
-   **Version 13.2.2 - September 2023**

    New: Added usage metrics to capture MTTR for security incidents.

-   **Version 13.2.1 - August 2023**

    Fixed:

    -   In the Timeline section at the bottom of the PIR report, the value of the short description is not visible in the bolded header as well as in the values of any of the encrypted fields of the corresponding response tasks \(SITs\).
    -   The field duration metric for sn\_si\_incident.assigned\_to can generate metrics against the wrong table as a result of using 'definition,' which is not set for field duration metrics.
-   **Version 13.1.0 - May 2023**
    -   Fixed:
        -   Security Analyst doesn't have access to modify the 'Read access' and 'Privileged access' fields on the security incident form.
        -   GlideChoiceList is not refreshed every time.
-   **Version 13.0.5 - April 2023**

    Changed: Updated to support this application on the Security Incident Response workspace.

-   **Version 13.0.1 - March 2023**

    Fixed: State choices are not populating for the Security Incident when we switch to the 'NIST Open' process definition.

-   **Version 12.9.9 - February 2023**

    New: Changes to support Security Incident Response Workspace.

-   **Version 12.9.6 - January 2023**

    Fixed: The base system 'report\_view' ACLs for the SIR report are missing.

-   **Version 12.9.5 - December 2022**
    -   Changed:
        -   Added report\_view ACL for the following tables:
            -   sn\_si\_audit\_log
            -   task\_cmdb\_ci\_service
-   **Version 12.9.4 - November 2022**
    -   Fixed:
        -   After submitting a PIR form, the texts \(answers\) get word-wrapped and show as one statement even though the input was entered into different lines.
        -   Security Tag's order in SIR classic UI differs from the one that is created.
        -   Update async BR to the new value of async\_always.
-   **Version 12.9.2 - August 2022**
    -   Fixed:
        -   Non-admin users cannot view the security incident catalog items from the sc\_cat\_Item table.
        -   A closed security incident returns to the review state after the associated problem/incident moves to the closed state.
        -   Security Case form issues in the Sandiego environment.
        -   The "Security Tags Toolbar" field shrinks when placed in a different place on the security incident form.
-   **Version 12.9.1 - March 2022**

    Fixed: Closing the Parent SIR does not close the child security incident when there is a Response task.

-   **Version 12.8.9 - January 2022**

    Changed: Minor changes to the Integrations Capability framework V2.

-   **Version 12.8.1 - December 2021**
    -   Changed: MITRE ATT&amp;CK 2.0 updates
    -   Fixed:
        -   The Security Incident Response module is creating Knowledge articles with the same numbers as current knowledge articles
        -   In the Security Incident table \(sn\_si\_incident\), the metric definition 'Incident State Duration' is incorrectly configured.
-   **Version 12.5.1 - August 2021**
    -   Fixed:
        -   Fixed sighting search work notes to capture the count of external sightings.
        -   Issues related assigning or closing a task.
        -   Fixed mapping between security incident and incident.
-   **Version 12.4.1 - June 2021**

    Fixed: Service portal Security Incident catalog features, email parsing, and scheduled jobs.

-   **Version 12.3.5 - May 2021**

    Changed: Added a few Restricted Caller Access \(RCA\) files from other applications to the Security Incident Response \(SIR\) application.

-   **Version 12.2.7 - February 2021**

    New: Post incident review reports provides the set up capability to create multiple report templates and configure those to align with the security incidents.

-   **Version 12.0.0 - December 2020**
    -   New: Introduced the MITRE ATT&amp;CK framework which improves the ServiceNow AI Platform SOAR capabilities that enable proactive analysis, response, and reporting on threats across the security infrastructure.
    -   Changed: As part of the inclusive language initiative, allow list and deny list tags have been replaced with allow list and deny list respectively.
    -   Fixed: This release contains few functional fixes.
-   **Version 11.1.1 - November 2020**

    New: Enabled report\_view ACLs for sensitive tables and fields.

-   **Version 11.0.4 - October 2020**

    Changed: The app has been updated to incorporate modifications to the CrowdStrike Falcon Host portal authentication process.

-   **Version 11.0.1 - September 2020**
    -   New:
        -   Post Incident Review Assessments change provides the configurations to define the assessment trigger conditions to generate both mandatory and optional assessments for specific security incidents.
        -   File type observable security change provides stringent security measures to store the suspicious files and enables the files type observables for sandbox integration.
-   **Version 10.5.2 - August 2020**
    -   Changed: The number of related lists shown on Security Incident form have been reduced. Users will now see only the most commonly used related lists by default.
    -   Fixed: Performance issues with the "Related Configuration Items" and "Related Users" related lists have been addressed.
-   **Version 10.4.0 - June 2020**
    -   New: Created new form to collect customer configuration items and submit it to Licensing team
    -   Fixed: Security tag assignment to newly created security incidents
-   **Version 10.0.5 - April 2020**
    -   Fixed: Dispatch actions updated for compatibility with Security Incident Response UI
    -   Removed: ATF Test and related test configuration steps and variables
-   **Version 10.0.2 - March 2020**
    -   New: Capability Framework v2: The updated Integrations Capability framework provides a consistent architecture to support interoperability with third-party integrations. The changes include:
        -   Ability to specify conditions for triggering capabilities and implementations \(For example: based on Incident Category\)
        -   Easy configuration of capability and integration execution parameters like Batch input size, rate limits and time out period
        -   Creating your own Capability
        -   Easier troubleshooting of Capability executions
-   **Version 9.0.1 - November 2019**
    -   New: User Reported Phishing 2.0 provides an updated way to ingest phishing emails. It includes email aggregation, email header extraction, and improved configuration capabilities.
    -   Fixed: Bug fixes.
-   **Version 8.0.10 - June 2019**

    Refer to Security Incident Response release notes for product changes and updates in the Madrid release.


