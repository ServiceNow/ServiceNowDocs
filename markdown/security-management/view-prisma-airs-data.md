---
title: Viewing imported data for the Vulnerability Response Integration with Palo Alto Prisma AIRS
description: View and work with imported data from the Vulnerability Response Integration with Palo Alto Prisma AIRS integration on records and dashboards in your ServiceNow AI Platform instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/view-prisma-airs-data.html
release: zurich
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 3
breadcrumb: [Palo Alto Prisma AIRS Integration for AI Security Exposure Management, Integrations, Unified Security Exposure Management, Security Operations]
---

# Viewing imported data for the Vulnerability Response Integration with Palo Alto Prisma AIRS

View and work with imported data from the Vulnerability Response Integration with Palo Alto Prisma AIRS integration on records and dashboards in your ServiceNow AI Platform instance.

## AI Security Exposure data tables

Roles required: sn\_vul\_prisma\_airs.read or sn\_vul\_prisma\_airs.admin.

After the integration runs, data is organized into the following tables by data type.

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
|Prisma AIRS Red Team Scan Guardrails \(sn\_vul\_prisma\_airs\_red\_team\_scan\_guardrails\)|Guardrail policies applied during Red Team scans, including policy ID, policy name, and policy configuration.|

See [Viewing AI Exposures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/ai-security-exposure-home.md) for more information about the finding types and the data displayed on the AI Security Exposure Management dashboard.

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

## Troubleshooting

<table><thead><tr><th>

Issue

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

Integration not running

</td><td>

-   Verify API credentials are correct.
-   Check network connectivity to Prisma AIRS.
-   Review system logs for error messages.

</td></tr><tr><td>

No data appearing

</td><td>

-   Verify scans or validations exist in Prisma AIRS.
-   Check that scans have severity findings. The integration only fetches scans with issues.
-   Verify transform maps are active.

</td></tr><tr><td>

Authentication errors

</td><td>

-   Confirm Client ID, Client Secret, and TSG ID are valid.
-   Check that the API URL is correct.
-   Check that the AUTH URL is correct.
-   Verify your Prisma AIRS subscription is active.

</td></tr></tbody>
</table>## Best practices

-   **Start with manual runs**

    Test each integration manually before scheduling to confirm data is importing correctly.

-   **Set appropriate limits**

    Adjust the Scan Limit and Validation Limit parameters based on your data volume to avoid overloading the instance.

-   **Monitor import sets**

    Regularly check import set processing for errors after each run.

-   **Schedule during off-peak hours**

    Run automated syncs when system load is low to minimize performance impact.

-   **Review data regularly**

    Use ServiceNow reporting to track AI security trends over time.


**Parent Topic:**[Palo Alto Prisma AIRS integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/prisma-airs-integration.md)

