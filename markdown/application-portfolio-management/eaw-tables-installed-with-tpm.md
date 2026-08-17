---
title: Tables installed with TLM in the EA Workspace
description: Several types of tables are installed with Technology Lifecycle Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-tables-installed-with-tpm.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate the Technology Lifecycle Management \(TLM\) plugin, Configure Technology Lifecycle Management, Configure EA Workspace using the Setup page, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Tables installed with TLM in the EA Workspace

Several types of tables are installed with Technology Lifecycle Management.

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

The following tables are installed with the Technology Lifecycle Management \(TLM\) plugin:

<table id="table_pzc_h55_yzb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TPM Discovered Technology \[sn\_apm\_tpm\_discovered\_technology\]

</td><td>

Stores hardware and software elements in your enterprise.**Note:** To view the software life-cycle data, you must activate the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin.

</td></tr><tr><td>

TPM Discovered Technology Run Log \[sn\_apm\_tpm\_discovered\_technology\_run\_log\]

</td><td>

Stores when Technology Lifecycle Management \(TLM\) refreshed its contents against Software Asset Management \(SAM\) Professional and Hardware Asset Management \(HAM\) Professional.

</td></tr><tr><td>

TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\]

</td><td>

Stores the technology life cycles associated with the discovered technologies.

</td></tr><tr><td>

TPM Technology Lifecycle Exception \[sn\_apm\_tpm\_technology\_lifecycle\_exception\]

</td><td>

Stores the life cycles that were approximated or couldn’t be found from Software Asset Management \(SAM\) Professional or Hardware Asset Management \(HAM\) Professional.

</td></tr><tr><td>

TPM Technology Risk \[sn\_apm\_tpm\_technology\_risk\]

</td><td>

Stores the TLM technology risk information.

</td></tr></tbody>
</table>**Parent Topic:**[Activate the Technology Lifecycle Management \(TLM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-install-tpm.md)

