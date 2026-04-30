---
title: Using DevOps Config
description: The developer, or app engineer, role uses DevOps Config, once it's installed and set up by the DevOps engineer role, to validate and correct config data \(that they commit\) before it gets deployed.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DevOps Config, IT Service Management]
---

# Using DevOps Config

The developer, or app engineer, role uses DevOps Config, once it's installed and set up by the DevOps engineer role, to validate and correct config data \(that they commit\) before it gets deployed.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

![DevOps Config use flow](../image/devops-config-use.png)

Consumption process:

1.  A configuration change is committed as part of the role of the developer, or app engineer.
2.  The build process is kicked off in the pipeline.

    When a configuration change is committed in the source code repository, it typically kicks off the build process in the pipeline.

3.  Upload configuration data using Azure DevOps pipeline tasks or Jenkins pipeline actions.

    DevOps Config pipeline tasks and actions are used to interact with your data model to upload config data for validation.

4.  Get snapshot status of the uploaded configuration file.

    A snapshort \(of configuration data\) is created when the configuration change is committed.

5.  Check validity of the snapshot using DevOps Config policies.

    Once config data is uploaded and the snapshot is created, it's validated in DevOps Config against a set of policies predefined for the specific deployment environment.

6.  Publish snapshot after validation.

    Once validated by DevOps Config, the config data is then published and a DevOps change request is created by DevOps Change Velocity \(change control\).

    Snapshot information is shown in the DevOps change request **Config changes** tab for accelerated root cause analysis.

7.  Approve the DevOps change request.

    Once the DevOps change request is approved, the config data is used downstream in your CI/CD pipeline.

8.  Deploy to your environment.

    Once the change is deployed to your environment, the change request is closed.

9.  Use DevOps Config exporters to export your config data to be used by your deployment tools.

