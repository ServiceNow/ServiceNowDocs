---
title: Business rules for TLM in EA Workspace
description: Several types of business rules are added with Technology Lifecycle Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-tpm-business-rules.html
release: zurich
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate the Technology Lifecycle Management \(TLM\) plugin, Configure Technology Lifecycle Management, Configure EA Workspace using the Setup page, Configure, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Business rules for TLM in EA Workspace

Several types of business rules are added with Technology Lifecycle Management.

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

The following business rules are added for Technology Lifecycle Management \(TLM\) in EA Workspace:

|Business rule|Table|Description|
|-------------|-----|-----------|
|Populate TPM Technology Lifecycle table|TPM Discovered Technology \[sn\_apm\_tpm\_discovered\_technology\]|Fetches the technology life-cycle data for your hardware and software elements in your enterprise.|
|Update Technology Lifecycle Info|TPM Discovered Technology \[sn\_apm\_tpm\_discovered\_technology\]|Updates technology life-cycle data for your hardware and software elements.|
|TPM Audit on TPM Lifecycle Exception|TPM Technology Lifecycle Exception \[sn\_apm\_tpm\_technology\_lifecycle\_exception\]|Fetches the life cycles that were approximated or couldn’t be found from Software Asset Management \(SAM\) Professional or Hardware Asset Management \(HAM\) Professional.|

**Parent Topic:**[Activate the Technology Lifecycle Management \(TLM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-install-tpm.md)

