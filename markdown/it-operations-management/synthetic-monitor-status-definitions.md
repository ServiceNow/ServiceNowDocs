---
title: Synthetic monitor status definitions
description: Learn what each synthetic monitor test status means, so you can distinguish a genuine endpoint failure from a test that never ran.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/synthetic-monitor-status-definitions.html
release: australia
topic_type: reference
last_updated: "2026-07-21"
reading_time_minutes: 2
keywords: [status, monitor status, Unknown, Failed, Passed]
breadcrumb: [Reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Synthetic monitor status definitions

Learn what each synthetic monitor test status means, so you can distinguish a genuine endpoint failure from a test that never ran.

## Overview of Synthetic monitor status

Each test run by a synthetic monitor reports one of the following statuses. Use these definitions to distinguish a monitor that detected a genuine problem with the monitored endpoint from a monitor whose test could not run at all.

## Status definitions

|Status|Definition|
|------|----------|
|**Passed**|The test executed and the response met all configured assertion criteria.|
|**Failed**|The test executed but the response did not meet one or more configured assertion criteria. The monitor successfully reached the endpoint and received a response, but that response failed evaluation. Examples include an unexpected status code, a response time over the configured threshold, or missing expected content.|
|**Unknown**|The test could not run, so no result is available for evaluation. An Unknown status means the monitor could not attempt the check at all, rather than reaching the endpoint and receiving an unsuccessful response. Unknown is expected in this case, and does not by itself indicate a problem with the monitored endpoint.|

**Important:** A Failed status indicates the monitored endpoint returned an unexpected result. An Unknown status indicates the monitor was unable to run the test at all. Treat these differently when triaging alerts: an Unknown status should prompt you to investigate the monitor's execution environment, such as its location or MID Server, rather than the health of the monitored endpoint itself.

## Common causes of an Unknown status

An Unknown status can occur whenever the test cannot run to completion. Common causes include the following.

<table id="table_unknown_causes"><thead><tr><th>

Cause

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MID Server removed from the synthetic monitoring location

</td><td>

If the MID Server assigned to a monitor's location is removed from that location, the test cannot run and the status becomes Unknown. This is expected behavior.

</td></tr><tr><td>

MID Server is down or not validated

</td><td>

If the MID Server assigned to a monitor's location exists but is down or has not been validated, the test cannot run and the status should become Unknown, since the check never actually executed.**Note:** In earlier releases, this scenario could incorrectly report a Failed status and generate an alert, making it appear that the monitored endpoint was down. If you see a Failed status for a monitor and suspect its MID Server is down or unvalidated, check the MID Server's status before troubleshooting the monitored endpoint.

</td></tr></tbody>
</table>## Related topics

[Upgrade issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/troubleshoot-sm-mid.md)

[Identifying system issues with synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/identifying-system-issues.md)

**Parent Topic:**[Synthetic monitoring reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/synthetic-monitoring-reference.md)

