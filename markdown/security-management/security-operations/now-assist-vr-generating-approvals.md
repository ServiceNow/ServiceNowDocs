---
title: Approval recommendations using generative AI
description: Learn more about the how the Approval Recommendation generative AI skill arrives at its approval recommendations and the sources it uses to generate them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/now-assist-vr-generating-approvals.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 4
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Approval recommendations using generative AI

Learn more about the how the Approval Recommendation generative AI skill arrives at its approval recommendations and the sources it uses to generate them.

## Overview for the Approval Recommendation skill

The Approval Recommendation generative AI skill provides exception and false positive approvers in Vulnerability Response with recommendations to help them make faster, more consistent decisions while reducing manual analysis effort.

A finding \(vulnerable item\) is a vulnerability detected on an asset. Some findings don't require immediate remediation, for example, false positives or cases where a fix isn't yet available. From these types of findings and remediation tasks, users submit exception requests and ask for approval to defer remediation or indicate that a finding is a false positive. Users can request to defer the remediation of a finding or remediation task for a specified period.

For example, an analyst might request a deferral for a finding that will be fixed with an upcoming patch that isn't currently available. A false positive might be a warning given by a scanner that is not actually an issue, for example, if a configuration item has been decommissioned but the scanner is still raising there is issue related to it.

In some cases, the approval requests for these exceptions and false positives require multiple levels or review and approval and can be quite time consuming. The Approval Recommendation AI skill can help locate historical, asset, and vulnerability details for exception and false positive requests and provide approvers with the following information:

-   A recommendation to approve or reject the request.
-   A confidence score.
-   Supporting reasoning.

## Sources and input parameters used for the recommendations

The Approval Recommendation generative AI skill considers information from following tables, data sources, and information to arrive at its approval recommendations.

-   See the following table for asset \(configuration item\) and vulnerability details.
-   Historical Approval data - Count totals for how many times similar request types for false positives and deferrals from a finding type \(VIT, CVIT, AVIT, CTR\) have been approved or rejected on records on the Change Approval \[sn\_sec\_exception\_change\_approval\] table.
-   Questionnaire responses \(optional configuration\) - If questionnaires are activated and available for exception requests, the questions and the remediation owner's answers are considered from records on the \[sn\_smart\_asmt\_question\_instance\] table. If questionnaires are not activated, this data is not considered.
-   Comments \(justifications\) from previous approvals - If multiple approval levels are configured, comments provided by approvers at earlier levels on records on the Change Approval \[sn\_sec\_exception\_change\_approval\] table are considered when generating a recommendation at the next level.
-   General request details - The following fields on records on the Change Approval \[sn\_sec\_exception\_change\_approval\] table are considered:
    -   Risk rating
    -   Until date \(how long the exception is being requested for\)
    -   Remediation status \(in-flight, no target\)
    -   Assignment group
    -   Reason / justification notes \(why a request is submitted\)
    -   Work notes
    -   Request type
    -   Compensating control \(if available\)

## Asset and Vulnerability details

|Application|Source table|Description|
|-----------|------------|-----------|
|Vulnerability Response \(Host\)|Configuration item \(CI\) \[cmdb\_ci\] table records for Host assets|Total number of assets, business criticality, environment, internet-facing, and external-facing status.|
|Container Vulnerability Response \(CVR\)|Discovered Item \(Container\) \[sn\_vul\_container\_image\] table records for Container assets|Total number of assets, business criticality, environment, internet-facing, and external-facing status status.|
|Application Vulnerability Response \(AVR\)|Discovered Item \(Application\) \[sn\_vul\_app\_release\] records for Application Vulnerability Response|Total number of applications, business criticality, active/inactive status.|
|Configuration Compliance CC|Test Results \[sn\_vulc\_result\] table for Configuration Compliance|Total number of assets, business criticality, environment, internet-facing, and external-facing status status.|

|Application|Vulnerability details|
|-----------|---------------------|
|Vulnerability Response \(Host VR\)|Total counts of vulnerabilities, normalized severity, CVSS scores, CISA exists, active exploit, preferred solution, EPSS percentile.|
|Container Vulnerability Response \(CVR\)|Total counts of container vulnerabilities, normalized severity, CVSS scores, CISA exists, active exploit, preferred solution, EPSS percentile.|
|Application Vulnerability Response \(AVR\)|Total counts of application vulnerabilities, normalized severity, CVSS scores, active exploit, preferred solution, EPSS percentile, and if threat exists.|
|Configuration Compliance \(CC\)|Test result data is used instead of vulnerability data. Total counts of tests, test source category, test subcategory, criticality, and technology.|

The Approval Recommendation generative AI skill provides its suggestions and is visible on approval request records \(CA\)s. For more information about how to invoke the agent and get the recommendations, see [Generate approval recommendations with generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/sem-approval-recommendation-skill.md).

-   **[Generate approval recommendations with generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/sem-approval-recommendation-skill.md)**  
Use a generative AI skill to streamline the approval process for exceptions and false positive requests with AI-driven recommendations. Reduce manual effort and improve decision accuracy for your approvers in the Security Exposure Management Workspace.

**Parent Topic:**[Using Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/using-unified-security-exposure-management.md)

