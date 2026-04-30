---
title: Digital Product Release data collectors
description: The Digital Product Release Policy Content Pack contains a set of data collectors to collect DevOps data to be validated against policies.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Digital Product Release \(DPR\), Digital Product Release Data Collectors, DevOps data collectors, Data Collectors, Digital Product Release Policy Content Pack]
breadcrumb: [Digital Product Release Policy Content Pack, Digital Product Release, IT Service Management]
---

# Digital Product Release data collectors

The Digital Product Release Policy Content Pack contains a set of data collectors to collect DevOps data to be validated against policies.

## Approval Task Completeness

The Approval Task Completeness data collector checks if all approval release tasks associated with a release phase are complete.

Input: Release phase.

Output:

-   true: All approval tasks are approved.
-   false: One or more approval tasks aren’t approved, or there are no approval tasks for the release phase.

## Artifact Story Complete

The Artifact Story Complete data collector returns the percent of stories completed that are associated with a release artifact. The formula used to calculate the percentage is: `Percentage of stories completed = (Number of completed Stories / (Total number of stories - Number of stories in cancelled state - Number of stories in deleted state)) * 100`.

Input: List of artifacts for a release phase.

Output: % of stories that are complete.

## Change Request State Validation

The Change Request State Validation data collector returns the number of change requests in the specified states. It can check at change requests in one phase or all phases of a release, based on the input.

Input: List of states to validate, Validates all phases, Release ID, and Phase ID.

Output: Total number of change requests in the given states.

## Code Coverage

The Code Coverage data collector returns the current code coverage calculated based on the artifact versions.

Input: List of artifacts for a release phase.

Output: % of code coverage.

## Commits Without Work Item

The Commits Without Work Item data collector returns the percent of commits that don't have an associated Work Item. The formula used to calculate the percentage is: `Percentage of commits without work item = (Number of commits without work item / Total number of commits in artifact) * 100`.

Input: List of artifacts for a release phase.

Output: % of commits without Work Item.

## Planned Story Completeness

The Planned Story Completeness data collector returns the percent of planned stories that are marked as complete. Stories from the Epics that are associated with the release are considered. The data collector also checks if the product version is associated with plan version. If it’s associated with plan version, it also considers all stories associated with plan version.The formula used to calculate the percentage is: `Percentage of stories completed = (Number of completed Stories / (Total number of stories - Number of stories in cancelled state - Number of stories in deleted state)) * 100;`.

Input: List of Epics associated with a release.

Output: % of planned stories that are marked as complete.

## Security Vulnerability

The Security Vulnerability data collector returns the number of security vulnerabilities that are associated with a particular category. Security vulnerabilities are identified based on the artifact versions and the category of vulnerability as follows:

-   Blocker: Returns the sum of blocker issues. Valid only for DevOps data.
-   Critical priority issues: For DevOps data, returns the sum of Critical issues. For SecOps data, returns the sum of Very High Priority issues. For both DevOps and SecOps data, returns the cumulative of the Critical and Very High Priority issues.
-   High priority issues: Returns the sum of High Priority issues from both DevOps and SecOps data.
-   Medium priority issues: Returns the sum of Medium Priority issues from both DevOps and SecOps data.
-   Major issues: Return the sum of Major issues from all artifacts. Valid only for DevOps data.
-   Minor issues: Return the sum of Minor issues from all artifacts. Valid only for DevOps data.

Input: List of artifacts for a release phase.

Output: Total number of vulnerabilities.

## Test Pass

The Test Pass data collector returns the percent of passed tests based on artifact versions. If the test type is provided, it returns the test results only for the given test type, otherwise for all test types for the artifact version. The formula used to calculate the percentage is: `Percentage of tests passed = (Number of tests passed / (Total number of tests - Number of skipped tests)) * 100`.

Input: List of artifacts for a release phase and Test type \(optional\).

Output: % of tests passed.

## Work Items Have Commits

The Work Items Have Commits data collector returns whether all Work Items have a related commit. The Work Items are identified based on the Epics related with the release.The data collector also checks if the product version is associated with plan version. If it’s associated with plan version, it also considers all stories associated with plan version. The formula used to calculate the percentage is: `Percentage of stories without commits = (Number of completed stories without commits / Total number of stories in completed state) * 100`.

Input: List of artifacts for a release phase.

Output: % of commits without Work Item.

**Related topics**  


[Digital Product Release policies](dpr-policies.md)

[Passing parameters to PaCE policies](https://www.servicenow.com/docs/access?context=pace-passing-parameters&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

