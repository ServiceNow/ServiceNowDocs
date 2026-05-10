---
title: Enable Claim workspace, Fraud score, and Claim summary pages
description: Enable Fraud score and Claim summary pages on the claim case so that a claims manager, adjuster, or processor can view them.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Personal Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Enable Claim workspace, Fraud score, and Claim summary pages

Enable Fraud score and Claim summary pages on the claim case so that a claims manager, adjuster, or processor can view them.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Enable the CSM default record page under CSM/FSM Configurable Workspace.

    For more information, see [CSM Configurable Workspace record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-workspace-record-pages.md).

3.  From the CSM default record page, set the page order.

4.  Set the variant conditions on the following record pages.

<table id="choicetable_zrz_43y_dyb"><thead><tr><th align="left" id="d53774e91">

Claims page variant

</th><th align="left" id="d53774e94">

Navigation to page records

</th></tr></thead><tbody><tr><td id="d53774e100">

**Record page for the adjuster task**

</td><td>

To access the record page for the adjuster task, navigate to: **CSM Configurable Workspace** &gt; **Record** &gt; **Claim Adjuster Record Page**.The record page for the adjuster task is a variant of CSM default record page. For more information, see [CSM Configurable Workspace record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-workspace-record-pages.md).

</td></tr><tr><td id="d53774e127">

**Claim workspace page**

</td><td>

To access the Claim workspace page for updates, navigate to page collection: **CSM default record post-Details** &gt; **Claim workspace** &gt; **Claim Workspace Default**.

</td></tr><tr><td id="d53774e148">

**Fraud score page**

</td><td>

To access the Fraud score page for updates, navigate to page collection: **CSM default record post-Details** &gt; **Fraud score** &gt; **Default**.

</td></tr><tr><td id="d53774e169">

**Claim Summary page**

</td><td>

To access the Claim summary page for updates:Navigate to page collection: **CSM default record pre-Details** &gt; **Claim summary** &gt; **Claim Summary Default**.

Or navigate to page collection **CSM default record post-Details** &gt; **Claim Summary** &gt; **Claim Summary On Adjuster**.

</td></tr></tbody>
</table>
