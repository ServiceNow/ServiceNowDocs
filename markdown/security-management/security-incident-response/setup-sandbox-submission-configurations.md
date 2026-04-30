---
title: Set up Sandbox submission configurations
description: Set up the Sandbox configuration to define the analysis environment and runtime options for your security incident record submissions for the malware analysis.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Falcon X Sandbox integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up Sandbox submission configurations

Set up the Sandbox configuration to define the analysis environment and runtime options for your security incident record submissions for the malware analysis.

## Before you begin

Role required: sn\_si.admin

## About this task

Before you can submit files or URLs to the CrowdStrike Falcon X Sandbox using the integration, you must configure at least one submission configuration. The submission configuration defines the Sandbox operating system, scan type, run time options, and other incident handling characteristics. You may want to create multiple configurations to use the different options that available in the CrowdStrike Falcon X Sandbox environment.

## Procedure

1.  Navigate to **All** &gt; **CrowdStrike Falcon X Sandbox** &gt; **Configuration Settings**.

2.  Click **New**.

3.  Complete the following fields to create a configuration for a Full **Scan type**.

<table id="table_x33_npy_ymb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the submission configuration. This name appears to analysts when they submit a file. It is important to ensure that the name is descriptive and easily distinguishable from the other configurations \(example, Win 10 Full Scan\). If the name is not unique, an error appears and duplicate configuration record names do not save.

</td></tr><tr><td>

Scan type

</td><td>

Scan type as **Full**. A **Quick** scan type provides a limited threat analysis.

</td></tr><tr><td>

Operating system

</td><td>

Analysis VM environment that the sandbox scans the file or URL in.

</td></tr><tr><td>

Active

</td><td>

Option that you select when manually submitting files or URLs.

</td></tr><tr><td>

Default configuration for automated submission

</td><td>

Option that is cleared by default. Selecting this option enables this configuration to be available for automating malware analysis submissions. **Note:** You can have only one active submission configuration as the default configuration for automated submissions.

</td></tr><tr><td>

Display tags

</td><td>

Option that is cleared by default. When you select this option, tags are displayed to provide the status of a file or URL submission. The analysis may take several minutes to process. The display tags are submission initiated, submission completed, or submission failed.

</td></tr><tr><td>

Additional runtime options

</td><td>

Option that is cleared by default. When you select this option, additional runtime parameters that Sandbox supports are available.

</td></tr><tr><td>

Runtime action scripts

</td><td>

Option that enables you to use an action script that simulates human behavior and interacts with the file or URL during the analysis. [https://www.crowdstrike.com/endpoint-security-products/falcon-sandbox-malware-analysis/](https://www.crowdstrike.com/endpoint-security-products/falcon-sandbox-malware-analysis/) See CrowdStrike Falcon X Sandbox documentation for more details.

</td></tr><tr><td>

Network Settings

</td><td>

Option that allows you to select the type of network settings used while submitting an URL or file to Sandbox.

</td></tr></tbody>
</table>4.  Click **Submit**.

    After you submit the configuration, it is saved on the Configuration Settings page as a record. The configuration must be **Active** to be used in sandbox submissions.


## What to do next

After you configure sandbox

submissions, the next step is to [manually submit files or ULRs to Sandbox](submit-files-or-urls-to-sandbox.md)

.

