---
title: Check Zscaler remediation
description: Verify that Zscaler remediation stops and starts the Zscaler app after the remediation monitoring check fails.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/zscaler-check-remediation.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Perform Zscaler remediation, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Check Zscaler remediation

Verify that Zscaler remediation stops and starts the Zscaler app after the remediation monitoring check fails.

## Before you begin

Verify that the Zscaler monitoring check returns an **Application Status** value of **Down**, indicating that the Zscaler app isn’t working properly.

Role required: agent\_client\_collector\_admin

## Procedure

-   Navigate to **All** &gt; **Remediate Zscaler VPN** &gt; **Remediation Result**.

    The **Application Remediation Status** page appears.

    \[Omitted image "app-remediation-status.png"\] Alt text: Application remediation status page

    When remediation successfully shuts down and restarts Zscaler, the Remediation Result column has a value of **Success**. The Task Associated column displays a link to the incident created on remediation. When remediation is successful, the incident closes automatically.


**Parent Topic:**[Perform Zscaler remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/zscaler-remediation-concept.md)

