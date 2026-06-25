---
title: Discovery Admin Workspace Error Details
description: The Error Details page displays the root cause and remediation steps for a specific Discovery error, along with the list of individual error instances associated with that error.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/daw-error-details.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 2
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace Diagnostics, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace Error Details

The Error Details page displays the root cause and remediation steps for a specific Discovery error, along with the list of individual error instances associated with that error.

To access Discovery error details in Discovery Admin Workspace, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Diagnostics** &gt; **Errors**.

**Note:** The capabilities described here are available in Discovery Admin Workspace v1.17.0. This page is only accessible when the **sn\_disco\_workspace.enable\_error\_framework** system property is enabled. Specific version requirements are noted for individual features where applicable.

After selecting an error card, the header displays key information including the error title, severity, refined code, and category.

\[Omitted image "daw-error-details-overview.png"\] Alt text: Error Details page in Discovery Admin Workspace

## Key features

-   **Overview**

    The Overview tab is the starting point for resolving an error. The **Root cause** section explains what triggered the error, and the **Remediation instructions** section provides the steps to resolve it.

-   **Errors**

    The Errors tab displays the list of individual error instances associated with the refined code. Each instance represents a specific device or schedule where the error occurred.

    Use the filter, **Sort by**, and **Group by** options to apply advanced filtering to the table. The table includes Fixed filters, which are pre-applied and can't be removed or modified. Select **Export** to download the list of error instances in Excel, CSV, JSON, or PDF formats.

    The Errors table includes the following information:

    |Column|Description|
    |------|-----------|
    |IP address / Error key|The IP address or unique key that identifies the affected device or target. Select the hyperlink to view additional details and perform actions on this error in a side panel.|
    |State|The current state of the error instance. Possible values are Open, Closed, and Ignored.|
    |Error re-opened|The number of times this error instance has re-opened after being closed.|
    |Impacted schedule|The Discovery schedule associated with the error instance. Select the schedule name to navigate to its [schedule details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-schedules.md) page.|
    |Last occurrence|The date and time when the error was most recently detected.|
    |Consecutive \#|The number of consecutive Discovery runs in which this error has occurred.|
    |Refined on|The date and time when the error classification was last refined.|

    Selecting an IP address / Error key hyperlink opens a side panel, as shown in the following image.

    \[Omitted image "daw-error-details-pnl.png"\] Alt text: Error details side panel

    The **Context** section of the panel displays metadata collected during the Discovery run for the affected device, such as probe results, lookup parameters, and CMDB match data. Select the **Actions** drop-down to perform an action on the error instance. The fields and actions in this section vary by error type.

    You can also select the Now Assist \(\[Omitted image "now-assist-icon.png"\]\) icon to open the panel chat and ask Now Assist to analyze the error code. Now Assist generates a summary and remediation steps based on the error context.

    **Note:**

    -   Now Assist for Error Framework \(com.sn\_ef\_gen\_ai\) is available in Australia Patch 3 and requires the Now Assist for Platform \(sn\_genai\_platform\) plugin.
    -   The Error Analysis and Remediation Workflow and Error Analysis and Remediation Agent are enabled by default with the Now Assist for Error Framework plugin.
    -   To interact with an agent, you must first [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

