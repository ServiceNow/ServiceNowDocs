---
title: View the Cybersecurity Controls module
description: View the Cybersecurity Controls module for a list of the Authority documents, Controls, Control Objectives, and CIS Indicator Templates mapped to specific CIS controls classified by domain, implementation group, and ISO controls.
locale: en-US
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

    ![Technology Controls Monitoring module.](../image/tech-controls-monitoring.png)

    **Note:** The CIS controls module is renamed from CIS controls @R to Cybersecurity Controls. The Indicator Templates module is renamed to CIS Indicator Templates.

2.  Select **Authority Documents**.

    The authority documents for source CIS, CIS v8, and CSA CCM v4 are listed as shown in the example.

    ![Authority documents.](../image/techctrlmoni-auth-doc-module-csa-ccm-v4-src-added.png)

    The authority document ADCIS10002 is added for CIS v8. Similarly, AD0020002 is added for CSACCMv4.

    For the authority document record, the Content References related list is added for mapping.![Content References related list.](../image/content-reference-rel-list-added-f-every-record-for-mapping.png)

    The citations associated with the authority document are shown in the example.

    ![Authority document citation list](../image/auth-doc-asso-178-citations-rel-list-2.png)

3.  Select **Citations**.

    The citations for source CIS, CIS v8, and CSA CCM v4 are listed as shown in the example.

    ![Citations.](../image/techctrlmoni-citations-module-csa-ccm-v4-src-added.png)

    Every citation has a control objectives related list as shown in the example.![Control objectives related list.](../image/every-citation-one-control-obj-rel-list-3.png)

4.  Select **Control Objectives**.

    The control objectives for source CIS, CIS v8, and CSA CCM v4 are listed as shown in the example.

    ![Control objectives.](../image/techctrlmoni-control-obj-module-csa-ccm-v4-src-added.png)

5.  Select **CIS Indicator Templates**.

    The CIS indicator templates for source CIS, CIS v8, and CSA CCM v4 are listed as shown in the example.

    ![CIS indicator templates.](../image/techctrlmoni-cis-indi-temp-module-csa-ccm-v4-src-added.png)

    You can view the indicator templates for different sources. The following example shows the indicator templates for NIST CSF.![Indicator templates for NIST CSF.](../image/contr-obj-source-is-nist-csf-72-mappings.png)

    The Related source IDs column displays the source ID for the indicator template.![Related source IDs.](../image/indi-temp-1-1-mapped-to-prds3-idam1.png)

    The indicator template is mapped to the Content column as shown in the example.![Indicator template is mapped to the Content column.](../image/cis-v8-indi-template-mapped-to-content-column.png)

6.  Select **CIS Indicator Templates**.

    The CIS Indicator Templates are displayed in the instance.


**Parent Topic:**[Technology Controls Monitoring Accelerator](../concept/tech-controls-monitoring-accel.md)

