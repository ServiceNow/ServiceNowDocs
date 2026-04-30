---
title: Use the Zscaler dashboard
description: Use the Zscaler dashboard to view Zscaler monitoring and remediation statuses in graph format.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Perform Zscaler remediation, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Use the Zscaler dashboard

Use the Zscaler dashboard to view Zscaler monitoring and remediation statuses in graph format.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Remediate Zscaler VPN** &gt; **Dashboard**.

    The Zscaler Remediation Dasbhoard appears.

    ![Zscaler Remediation dashboard](../image/zscaler-dashboard.png "Zscaler Dashboard")

    The dashboard displays graphs divided according to the following sections:

    |Section|Description|
    |-------|-----------|
    |Application Monitoring Status|Displays a bar graph of the number of Zscaler apps by date, and their statuses \(Up, Down, Unknown, Other\).|
    |Remediation Result|Displays a line graph of the number of Zscaler remediations, and their statuses \(Success, Failed, Not Required\).|
    |Zscaler Incidents|Displays a line graph of the number of Zscaler incidents created, and their statuses \(Opened, Closed\).|

2.  In the **Host CI** window on the upper right side of the page, select the CI whose data you want to view.

    The default value is All, indicating that the dashboard displays data from all of the CIs on the host.


**Parent Topic:**[Perform Zscaler remediation](../concept/zscaler-remediation-concept.md)

