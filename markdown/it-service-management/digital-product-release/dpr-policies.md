---
title: Digital Product Release policies
description: The Digital Product Release Policy Content Pack contains a set of policies to automate phase gate verification and continuous evaluation of software artifacts.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [PaCE content, PaCE policies, PaCE content policies, DevOps Config policies, DevOps Config policies, PaCE policies, DevOps Config Policy content pack]
breadcrumb: [Digital Product Release Policy Content Pack, Digital Product Release, IT Service Management]
---

# Digital Product Release policies

The Digital Product Release Policy Content Pack contains a set of policies to automate phase gate verification and continuous evaluation of software artifacts.

You can use or customize these default DPR policies to validate that your configuration data content is conformable, or administrate the full life cycle of PaCE policies. For more information, see [Policy as Code Engine \(PaCE\)](https://www.servicenow.com/docs/access?context=pace-managing-policies&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Note:** You can’t modify the base system policies. However, you can create a copy of the policy and customize it.

These policies are for both product and service releases. However, a few don't apply to service releases. For more information about those policies, see [Policies not applicable to service releases](dpr-policies.md#dpr-section_policy-not-service).

## All Completed Stories Have Associated Commits \(all\_completed\_stories\_have\_associated\_commits\)

This policy checks whether all the completed stories of a release have associated commits.

The policy results into a non-compliant status when a completed story of a release has no associated commits.

## All Planned Stories Are Completed \(all\_planned\_stories\_are\_completed\)

This policy checks whether all the planned stories of a release are completed.This policy also checks if the product version is associated with plan version. If it’s associated with plan version, it checks all stories associated with plan version in addition to the stories associated with epics in features or enhancements.

The policy results into a non-compliant status when the completion percentage of stories planned for a release isn’t `100%`. The completion percentage of planned stories is calculated as `(Total completed stories/Total planned stories) * 100`.

## Code Coverage Exceeds Threshold \(code\_coverage\_threshold\)

This policy checks whether the percentage of code coverage exceeds the threshold value.

The policy results into a non-compliant status when the percentage of code coverage is less than the specified threshold value. The percentage of code coverage for a release is the average code coverage calculated for all artifact versions included in the release.

**Note:** The artifact versions with no code coverage data are excluded from the average code coverage calculation.

-   **Input arguments**

    minCodeCoverageThreshold

    -   The minimum accepted value for the code coverage for a release.
    -   Default value: `100`
    -   Type: Integer
    -   Usage: Mandatory

## Integration Test Pass Exceeds Threshold \(integration\_test\_pass\_threshold\)

This policy checks whether the percentage of passed integration tests is not less than the threshold value.

The policy results into a non-compliant status when the percentage of passed integration tests is less than the specified threshold value. The passed integration tests percentage is calculated as `(Total passed integration tests for all artifact versions/Total integration tests for all artifact versions) * 100`.

-   **Input arguments**

    minTestPassThreshold

    -   The minimum accepted value for the percentage of passed integration tests.
    -   Default value: `100`
    -   Type: Integer
    -   Usage: Mandatory

## Load Test Pass Exceeds Threshold \(load\_test\_pass\_threshold\)

This policy checks whether the percentage of passed load tests is not less than the threshold value.

The policy results into a non-compliant status when the percentage of passed load tests is less than the specified threshold value. The passed load tests percentage is calculated as `(Total passed load tests for all artifact versions/Total load tests for all artifact versions) * 100`.

-   **Input arguments**

    minTestPassThreshold

    -   The minimum accepted value for the percentage of passed load tests.
    -   Default value: `100`
    -   Type: Integer
    -   Usage: Mandatory

## No Critical Vulnerabilities Found \(no\_critical\_vulnerabilities\)

This policy checks whether there are no critical vulnerabilities found in a release.

The policy results into a non-compliant status when the total number of vulnerabilities categorized as blocker, critical, high, or major is greater than zero.

## Regression Test Pass Exceeds Threshold \(regression\_test\_pass\_threshold\)

This policy checks whether the percentage of passed regression tests isn’t less than the threshold value.

The policy results into a non-compliant status when the percentage of passed regression tests is less than the specified threshold value. The passed regression tests percentage is calculated as `(Total passed regression tests for all artifact versions/Total regression tests for all artifact versions) * 100`.

-   **Input arguments**

    minTestPassThreshold

    -   The minimum accepted value for the percentage of passed regression tests.
    -   Default value: `100`
    -   Type: Integer
    -   Usage: Mandatory

## Smoke Test Pass Exceeds Threshold \(smoke\_test\_pass\_threshold\)

This policy checks whether the percentage of passed smoke tests is not less than the threshold value.

The policy results into a non-compliant status when the percentage of passed smoke tests is less than the specified threshold value. The passed smoke tests percentage is calculated as `(Total passed smoke tests for all artifact versions/Total smoke tests for all artifact versions) * 100`.

-   **Input arguments**

    minTestPassThreshold

    -   The minimum accepted value for the percentage of passed smoke tests.
    -   Default value: `100`
    -   Type: Integer
    -   Usage: Mandatory

## System Test Pass Exceeds Threshold \(system\_test\_pass\_threshold\)

This policy checks whether the percentage of passed system tests is not less than the threshold value.

The policy results into a non-compliant status when the percentage of passed system tests is less than the specified threshold value. The passed system tests percentage is calculated as `(Total passed system tests for all artifact versions/Total system tests for all artifact versions) * 100`.

-   **Input arguments**

    minTestPassThreshold

    -   The minimum accepted value for the percentage of passed system tests.
    -   Default value: `100`
    -   Type: Integer
    -   Usage: Mandatory

## User Acceptance Test Pass Exceeds Threshold \(user\_acceptance\_test\_pass\_threshold\)

This policy checks whether the percentage of passed user acceptance tests is not lower than the threshold value.

The policy results into a non-compliant status when the percentage of passed user acceptance tests is less than the specified threshold value. The passed user acceptance tests percentage is calculated as `(Total passed user acceptance tests for all artifact versions/Total user acceptance tests for all artifact versions) * 100`.

-   **Input arguments**

    minTestPassThreshold

    -   The minimum accepted value for the percentage of passed user acceptance tests.
    -   Default value: `100`
    -   Type: Integer
    -   Usage: Mandatory

## Validate change requests \(validate\_change\_requests\)

This policy checks whether all change requests are in the given states, across all phases or a single phase of a release.

The policy results into a non-compliant status when at least one change request is not in any of the given states.

-   **Input arguments**

    **Validate all phases**: Determines whether to check the state of change requests in all phases or in a single phase of a release.

    -   Default value: `False`
    -   Type: Boolean
    -   Usage: Mandatory
    **States to validate**: An array of states of change requests to validate. It accepts comma-separated numeric values corresponding to the states.

    -   Default value: Empty
    -   Type: Data Array
    -   Usage: Mandatory

## Policies not applicable to service releases

The following policies don't apply to service releases.

-   all\_completed\_stories\_have\_associated\_commits
-   integration\_test\_pass\_threshold
-   regression\_test\_pass\_threshold
-   system\_test\_pass\_threshold
-   code\_coverage\_threshold
-   no\_critical\_vulnerabilities
-   load\_test\_pass\_threshold
-   smoke\_test\_pass\_threshold
-   user\_acceptance\_test\_pass\_threshold

**Related topics**  


[Digital Product Release data collectors](dpr-data-collector.md)

