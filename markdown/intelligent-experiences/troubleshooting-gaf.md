---
title: Troubleshooting Group Action Framework
description: Troubleshoot common errors associated with configuring GAF, such as failed action strategy job trigger or the scheduled job failing to execute.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/troubleshooting-gaf.html
release: australia
topic_type: concept
last_updated: "2026-07-16"
reading_time_minutes: 2
keywords: [group action framework, gaf]
breadcrumb: [Reference, AI Agent Studio, Enable AI experiences]
---

# Troubleshooting Group Action Framework

Troubleshoot common errors associated with configuring GAF, such as failed action strategy job trigger or the scheduled job failing to execute.

## Identifying GAF script executions and logs

Review records on the GAF scheduled script executions \[sn\_gaf\_sysauto\_script\] table to verify whether the script ran. The interval between script runs to refresh the clusters is not configurable and may vary between different skills, AI agents, or agentic workflows, but the default is 90 days for the ITSM GAF Grouping and CSM GAF Grouping jobs.

To find logs where GAF is used on your instance, go to the Generative AI Log \[sys\_generative\_ai\_log\] table and filter the **Metadata Table** field for `sn_gaf`. Actions performed by skills, AI agents, and agentic workflows that use GAF all generate logs.

## Common errors and resolution steps

You can encounter certain errors when configuring Group Action Framework if the skills or scheduled job aren't configured correctly. Common error messages, their causes, and potential solutions are described as follows.

-   **"Action strategy job trigger failed. The topic is not generated for any group."**

    Resolution steps:

    -   Verify your LLM provider \(OpenAI, Anthropic, etc.\) has valid credentials and available token quota. Check the LLM provider configuration in your instance.
    -   Verify that the GAF record group \[sn\_gaf\_record\_group\] table contains records. If empty, the grouping skill may have failed. Check the ML Solution \[ml\_solution\] table for error details.
    -   Verify that the Action Strategy Group table field in your Grouping Skill Config is empty. The field is populated automatically by the GAF setup job because the Group table refers to the table where the grouped records are, not the source table. If this field is populated before you run the script, the GAF job will fail. Clear the field and retry.
    -   Verify you have at least 2,000 records in your source table. If fewer, add more data or adjust your filters.
-   **"Scheduled job did not execute" or job status shows as "Waiting"**

    Resolution steps:

    -   Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**, search for the prerequisite job \(e.g., "HR service GAF grouping job"\), and verify that the **Active** field is set to true and the **Class** field is populated.
    -   Verify you have the sn\_aia.admin role to run background scripts.
    -   If the job is in "Waiting" status, the system may be busy. Wait a few minutes and check again.
-   **"Failed to initialize pipeline: Failed to load message\_content dataset. No columns to parse from file."**

    You might not have the right role to run the scripts required to populate the GAF tables. There must be a ml\_platform read ACL for GAF to be configured.

    Resolution: If the read ACL is not present, create it and grant the appropriate role access, such as admin, ml\_admin, or sn\_aia.admin.


