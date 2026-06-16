---
title: ReleaseOps release notes
description: Version history for the ReleaseOps application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-releaseops.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# ReleaseOps release notes

Version history for the ReleaseOps application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.3.1 - June 2026**
    -   Defect fixes.
        -   Deployment Request Lifecycle
            -   Fixed: Failed/Cancelled Deployment Requests can now be recovered — Previously, there was no way to recover a DR that failed or was cancelled for any reason. \(PRB2016691\)- Fixed: "Ready to Assess" UI action now appears correctly on valid DRs via AEMC interface \(PRB1983286\)- Fixed: UI actions on Deployment Requests now work as expected \(PRB1993143\)- Fixed: Promoting an update set already associated to a DR no longer creates an empty draft DR \(PRB2005326\)
        -   Update Set Operations
            -   Fixed: Update sets no longer queried locally on the controller instance — Previously, incorrect local queries could cause both the Release and DR to fail. \(PRB1924757\)- Fixed: Update set state no longer committed unexpectedly before preview/commit — Race condition that caused Release and DR failures has been resolved. \(PRB1924767\)- Fixed: Integrate DR subflow now warns when an update set is already committed — Prevents silent failures when processing unexpectedly committed update sets. \(PRB2006340\)- Fixed: Invalid data mapping in Integration DR subflow for deployment instance URL \(PRB2013552\)
        -   Release Management
            -   Fixed: On-demand release freeze date is no longer editable — The missing freeze date warning no longer displays incorrectly. \(PRB2006663\)- Fixed: Release Date is now correctly assigned when a Change is associated — Previously the field was made readonly without being populated. \(PRB1956031\)
        -   Setup &amp; Configuration
            -   Fixed: ReleaseOps Guided Setup can now be restarted — Previously, re-running the Guided Setup was not possible. \(PRB1981557\)- Fixed: Read-only directive now applies correctly for Australia upgrades with ReleaseOps ZS2 v1.2.3 \(PRB1997746\)
        -   Work Notes &amp; Messaging
            -   Fixed: Misleading work notes in Deployment Request during ATF test execution — Work notes now accurately reflect test run status. \(PRB1979850\)
-   **Version 2.1.1 - June 2026**
    -   New: Synchronize deployment requests on Prod with Dev via MIM.
    -   Fixed:
        -   Promoting an update set already associated to a DR no longer creates an empty draft DR \(PRB2005326\)
        -   The deferred flag on a DR is now correctly cleared when blanking the release field \(PRB2016009\)
        -   Invalid data mapping in Integration DR subflow for deployment instance URL \(PRB2013552\)
        -   Integrate DR subflow now warns when an update set is already committed \(PRB2006340\)
        -   On-demand release freeze date is no longer editable; missing freeze date warning no longer displays incorrectly \(PRB2006663\)
        -   Release Notes version no longer resets to 0 after deleting and regenerating \(PRB1989009\)
        -   OnDemandValidator getRowCount now correctly calls the function instead of referencing it \(PRB2007218\)
        -   ReleaseOps Guided Setup now creates the remote instance between prod and dev for the Deployment Analyzer \(PRB2007225\)
        -   Updated stale sys\_dictionary XML reference \(PRB2020934\)
        -   Worknotes links to update set no longer return "record not found" \(PRB1996809\)
        -   ReleaseOps logging now includes relevant information in syslog table \(PRB1999832\)
-   **Version 2.0.1 - April 2026**
    -   New:
        -   Leverage Automated Test Framework \(ATF\) code coverage and code difference to view what percentage of code is covered by ATF test suites and what code is new in deployment requests.
        -   Add manual, flexible activities to your ReleaseOps deployments using runbook tasks, which pause playbook progression until all associated tasks are completed.
        -   With Now Assist for Creator, you can generate update set descriptions and release notes for ReleaseOps releases.
    -   Changed: Cancel deployment requests stuck in the "Assessing" state with the "Cancel" button. You can also move deployment requests in the "Cancelled" or "Failed" state back to the "Draft" state with the "Move back to draft" option.
    -   Fixed: Improvements to ReleaseOps guided setup.
-   **Version 1.2.3 - February 2026 \(Zurich\)**

    Use new ReleaseOps guided setup to help make the initial configuration process easier.

-   **Version 1.2.1 - December 2025 \(Zurich\)**

    New: Use new ReleaseOps guided setup to help make the initial configuration process easier.

-   **Version 1.0.3 - August 2025**
    -   ReleaseOps: Deploy Custom Apps and Update Sets Reliably and Quickly
    -   ReleaseOps helps overcome the complexity of deploying software updates safely and at scale. It's built to automate manual steps while still maintaining control. It will assist in policy and quality control compliance, improve visibility, and promote confidence that you can deploy code changes consistently.
    -   At its core, ReleaseOps introduces structured deployment workflows that guide your ServiceNow application updates from development to production. These workflows are powered by Releases and Deployment Requests, which serve as the foundation for managing Update Set driven deployments across ServiceNow instances.
    -   Pipelines automate the movement of code between instances and allow ReleaseOps to enforce organizational standards through customizable integrations that may include:
        -   Instance Scan
        -   Automated Test Framework \(ATF\)
        -   Change Management
    -   To ensure visibility and deployment success, ReleaseOps generates Deployment Tasks when issues are detected, assigning them to the right developers or stakeholders for resolution before the deployment proceeds.Teams benefit from the flexibility to follow a controlled release cadence while retaining the agility to fast-track hotfixes or urgent security patches on demand.
    -   Throughout the process, ReleaseOps delivers full transparency with real-time status updates, progress tracking, and detailed notes, keeping developers, release managers, and stakeholders aligned.

**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

