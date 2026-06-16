---
title: Workflow Studio - Designer release notes
description: Version history for the Workflow Studio - Designer application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-flow-designer-designer.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Workflow Studio - Designer release notes

Version history for the Workflow Studio - Designer application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Flow Execution Analysis
        -   Map and Transform Data Step
    -   Fixed:
        -   PRB2009829 - Sub-flow 'Default value' for reference fields are not working as expected
        -   PRB1948914 - A flow variable was removed from the flow at some point, but it still appears in the flow executions
        -   PRB2025388 - Missing "Changes" operation in flow designer triggers, and
        -   PRB2017822
        -   PRB2015512
-   **Version 28.4.0 - June 2026 \(Zurich\)**

    New: Support for increasing the upper limit of dynamic inputs, which was previously capped at 40. You can use the system property "sn\_flow\_designer.max\_dynamic\_input\_items" to set this value up to recommended limit of 500.

-   **Version 29.2.2 - May 2026 \(Australia\)**
    -   New: Flow Execution Analysis enables users to summarize and analyze flow execution details to identify errors and suggest potential fixes.
    -   Fixed: Fixed critical defects such as PRB1976087 \(Nested Go Back To Flow Logic causing flow execution blank screen\) and PRB2005619 \(We are missing "Changes" operation in flow designer\).
-   **Version 28.3.1 - May 2026 \(Zurich\)**
    -   New: Support for triggers as a service.
    -   Fixed: Critical defect fixes including PRB1977516 \(Data is not being save or not passing to the flow execution for the Array.string data type\) &amp; PRB1970275 \(List Collector cannot be used as an input to a For Each flow logic block\).
-   **Version 29.1.0 - April 2026**
    -   New:
        -   Test conversational subflows and actions during design.
        -   Run a flow with high-security roles.
    -   Changed: Uplift UI for flow recommendations in dark and light theme.
    -   Fixed:
        -   PRB1957192: JIRA Spoke: Issue Type ID not loading even after selecting the Project Id
        -   PRB1982236: Flows not saving "Determines uniqueness" changes to Create and Update Record action.
-   **Version 29.0.5 - March 2026 \(Australia\)**

    Fixed: Critical defect fixes for the Australia release.

-   **Version 28.2.5 - March 2026 \(Zurich\)**
    -   Fixed:
        -   This release includes critical defect fixes. Some of them include:
        -   PRB1962475: Incorrect dates displayed in Flow Designer History tab after Zurich Patch 1 Hot Fix 1
        -   PRB1938489: Unable to expand the script when using a "Make a decision" action
        -   PRB1966361: Buttons in Find bar within inline script editor do not render
        -   PRB1926039: Values of tables such as sc\_task and incident are not rendered in UI for 'Look Up Record' / 'Create Record' step in action
        -   PRB1970275: List Collector cannot be used as an input to a For Each flow logic block
        -   PRB1928650: Getting error while publishing the Remote Process Sync Outbound subflow
        -   Other critical PRBs including PRB1949291, PRB1970167, PRB1965643, PRB1974070 and PRB1971893 were also fixed in this release
-   **Version 27.5.1 - March 2026**
    -   Fixed:
        -   Configure Connection in flow does not update in actions after upgrading to Yokohama
        -   Lines overlapping in flow components
        -   Assign Subflow Outputs action displays duplicated variable outputs
-   **Version 27.5.0 - January 2026 \(Yokohama\)**
    -   New: Made compatible with Yokohama Patch 11+
    -   Fixed: Fixed issue where clicking Cancel after editing an IF flow logic would delete the IF block and its children
    -   Removed: Removed requirement for the now.assist.creator role for flow recommendations
-   **Version 25.1.4 - March 2024**

    Fixed: Optimized the efficiency of opening, updating, creating flows within Workflow Studio. This change significantly reduces the time required for both initial access and subsequent interaction.

-   **Version 25.1.3 - February 2024**
    -   Flow Designer is a ServiceNow AI Platform feature that enables process owners to automate work. Build multi-step flows from reusable components without having to code.
    -   Flow Designer is the default ServiceNow AI Platform process automation builder used to create flows. Flow Designer replaces the legacy Workflow graphical editor.

**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

