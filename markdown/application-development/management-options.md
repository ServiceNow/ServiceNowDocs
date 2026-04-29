---
title: Deployment management options
description: ServiceNow offers multiple management options for orchestrating deployments. Your choice depends on your organization’s maturity, licensing, and operational preferences. You can choose between ReleaseOps, App Engine Management Center Pipelines and Deployments, or System Update Sets.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Deployment, Getting Started guide for developers, Building applications]
---

# Deployment management options

ServiceNow offers multiple management options for orchestrating deployments. Your choice depends on your organization’s maturity, licensing, and operational preferences. You can choose between ReleaseOps, App Engine Management Center Pipelines and Deployments, or System Update Sets.

|Capability|ReleaseOps|App Engine Management Center Pipelines and Deployments|System Update Sets|
|----------|----------|------------------------------------------------------|------------------|
|Introduced|Zurich release \(2025\)|San Diego release \(2022\)|Legacy \(platform foundation\)|
|Deployment unit|System Update Sets with automated pipeline.|Application versions with Application Repository.|Grouped configuration changes.|
|Automation|Playbook, automated validation, and pipeline orchestration.|Guided pipelines with approval gates, Automated Test Framework, and Instance Scan.|Manual: retrieve, preview, commit.|
|Version tracking|With update set batches and release packages.|Full semantic versioning in the application repository.|Limited \(update set names only\).|
|Best for:|Organizations wanting automated CI/CD-style pipelines for any deployment type.|Teams building custom scoped applications with App Engine products.|Quick operational changes, global scope configuration, legacy workflows.|
|Licensing|Included with platform.|Included with App Engine.|Included with platform.|

## ReleaseOps

ReleaseOps is the deployment orchestration tool introduced with the Zurich release. It provides automated pipelines that move update sets from development through test to production with built-in validation steps called Playbook.

ReleaseOps uses the multi-instance framework \(MIF\) to coordinate across instances. It can be installed on all participating instances with the Application Manager. It supports on-demand deployments and scheduled release trains.

For more information, see [ReleaseOps](../../release-ops/concept/releaseops-landing.md).

## App Engine Management Center Pipelines and Deployments

App Engine Management Center has been available since the San Diego release. It provides a centralized dashboard for monitoring custom application development, managing deployment pipelines, and governing developer access. Pipelines and Deployments within App Engine Management Center orchestrate the movement of application versions through configurable pipeline stages with built-in quality gates. The built-in quality gates include Automated Test Framework execution and Instance Scan checks. App Engine Management Center also generates change requests for each deployment, providing audit trail and compliance documentation.

For more information, see [App Engine Management Center](../../app-engine-management-center/concept/app-engine-management-center.md).

## System Update Sets

System Update Sets are the original deployment mechanism on the ServiceNow platform. They capture configuration changes as a group that can be transferred between instances with XML export/import or remote instance retrieval. While System Update Sets remain widely used, especially for global scope changes and operational teams, they lack the version management, automated validation, and pipeline orchestration that modern tools provide. They are also prone to human error. Scope contamination, missing dependencies, and ordering issues are common pitfalls.

For more information, see [System update sets](../../system-update-sets/concept/system-update-sets.md).

**Parent Topic:**[Deployment](get-started-deployment.md)

