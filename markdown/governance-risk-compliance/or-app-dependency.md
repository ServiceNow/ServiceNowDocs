---
title: Key dependencies for Operational Resilience
description: Before you install the Operational Resilience application, you must install the required GRC applications in your instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Operational Resilience, Governance, Risk, and Compliance]
---

# Key dependencies for Operational Resilience

Before you install the Operational Resilience application, you must install the required GRC applications in your instance.

The following example shows the Operational Resilience hierarchy, required GRC applications, and optional GRC applications that you can add to the reporting dashboard.

![Operational Resilience application hierarchy.](../image/or-application-dependency.png "Operational Resilience application hierarchy")

## Required and optional plugins for Operational Resilience

The Operational Resilience application \(com.sn\_grc\_oper\_res\) is available from the ServiceNow Store. The following plugins are required \(hard dependencies\) for Operational Resilience.

1.  GRC: Common Workspace Elements \(com.sn\_grc\_workspace\)
2.  GRC: Profiles \(com.sn\_grc\)
3.  GRC: Core Case Management \(com.sn\_grc\_case\_mgmt\)
4.  Data Relationships Framework \(com.sn\_app\_grc\_relationship\_config\)
5.  Data registry \(com.sn\_app\_grc\_data\_registry\)
6.  GRC: Risk Shared Common Components \(com.irm-shared-common-components\)
7.  Document Templates \(com.snc.app-document-templates\)

The following plugins are optional \(soft dependencies\) for Operational Resilience.

1.  GRC: Policy and Compliance Management \(com.sn\_compliance\)
2.  Advanced Risk \(com.sn\_risk\_advanced\)
3.  GRC: Risk Management \(com.sn\_risk\)
4.  GRC: Business Continuity Planning \(com.snc.bcm.app\_bcm\_planning\)
5.  GRC: Business Impact Analysis \(com.snc.bcm.app\_bcm\_bia\)
6.  GRC: Crisis Management \(com.snc.bcm.app\_bcm\_exercise\)
7.  Vulnerability Response \(com.snc.vulnerability\)

Depending on the applications installed in your instance, you can view the reports on the Operational Resilience reporting dashboard.

