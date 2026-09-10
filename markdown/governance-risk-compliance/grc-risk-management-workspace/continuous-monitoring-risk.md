---
title: Manage continuous monitoring for risks between Risk Management and Vulnerability Response
description: Continuous monitoring for risks is a feature integration between the GRC: Risk Management and the Security Operations Vulnerability Response products, which uses indicators to quickly identify high impact vulnerabilities based on business impact.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-risk-management-workspace/continuous-monitoring-risk.html
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Manage continuous monitoring for risks between Risk Management and Vulnerability Response

Continuous monitoring for risks is a feature integration between the GRC: Risk Management and the Security Operations Vulnerability Response products, which uses indicators to quickly identify high impact vulnerabilities based on business impact.

Risk administrators, managers, or users can monitor critical vulnerabilities by viewing the direct effect on risk posture. A new **Business Services** entity type and indicator templates automatically identify impacted services that are critical, represent a loss of availability, and are greater than two weeks old. These high-risk vulnerabilities can result in a breach and possible loss of intellectual property.

**Note:** The Entity type called 'Critical Business Services' is set to inactive by default and must be turned on.

## Data Visibility Between Risk Management and Vulnerability Response

When continuous monitoring is activated and configured, Risk Management \(IRM\) and Vulnerability Response \(VR\) systems exchange data in real-time. The following table clarifies where updates are visible in each system:

|Data Type|Visible in Risk Management \(IRM\)|Visible in Vulnerability Response \(VR\)|
|---------|----------------------------------|----------------------------------------|
|Vulnerability Data|Vulnerability issues from VR appear on IRM Risk dashboards and linked to relevant risk records. Vulnerability metrics \(age, severity, affected services\) update in near real-time on IRM indicators and dashboard widgets.|VR issues display as individual records in the standard VR interface with vulnerability scan data, severity, and remediation status.|
|Business Service Context|IRM dashboards display which Business Services are impacted by vulnerabilities, enabling risk managers to prioritize remediation based on business criticality.|VR issue records linked to Business Services show the associated risk context through related records and can display IRM risk statement associations.|
|Risk Issues|Risk issues created from high-impact vulnerabilities appear in IRM risk records and risk registers.|VR users can view linked Risk records to understand the broader risk context and organizational response to identified vulnerabilities.|
|Remediation Status|IRM dashboards show remediation progress tracked in VR, allowing risk managers to monitor mitigation activity.|VR issue records are the source of truth for remediation actions and timelines.|

## Continuous monitoring for risk workflow

1.  The system admin activates the Risk Management and Vulnerability Response plugins.

    **Note:** Both plugins must be active for data synchronization to occur. Verify plugin status in System Administration &gt; Plugins.

2.  The risk administrator creates risk statements and indicator templates that represent key vulnerabilities and their business impact.
3.  The risk manager associates the **Critical Business Services** entity type to the risk statements and indicator templates. This step links business criticality to vulnerability monitoring.

    **Note:** The Critical Business Services entity type is set to inactive by default and must be activated before it can be associated with risk statements. Activate in System Definition &gt; Entity Types.

4.  The Vulnerability Response application ingests vulnerability data from security scanners and related tools, automatically categorizing findings by affected business services.
5.  As vulnerabilities are identified and matched to the configured indicator templates, the system automatically creates or updates Risk Issues in IRM. These appear on IRM dashboards and in the Risk register within seconds of VR ingestion.
6.  Risk and security teams are notified of high-impact vulnerabilities through their respective dashboards. Risk managers can view vulnerability details in IRM context; Security Operations teams manage remediation in VR.
7.  Dashboards in both systems provide an up-to-date view for business stakeholders as risks are identified and remediated. IRM dashboards show business impact; VR dashboards show remediation progress.

## Activating and Configuring Continuous Monitoring

To enable continuous monitoring between Risk Management and Vulnerability Response:

1.  Navigate to **All** &gt; **System Administration** &gt; **Plugins** and verify that both **com.snc.grc.risk** \(Risk Management\) and the appropriate Vulnerability Response plugin are active.
2.  Navigate to **All** &gt; **Risk** &gt; **Setup** &gt; **Indicator Templates** and create indicator templates for the vulnerabilities you want to monitor.
3.  Associate the **Critical Business Services** entity type to your risk statements. Navigate to **All** &gt; **Risk** &gt; **Setup** &gt; **Risk Statements**, open a risk statement, and add the Critical Business Services entity type in the Entity Associations section.
4.  Configure vulnerability ingestion settings in Vulnerability Response to map vulnerability data to your business services.
5.  Test the integration by triggering a vulnerability scan or import. Verify that Risk Issues appear on your IRM dashboards within the expected time window.

**Parent Topic:**[Governance, Risk, and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/r_WhatIsGRC.md)

