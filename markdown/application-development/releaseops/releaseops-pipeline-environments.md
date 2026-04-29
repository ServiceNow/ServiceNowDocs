---
title: Pipelines in ReleaseOps
description: A pipeline is the flow of a deployment in ReleaseOps. A pipeline's flow is defined within playbooks, which enables you to customize as needed.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer, custom pipeline, large scale deployment ServiceNow]
breadcrumb: [Explore, ReleaseOps, Deploying applications, Building applications]
---

# Pipelines in ReleaseOps

A pipeline is the flow of a deployment in ReleaseOps. A pipeline's flow is defined within playbooks, which enables you to customize as needed.

A pipeline consists of two stages, each represented by its own playbook: an assessment stage and a release stage.

-   The assessment stage moves changes in individual deployment requests through subprod instances and is designed to do deployment analysis and run scans and tests.
-   The release stage moves all changes within a release across its member deployment requests that have passed assessment by the scheduled date to production.

ReleaseOps includes sample playbooks to that include basic pipeline structure and capabilities. You can use the ReleaseOps sample playbooks or duplicate and customize them for your company's processes. The ReleaseOps sample playbooks are the release deployment playbook, deployment request assessment playbook, and on-demand deployment request assessment playbook.

|Playbook|Stage|Description|
|--------|-----|-----------|
|Deployment request assessment playbook|Assessment stage for a standard/scheduled release|Moves update sets in deployment request to the test instance and executes defined Automated Test Framework \(ATF\) tests \(as specified in the deployment request and the pipeline\).|
|On-demand deployment request assessment playbook|Assessment stage for an on-demand release|Runs the deployment analyzer and Instance Scan with [sample rules](../reference/deployment-analyzer-rules.md) to either enable or deny an on-demand deployment. Doesn’t run any ATF tests.|
|Release deployment playbook|Release stage|Prepares a release, including moving deployment requests that aren’t ready out of the release and calculating update set ordering. Used for both on-demand and scheduled releases.|

A pipeline maps intermediate instances to the playbook. For example, the sample playbooks reference a test instance, which must be mapped to a physical deployment instance. The actual pipeline runs from the source instance specified in the deployment request, to the destination instance specified in the release. Intermediate instances \(such as test\) are defined in the pipeline. ATF test suites can also be specified at the pipeline level to enforce a given list of tests to be run when a given pipeline is used.

Pipelines can use the sample ReleaseOps playbooks, custom playbooks, or a mix of both. Multiple pipelines can leverage the same playbooks by mapping a different instance definition, which is then referenced in the playbooks.

However, because the activities required during deployment might vary from release to release, ReleaseOps also provides a more flexible solution to having to create and adjust custom playbooks each time: runbook tasks. Runbook tasks can be added at the deployment request level and enable you to define the kind of activity \(manual or automated\) needed at the given playbook stage. For more information about runbook tasks, see [Runbook tasks in ReleaseOps](runbook-tasks.md).

