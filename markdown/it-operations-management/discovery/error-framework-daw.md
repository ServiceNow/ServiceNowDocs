---
title: Error Framework in Discovery Admin Workspace
description: Discovery Admin Workspace uses the Error Framework to surface actionable Discovery errors. You can review errors, understand their causes, and take steps to resolve them directly from the Diagnostics page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/error-framework-daw.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 4
breadcrumb: [Discovery Admin Workspace Diagnostics, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Error Framework in Discovery Admin Workspace

Discovery Admin Workspace uses the Error Framework to surface actionable Discovery errors. You can review errors, understand their causes, and take steps to resolve them directly from the Diagnostics page.

## Benefits

The Error Framework in Discovery Admin Workspace provides the following benefits:

-   A centralized view of Discovery errors grouped by category and severity.
-   Contextual details for each error, including affected devices and Discovery schedule.
-   Solution-focused error records that guide you to the root cause and remediation steps first.
-   Actions you can trigger directly from an error record to help resolve the issue.
-   AI-powered insights that prioritize your errors and surface high-impact items and quick wins.
-   Aggregated error statistics to identify patterns across discovery runs.
-   A domain filter to focus on errors relevant to your domain.

## How it works

When Discovery runs, it logs actionable errors to the Error Framework. Each error includes a unique error code, context about where and why it occurred, and one or more resolution actions. The Diagnostics page in Discovery Admin Workspace displays these errors on the Errors tab.

After Discovery completes, the framework refines error classifications using enrichment data from the discovery run. For example, if a device initially logged an SNMP connection error but was successfully discovered through another protocol, reﬁnement updates the error to an informational state. Errors downgraded to informational severity are filtered from the default view so you can focus on errors that need attention.

Error Framework is enabled by default. Administrators can disable it by setting the **sn\_disco\_workspace.enable\_error\_framework** system property to `false`. When Error Framework is inactive, Discovery reverts to the legacy Diagnostics experience.

**Note:** The Error Framework only logs actionable errors that have documented resolution steps. It doesn't replace system-level debug logging.

-   **Error Classification**

    The framework classifies Discovery errors using two levels of rules:

    -   **Base rules**: ServiceNow-provided rules that map known Discovery log patterns to standardized error codes in the SN-DISC format.
    -   **Refinement rules**: Rules that further classify errors based on additional context gathered after the discovery run completes. Refinement can change an error's code or downgrade its severity. Default refinement rules are provided for known Discovery scenarios.
    The framework processes errors through base classification first, then applies refinement. As part of this process, each error record is enriched with data from related Discovery sources, including CMDB records, credential affinities, IP address details, and Discovery schedule configuration. This context is available on the error record and reduces the need to navigate between multiple tables during investigation. The refined error code is what appears on the Errors tab of the [Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md) page. Errors downgraded to informational severity are filtered from the default view, so you can focus on errors that need attention.

-   **Error severity levels**

    Each error is assigned a severity level based on its impact on discovery. The following table describes the severity levels.

    |Severity|Description|
    |--------|-----------|
    |Critical|The error prevents discovery from completing for the affected device or schedule.|
    |High|The error significantly affects discovery results but doesn't stop the run.|
    |Medium|The error may affect some discovery results. Review and resolve when possible.|
    |Low|The error has minimal impact. Address when convenient.|
    |Info|Informational only. No action is required.|

-   **Error states**

    Errors move through the following states during their life cycle:

    -   **Open**: The error is active and hasn't been resolved.
    -   **Closed**: The error has been resolved.
    -   **Ignored**: The error has been acknowledged and suppressed from active views.
    **Note:** Closed and ignored error records are retained for seven days. Error instance records are retained for 90 days.

-   **Error actions**

    Each error code can have one or more actions associated with it. Actions are available from the error record and can include the following types:

    -   Changing the state of an error instance to Open, Ignored, or Resolved.
    -   Adding the affected IP address to the global exclusion list.
    -   Retrying discovery for the affected device or schedule.
    -   Displaying a message with remediation steps to resolve the error.
    **Note:** Available actions vary by error type.

    For more information, see [Discovery Admin Workspace Error Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-error-details.md).

-   **AI insights**

    The [Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md) page includes an AI Insights panel powered by Now Assist for Error Framework. The panel analyzes your current Discovery errors and generates a prioritized summary to help you focus on the most important issues first. Insights are scoped to your active domain and update automatically when you change filters on the Errors tab.

    The panel surfaces the following:

    -   Highest-impact errors that are affecting the most devices or schedules.
    -   Quick wins, which are errors that can be resolved with minimal effort.
    You can also use Now Assist agents to analyze a specific error code and receive a summary with remediation steps on demand.

    **Note:**

    -   Now Assist for Error Framework \(com.sn\_ef\_gen\_ai\) is available in Australia Patch 3 and requires the Now Assist for Platform \(sn\_genai\_platform\) plugin. If the plugin is not enabled, the panel displays a prompt to enable it.
    -   The Error Analysis and Remediation Workflow and Error Analysis and Remediation Agent are enabled by default with the Now Assist for Error Framework plugin.
    -   To interact with an agent, you must first [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

## Roles

The discovery\_admin role is required to access Discovery Admin Workspace and interact with errors.

## Requirements

The following are required to use Error Framework features in Discovery Admin Workspace:

-   Australia Patch 3.
-   Discovery Admin Workspace v1.17.0.

