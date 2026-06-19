---
title: Request an exception using GRC: Policy and Compliance Management in the IT Remediation Workspace
description: Request a policy exception for the host vulnerable item \(VIT\), application vulnerable item \(AVIT\), container vulnerable item \(CVIT\) or remediation task \(VUL, AVUL, CVUL, or CRG\) from the IT Remediation Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/it-remediation-workspace/vr-ws-request-exception-grc.html
release: zurich
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Request an exception using GRC: Policy and Compliance Management in the IT Remediation Workspace

Request a policy exception for the host vulnerable item \(VIT\), application vulnerable item \(AVIT\), container vulnerable item \(CVIT\) or remediation task \(VUL, AVUL, CVUL, or CRG\) from the IT Remediation Workspace.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## About this task

**Note:** Starting with v19.0 of Vulnerability Response, the following terms have been renamed:

|Terminology prior to v19.0|Terminology v19.0 onwards|
|--------------------------|-------------------------|
|Test Result Groups|Remediation Tasks|
|Configuration Issues|Configuration Test Results|
|Policy|Test group|

## Procedure

1.  Navigate to **Workspaces** &gt; **IT Remediation Workspace**.

2.  In the application navigator, select the List icon \(\[Omitted image "icon-polaris-list-workspace.png"\] Alt text: List icon.\).

3.  On the List page, under Host vulnerable items, Application vulnerable items, Container vulnerable items, or Remediation tasks \(VUL, AVUL, CVUL, or CRG\), select the record that you want to request an exception for.

    The record that you select must be in the Open, Under investigation, or Awaiting implementation state.

4.  Select the **Request Exception** button.

5.  On the form, fill in the fields.

    For more information on the form fields, see [Request exception form fields for policy exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/it-remediation-workspace/itr-ws-request-exception-form-grc.md).

6.  Select **Request Exception**.

7.  On the Take Questionnaire modal, answer the questions to provide additional information about your request and select **Submit**.

    **Note:** The Take Questionnaire modal appears only when the questionnaire details are added to the respective integration registry.

    A message appears that your request is successfully submitted for approval.

    For more information on the Policy Exception Integration and the hand-off between the remediation owner and the compliance manager, see Policy and Compliance Management optional setup.


