---
title: View the Cybersecurity Controls module
description: View the Cybersecurity Controls module for a list of the Authority documents, Controls, Control Objectives, and CIS Indicator Templates mapped to specific CIS controls classified by domain, implementation group, and ISO controls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-common-functions/view-cybersecurity-controls.html
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Technology Controls Monitoring Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# View the Cybersecurity Controls module

View the Cybersecurity Controls module for a list of the Authority documents, Controls, Control Objectives, and CIS Indicator Templates mapped to specific CIS controls classified by domain, implementation group, and ISO controls.

## Before you begin

Role required: admin or sn\_compliance.reader

## About this task

**Note:** The Authority documents, Controls, and Control Objectives display the data related to source CIS, CIS v8, and CSA CCM v4. The module filters display the following data:

-   Authority Document - Source is CIS or CIS v8 or CSA CCM v4.
-   Citations - Source is CIS or CIS v8 or CSA CCM v4.
-   Control objectives - Source is CIS or CIS v8 or CSA CCM v4.
-   Indicator templates - Source is CIS or CIS v8.

Beginning with the Zurich release, Technology Controls Monitoring Accelerator provides pre-packaged CIS v8 controls and indicator templates.

## Procedure

1.  Navigate to **All** &gt; **Technology Controls Monitoring** &gt; **Cybersecurity Controls**.

    You can view the module as shown in the example.

    \[Omitted image "tech-controls-monitoring.png"\] Alt text: Technology Controls Monitoring module.

    **Note:** The CIS controls module is renamed from CIS controls @R to Cybersecurity Controls. The Indicator Templates module is renamed to CIS Indicator Templates.

2.  Select **Authority Documents**.

    The authority documents for source CIS, CIS v8, and CSA CCM v4 are listed as shown in the example.

    \[Omitted image "techctrlmoni-auth-doc-module-csa-ccm-v4-src-added.png"\] Alt text: Authority documents.

    The authority document ADCIS10002 is added for CIS v8. Similarly, AD0020002 is added for CSACCMv4.

    For the authority document record, the Content References related list is added for mapping.\[Omitted image "content-reference-rel-list-added-f-every-record-for-mapping.png"\] Alt text: Content References related list.

    The citations associated with the authority document are shown in the example.

    \[Omitted image "auth-doc-asso-178-citations-rel-list-2.png"\] Alt text: Authority document citation list

3.  Select **Citations**.

    The citations for source CIS, CIS v8, and CSA CCM v4 are listed as shown in the example.

    \[Omitted image "techctrlmoni-citations-module-csa-ccm-v4-src-added.png"\] Alt text: Citations.

    Every citation has a control objectives related list as shown in the example.\[Omitted image "every-citation-one-control-obj-rel-list-3.png"\] Alt text: Control objectives related list.

4.  Select **Control Objectives**.

    The control objectives for source CIS, CIS v8, and CSA CCM v4 are listed as shown in the example.

    \[Omitted image "techctrlmoni-control-obj-module-csa-ccm-v4-src-added.png"\] Alt text: Control objectives.

5.  Select **CIS Indicator Templates**.

    The CIS indicator templates for source CIS, CIS v8, and CSA CCM v4 are listed as shown in the example.

    \[Omitted image "techctrlmoni-cis-indi-temp-module-csa-ccm-v4-src-added.png"\] Alt text: CIS indicator templates.

    You can view the indicator templates for different sources. The following example shows the indicator templates for NIST CSF.\[Omitted image "contr-obj-source-is-nist-csf-72-mappings.png"\] Alt text: Indicator templates for NIST CSF.

    The Related source IDs column displays the source ID for the indicator template.\[Omitted image "indi-temp-1-1-mapped-to-prds3-idam1.png"\] Alt text: Related source IDs.

    The indicator template is mapped to the Content column as shown in the example.\[Omitted image "cis-v8-indi-template-mapped-to-content-column.png"\] Alt text: Indicator template is mapped to the Content column.

6.  Select **CIS Indicator Templates**.

    The CIS Indicator Templates are displayed in the instance.


**Parent Topic:**[Technology Controls Monitoring Accelerator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/tech-controls-monitoring-accel.md)

