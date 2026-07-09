---
title: Submit exceptions for Scan Engine findings
description: For Recommend level findings, developers can submit exception requests if they determine the finding should not be considered an issue to deter development.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/submitting-exception-reasons-scan-engine.html
release: australia
topic_type: task
last_updated: "2026-06-26"
reading_time_minutes: 1
breadcrumb: [Prevent technical debt with real-time code fixes, Prevent and resolve technical debt, Platform Health, Using Impact, Impact]
---

# Submit exceptions for Scan Engine findings

For Recommend level findings, developers can submit exception requests if they determine the finding should not be considered an issue to deter development.

## Before you begin

Generally, exceptions require approval from a system administrator. However, certain settings configured by a system administrator may determine if the exception is automatically approved or rejected. If the exception is approved, the finding is excluded from technical debt.

**Note:** The record under the Scanned Record field of the finding, sn\_se\_finding, record should be extending sys\_metadata table in order for the Scan Engine Exceptions UI action button to be available. For more information on configuring exception properties, refer to [Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/exception-reason-properties.md).

Role required: sn\_se.scan\_engine\_admin, sn\_impact\_common.Impact Developer, or sn\_impact\_common.Impact App Admin

## Procedure

1.  When a Recommend level finding is detected, select **View finding details** in the summary banner to open the Findings panel.

2.  In the Findings panel, select the **Recommend** tab to view Recommend level findings.

    \[Omitted image "real-time-findings-request-exception-new.png"\] Alt text: A Recommend level finding card in the Findings panel with the Create exception button.

3.  On the finding card, select **Create exception**.

4.  Enter the reason in the **Exception Reason** field for why an exception should be made for this finding.

5.  Select **Request Approval** to submit the exception for review by a system administrator.

    If approval requests are enabled, the exception state is set to Requested. If not, the state is Not Yet Requested.

6.  Select **OK** to save the exception request.

    The finding card updates to show a gray background with an **Exception requested** label. The **Create exception** button is replaced with a link to view the exception reason that was entered.

    **Note:** If the requester name or email notification does not display correctly in the exception record after submission, ensure your user account is properly synchronized between development and production environments. The Scan Engine exception workflow requires consistent user identification across instances.


