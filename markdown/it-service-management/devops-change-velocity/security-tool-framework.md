---
title: Security scan results
description: Security scan results display scan details from security scans configured on your GitHub Actions, Jenkins, Azure DevOps, GitLab, or Harness pipelines.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional info - Veracode, Veracode, Integrate, DevOps Change Velocity, IT Service Management]
---

# Security scan results

Security scan results display scan details from security scans configured on your GitHub Actions, Jenkins, Azure DevOps, GitLab, or Harness pipelines.

You can configure security scans in your GitHub Actions, Jenkins, Azure DevOps, GitLab, and Harness pipelines to retrieve the scan results in DevOps Change Velocity. Security inbound events will be created in ServiceNow from the corresponding pipeline run that are then processed to store the scan results. You can view the scan results for each scan that was part of your build or release pipeline executions.

**Note:** If you want to configure Veracode for the GitLab tool, you can either use the generic Docker container image to add the Veracode security step or perform the steps specified in the [Integrate security tools with GitLab](../task/configure-security-tool-for-gitlab.md) topic.

The retrieved scan summaries are stored in the following tables:

|Column name|Description|
|-----------|-----------|
|Source|Source application vulnerability scanner for this application record.|
|Detected Flaw Count|Total number of new detected flaws in the scan.|
|Last scan date|Date of the most recent scan.|
|Last scan rating|Rating assigned by the scanner based on the detected items of the most recent scans.|
|Last static scan date|Date of the most recent static scan.|
|Last static scan rating|Rating assigned by the scanner based on the detected items of the most recent static scan.|
|Last dynamic scan date|Date of the most recent dynamic scan.|
|Last dynamic scan rating|Rating assigned by the scanner based on the detected items of the most recent dynamic scan.|
|Last interactive scan date|Date of the most recent interactive scan.|
|Last interactive scan rating|Rating assigned by the scanner based on the detected items of the most recent interactive scan.|

|Column name|Description|
|-----------|-----------|
|Category name|Name of the vulnerability category.|
|Severity|Severity of the flaws in the scan report.|
|Count|Number of flaws in the category for a severity.|

**Parent Topic:**[Veracode integration with DevOps Change Velocity](../concept/veracode-integration-with-devops-change-velocity.md)

