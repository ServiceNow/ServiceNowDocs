---
title: Validating and correcting configuration data
description: For every change to an environment, there may be tens or hundreds of rules \(policies\) that need to be checked. CDM enables you to auto-validate configuration data to ensure that configuration changes are error-free and policy-compliant before the config data is consumed.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using DevOps Config, DevOps Config, IT Service Management]
---

# Validating and correcting configuration data

For every change to an environment, there may be tens or hundreds of rules \(policies\) that need to be checked. CDM enables you to auto-validate configuration data to ensure that configuration changes are error-free and policy-compliant before the config data is consumed.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## CDM automates much of the validation process

When teams deploy an application, they typically need to ensure that no errors are introduced at the code and configuration level, and that compliance policies are respected. For every change to an environment, there may be tens or hundreds of rules \(policies\) that need to be checked. A manual validation process is prone to errors.

DevOps provides developers, IT admins, DevOps Config engineers, or team leads a way to ensure that configuration changes are error free and policy-compliant. In addition, after validation gives developers or IT admins enough contextual information to identify and fix issues. This means that after a user commits any changes to configuration data, all relevant policies are applied, results evaluated, and appropriate actions are triggered \(for example, deploy or do not deploy\).

Here's the CDM process that auto-validates configuration data before it is consumed.

1.  You create a policy version based on an existing policy and then activate and publish the new version.
2.  For dynamic mapping of policies to deployables, create a condition on the CDM Deployable \[sn\_cdm\_deployable\] table. Associate the condition with one or more policies. At runtime, these policies are executed to validate deployables that meet the defined conditions.
3.  You map the policy to a deployable using static mapping or dynamic mapping to ensure that the policy executes against any snapshot of the deployable when requested \(manual or automated request\).

    For more information on policy mappings, see [PaCE Static and Dynamic Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-policy-mapping.md).

4.  When you commit a changeset for the deployable, the system must validate the resulting snapshot. To auto-trigger execution of the mapped policies whenever a changeset is committed, select the **Validate** option when committing the changeset. You also have the option to validate the snapshot manually.

    In both cases, the policies mapped using static mapping and dynamic mapping are executed.

    -   If you configured the automated process to be integrated with your pipeline, then the policies return the results of the validation process to the pipeline in JSON files. The pipeline decides whether to continue based on the validation decision: Compliant, Non-compliant.
    -   If the process is not integrated with your pipeline, or if validation failed or did not finish, then you review the validation decision and take appropriate action.

## Use pre-defined policies as models for your custom policies

CDM includes policies that you can use as models for custom policies that meet specific needs. Note the following important patterns in the pre-defined policies;

-   The policies all use the `CdmQuery` script include to retrieve config data.
-   Use `CdmQuery` with Secrets to ensure all data is included.
-   The `CdmPolicyUtil` script include adds warnings and failures.
-   When all policies have run and a failure has been populated in the output, the decision is `non_compliant`.
-   Use the logger for debugging. Remove the logs when the policy is ready to be published.
-   Use mapping input parameters to supply dynamic input values.

## Guidelines for validating snapshots

-   Do not manually validate snapshots that have already been validated and published.
-   If you select the **Validate snapshots** or **Validate and publish snapshots** option when committing a changeset, then the system auto-validates each snapshot when it is first generated.
-   To view the current validation failures or warnings for a snapshot, open the snapshot and select the **Validation Results** tab. For details, see [View the results of snapshot validation](../task/cdm-validation-results-view.md).
-   Use the Policy Test Playground feature to revalidate snapshots while you develop a policy. The resulting validation results are flagged as test results and do not affect operations.
-   If there is a requirement to revalidate all snapshots for a deployable, revalidate only after you have tested and published the policies.

## Practices to avoid

-   Do not use GlideRecord to retrieve config data records.
-   To display policy decisions on the UI, CDM requires warning and failure data in a particular structure. Use `CdmPolicyUtil` to add warnings or failures \(not manual insertions\). \(At least understand the structure that `CdmPolicyUtil` inserts into failures and warnings.\)
-   In policies, do not attempt to retrieve data that does not come from CDM data. This practice can result in cross-scope access issues.
-   Do not write "always-compliant" or "always-non-compliant" policies.
-   Do not hard-code any names or values in policies. Instead, use mapping input parameters to supply dynamic input values.

## Snapshot status

-   Not validated: This is the initial snapshot state where no policy has been executed against the snapshot.
-   Requested: The validation flow has started.
-   In progress: The validation flow is running and policies are currently executing.
-   Passed: The snapshot has passed all policies.
-   Failed: The snapshot has failed one or more policies.
-   Execution error: A policy failed to run to completiondue to an unexpected error, mostly when the [CdmPolicyUtil script include](../reference/cdm-about-cdmpolicyutil.md) is not used to provide warning and failure messages..

## Example flow

A user commits changes to config data before a deployment.

Data is validated against all assigned policies.

If validation fails, then deployment is stopped. A list of errors pointing to their location in the config data is given to the user. Available actions should be determined in the context of the application itself and the environment where the application is deployed. For example:

-   Allow deployment in a TEST environment regardless of the number of errors or warnings.
-   Stop deployment in PROD if any error.
-   Stop deployment in PROD if any warning and if the application is critical.
-   Allow deployment in PROD regardless of the number of warnings if non-critical.

User fixes errors and recommits change.

Data is validated again and the results are ok.

A snapshot is taken.

Deployment is executed.

**Related topics**  


[CdmQuery - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/CdmQueryScopedAPI.md)

