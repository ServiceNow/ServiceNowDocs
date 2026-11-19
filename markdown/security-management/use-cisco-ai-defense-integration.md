---
title: Vulnerability Response Integration with Cisco AI Defense data mapping
description: View and work with imported data from the Vulnerability Response Integration with Cisco AI Defense scan results and model validation data on records and dashboards in your ServiceNow AI Platform instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/use-cisco-ai-defense-integration.html
release: australia
topic_type: reference
last_updated: "2026-09-15"
reading_time_minutes: 2
breadcrumb: [Cisco AI Defense Integration for AI Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# Vulnerability Response Integration with Cisco AI Defense data mapping

View and work with imported data from the Vulnerability Response Integration with Cisco AI Defense scan results and model validation data on records and dashboards in your ServiceNow AI Platform instance.

Role required: sn\_vul\_cisco\_ai\_df.read or sn\_vul\_cisco\_ai\_df.admin.

After the integration runs, data appears in the following tables organized by data type.

|Table name|Description|
|----------|-----------|
|AI Scan Summary \(sn\_sec\_ai\_scan\_summary\)|Overview of all vulnerability scans, including scan status, findings by severity \(Critical, High, Medium, Low\), and total findings count.|
|AI Vulnerability Finding \(sn\_sec\_ai\_scan\_finding\)|Individual vulnerabilities found, including vulnerability ID, description, category, and severity level.|
|Discovered AI Assets \(sn\_sec\_ai\_src\_ci\)|AI models and files discovered during scans.|
|AI Vulnerability Entry \(sn\_sec\_ai\_vul\_entry\)|Detailed vulnerability information.|
|Model File \(sn\_sec\_ai\_file\)|File metadata including file name, file path, file size, file format, and last scanned timestamp.|

|Table name|Description|
|----------|-----------|
|AI Validation Findings \(sn\_sec\_ai\_validation\_finding\)|Validation job results including status, attack counts, and outcomes.|
|AI Validation Threat \(sn\_sec\_ai\_validation\_threat\)|Specific threat prompts tested against the model, including attack prompt, model response, attack result status \(FAILED, SUCCESS\), and severity level.|
|AI Threat Signature \(sn\_sec\_ai\_threat\_signature\)|Attack patterns detected, including attack category \(for example, CYBERBULLYING, HARASSMENT\), attack technique \(for example, keyboard\_augmenter\), MITRE ATT&amp;CK mappings, and NIST AI standards mappings.|

|Table name|Description|
|----------|-----------|
|Cisco AI Defense Policy \(sn\_vul\_cisco\_ai\_df\_policy\)|AI security policies imported from Cisco AI Defense, including policy status and connection type.|
|Cisco AI Defense Policy Guardrail \(sn\_vul\_cisco\_ai\_df\_m2m\_policy\_guardrail\)|Guardrail rules linked to each imported policy, including guardrail action and direction.|

See [Viewing AI Exposures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/ai-security-exposure-home.md) for more information about the finding types and the data displayed on the AI Security Exposure Management dashboard.

1.  Navigate to **All** &gt; **Security Exposure Management workspace** &gt; **AI Security Exposure Management** &gt; **AI Vulnerabilities**. The scan metrics are displayed.
2.  Select a scan metrics card to open it.
    -   Open Vulnerabilities
    -   Models scanned
    -   Model files scanned
3.  Select the **AI validation findings** tab.
4.  Select a validation metrics card to open it.
    -   Open validation findings
    -   Mitigated findings
    -   Active guardrails
    -   Models tested
    -   Number of attacks
5.  Select the **AI posture findings** tab.
6.  Select a Posture metrics card to open it.
    -   Open posture findings
    -   Agents with findings
    -   Tools with findings
    -   System prompts with findings
    -   MCP servers with findings

Integration not running:

-   Verify API credentials are correct.
-   Check network connectivity to Cisco AI Defense.
-   Review system logs for error messages.

No data appearing:

-   Verify that scans or validations exist in Cisco AI Defense.
-   Confirm that scans have severity findings. The integration only fetches scans with issues.
-   Verify transform maps are active.

Authentication errors:

-   Confirm the Tenant API Key is valid.
-   Confirm the API URL is correct.
-   Verify your Cisco AI Defense subscription is active.

-   Test each integration manually before scheduling.
-   Adjust limit parameters based on your data volume.
-   Regularly check import set processing for errors.
-   Run automated syncs when system load is low.
-   Use ServiceNow AI Platform reporting to track AI security trends.

**Parent Topic:**[Cisco AI Defense integration for AI security exposure management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/exploring-cisco-ai-defense-integration.md)

