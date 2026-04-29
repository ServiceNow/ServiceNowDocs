---
title: Deployment analyzer in ReleaseOps
description: The deployment analyzer reviews the update set in your release against rules to verify compliance with customizable rules.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer, code coverage, large scale deployment ServiceNow]
breadcrumb: [Explore, ReleaseOps, Deploying applications, Building applications]
---

# Deployment analyzer in ReleaseOps

The deployment analyzer reviews the update set in your release against rules to verify compliance with customizable rules.

The deployment analyzer scans a given deployment request \(and the update sets it contains\) to check for changes as compared to the current state of the production instance \(or the target release environment\). To do, the deployment analyzer relies on rules and Automated Test Framework \(ATF\) code coverage. The deployment analyzer operates as a playbook activity, the results of which can be consumed to decide different actions in the deployment process.

## Deployment analyzer rules

By default, the deployment analyzer has five rules. You can create rule types, definitions, and rules as needed. New rules appear in the playbook conditional setup automatically.

For more information, see [Deployment analyzer rules](../reference/deployment-analyzer-rules.md).

## Automated Test Framework \(ATF\) code coverage

The deployment analyzer also leverages Automated Test Framework \(ATF\) code coverage to evaluate code changes prior to deploying the changes to the production \(or target\) instance. ATF code coverage is a tool that enables you to determine what percentage of code in a deployment request is covered by ATF test suites.

By default, if ATF test suites cover less than 70 percent of the code in a deployment request, ReleaseOps transitions the deployment request to the **Reconciling** state and a test failure task is automatically created. You can adjust the ATF code coverage threshold in the deployment request assessment playbook. For more information, see [Set Automated Test Framework \(ATF\) code coverage](../task/set-atf-code-coverage-threshold.md).

For more information about ATF code coverage, see [ATF Code Coverage API](https://www.servicenow.com/docs/access?context=atf-code-coverage-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

