---
title: Compensating controls overview
description: A compensating control is an alternative safeguard that reduces the risk of a finding when the finding's standard remediation cannot be applied. Use compensating controls when the underlying vulnerability still exists but its risk is being managed through a different mitigation, instead of requesting an exception that defers remediation entirely.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-compensating-controls-overview.html
release: brazil
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 3
keywords: [compensating control, mitigation, exception management]
breadcrumb: [Questionnaire support in Exception Management via Smart Assessment, Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Compensating controls overview

A compensating control is an alternative safeguard that reduces the risk of a finding when the finding's standard remediation cannot be applied. Use compensating controls when the underlying vulnerability still exists but its risk is being managed through a different mitigation, instead of requesting an exception that defers remediation entirely.

## What is a compensating control

A compensating control is a mitigation that reduces the risk associated with a finding without removing the finding itself. Examples include:

-   Network segmentation that limits exposure of a vulnerable host to untrusted networks.
-   Application-layer access controls that restrict who can reach a vulnerable function.
-   Monitoring and alerting rules that detect attempted exploitation of the vulnerable component.
-   Endpoint detection-and-response policies that block known exploit signatures.

The finding remains in the system and continues to appear in vulnerability reports. The compensating control changes the residual risk, not the underlying vulnerability.

## When to use a compensating control instead of an exception

Choose a compensating control when all of the following are true:

-   The standard remediation \(patch, configuration change, code fix\) cannot be applied in the near term.
-   Another mitigation exists that demonstrably reduces the risk to an acceptable level.
-   You can produce evidence that the mitigation is implemented and effective.

Choose an exception \([Defer a Remediation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-defer-rem-task.md)\) instead when there is no available mitigation and you are accepting the residual risk for a defined period.

Choose a false positive \([Request a false positive for a vulnerable item or remediate task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-falsepst-reqst.md)\) instead when the finding is incorrect — the scanner reported a vulnerability that does not actually exist on the asset.

## Evidence requirements for a compensating control

The compensating-control approval flow requires evidence that the mitigation is in place and working. Acceptable evidence includes:

-   Configuration snapshots from the compensating-control system \(for example, firewall rule export, WAF policy ID\).
-   Test results showing that the mitigation blocks the relevant attack path.
-   Monitoring rule definitions and the most recent triggering alerts.
-   Architecture diagrams that show how the compensating control isolates the vulnerable asset.

Attach the evidence to the request when you submit it. Approvers reject requests that lack verifiable evidence.

## How compensating-control approvals work

Compensating-control requests follow the standard exception-management approval flow described in [Exception Management Overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-exception-management-overview.md):

1.  The remediation owner submits the request with the compensating-control description and evidence.
2.  If the matching approval rule has a questionnaire configured, the owner completes the questionnaire before submission.
3.  The request routes to the configured approver level or levels. Multi-level approval rules send the request through each level sequentially.
4.  On approval, the finding transitions to **Deferred** with reason **Mitigating control in place**; the compensating-control evidence is preserved on the change approval record. On rejection or expiry, the finding reverts to its previous state.

The form fields used for compensating-control questionnaires are documented in [Questionnaire Configuration form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-compensating-controls-approval-rule.md).

## Periodic review of approved compensating controls

A compensating control is not a permanent substitute for remediation. The approval includes an expiry date; before expiry, the requester must either:

-   Complete the standard remediation and close the finding.
-   Renew the compensating-control approval with updated evidence showing the mitigation is still in place and effective.

If neither action is taken before expiry, the finding reverts to **Open** and reappears in the assigned owner's queue.

