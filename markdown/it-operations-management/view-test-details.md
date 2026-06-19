---
title: View test details
description: View the results of an individual synthetic test run by a monitor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/view-test-details.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Identifying system issues with synthetic monitoring, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# View test details

View the results of an individual synthetic test run by a monitor.

## Before you begin

Role required: sn\_sow\_synthetics.synthetics\_viewer, sn\_sow\_synthetics.synthetics\_editor, sn\_sow\_synthetics.synthetics\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** and select the synthetic monitoring icon \(\[Omitted image "sys-mon-icon.png"\] Alt text: Synthetic monitoring\).

2.  Select a monitor from the list of all monitors.

3.  Select a test from the list of tests.

    The modal displays information about the test including a response body. In this example, it shows that the request was sent to a bad gateway.

    **Note:** If your monitor uses OAuth and a test fails with a 4xx error, it may be because your refresh token expired. Re-authenticate by visiting the OAuth credential page and clicking the credential link.

    \[Omitted image "sys-mon-failed\_monitor.png"\] Alt text: A modal displays information about the test including a response body that states that the request was to a bad gateway.


