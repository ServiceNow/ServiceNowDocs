---
title: Financial Services Control accelerator
description: The Financial Services Control Accelerator gives customers an operational head-start when adopting the Financial Services Control. When the accelerator is downloaded and activated in the GRC applications, pre-configured authority documents, citations, and control objectives.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# Financial Services Control accelerator

The Financial Services Control Accelerator gives customers an operational head-start when adopting the Financial Services Control. When the accelerator is downloaded and activated in the GRC applications, pre-configured authority documents, citations, and control objectives.

## Content for Federal Financial Institutions Examination Council \(FFIEC\)

Beginning with the Zurich release, Financial Services Control Accelerator supports the FFIEC content such as Authority Document, Citations, and Control Objectives for:

-   FFIEC Architecture, Infrastructure, and Operations \(AIO\) IT Examination Handbook
-   FFIEC Business Continuity Management \(BCM\) IT Examination Handbook
-   FFIEC Development, Acquisition, and Maintenance \(DAM\) IT Examination Handbook.

## Content for New York State Department Of Financial Services \(NYDFS\)

Beginning with the Zurich release, Financial Services Control Accelerator supports the New York State Department Of Financial Services \(NYDFS\) Second Amendment to 23 NYCRR 500 content such as Authority Document, Citations, and Control Objectives.

This accelerator also includes mapping of FFIEC and NYDFS control objectives and citations to CRI citations and control objectives. For more information, see [Cyber Risk Institute accelerator](../../grc-cri-accelerator/concept/cyber-risk-inst-accelerator.md).

Prior to running the Financial Services Control Accelerator application, you must download and activate the following GRC applications:

-   GRC: Policy and Compliance Management
-   GRC: Profiles

**Note:** Follow the instructions for [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

## Financial Services Control Accelerator controls

After you have accessed the Financial Services Control Accelerator, you can access the data for different regulators using these modules.

<table id="table_uqc_glt_zfc"><thead><tr><th>

Application/Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authority Documents

</td><td>

The Authority Documents module provides a list of authority documents, including the FFIEC and NYDFS authority documents. The authority documents include references to citations and control objectives.

 The authority documents are stored in the Authority Document table \[sn\_compliance\_authority\_document\].

</td></tr><tr><td>

Citations

</td><td>

The Citations module provides a list of citations contained in the FFIEC and NYDFS authority document. Each citation can include Content references.

 The citations are stored in the Citation table \[sn\_compliance\_citation\].

</td></tr><tr><td>

Control Objectives

</td><td>

The Control Objectives module provides a list of control objectives associated with the citations in the FFIEC and NYDFS authority document. Each control objective can include one or more content references.

 The control objectives are stored in the Control Objective table \[sn\_compliance\_policy\_statement\].

</td></tr></tbody>
</table>**Parent Topic:**[Governance, Risk, and Compliance use case accelerators](../../grc-common/reference/grc-use-case-accelerators.md)

