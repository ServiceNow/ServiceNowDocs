---
title: CAM workflow configuration
description: Configure custom workflows in Continuous Authorization and Monitoring to support compliance requirements beyond the default National Institute of Standards and Technology NIST Risk Management Framework.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 4
breadcrumb: [Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# CAM workflow configuration

Configure custom workflows in Continuous Authorization and Monitoring to support compliance requirements beyond the default National Institute of Standards and Technology NIST Risk Management Framework.

The CAM Workflow Configuration enables you to configure custom workflows and frameworks instead of restricting operations to the National Institute of Standards and Technology \(NIST\) framework. This flexibility enables you to adapt CAM to your specific compliance and authorization requirements.

Previously, CAM maintained tight coupling with the NIST framework and its seven-step process: Prepare, Categorize, Select, Implement, Assess, Authorize, and Monitor. The Workflow Configuration decouples CAM from this single framework, enabling you to create and map custom workflows to authorization packages and boundaries.

The configuration uses existing authorization package records and adds flexible state models that can map to different workflows. This approach maintains backward compatibility while enabling support for multiple workflows.

## Workflow configuration

A workflow configuration defines the workflow, framework, regulation, and its associated versions, impacts, and view rules. CAM ships NIST workflow configuration, but you can create additional workflows for other frameworks such as Protective Security Policy Framework \(PSPF\) or custom internal frameworks.

Each workflow configuration includes:

-   **Versions**: Different revisions of the workflow \(for example, NIST Rev 4 and Rev 5\)
-   **Workflow impacts**: Impact levels used to filter control objectives \(for example, Low, Moderate, High\)
-   **View rules**: Custom views that apply only to specific workflows
-   **State model**: Links the workflow to a specific state model

## State model

A state model defines the steps, transitions, and validations for a workflow. The state model is applied to the authorization package table and controls how packages move through the workflow life-cycle.

State models include:

-   **Workflow states**: Individual steps in the framework \(for example, Prepare, Categorize, Select\)
-   **State transitions**: Valid paths between steps, with required validation conditions.
-   **State model attributes**: Special capabilities like approval requirements or report generation. State model attributes are to control the functionality available at specific workflow steps.

## State transitions

State transitions define how packages move from one step to another. Each transition can include validation conditions that must be satisfied before proceeding.

Examples of validation conditions:

-   Authorization boundary field can’t be empty
-   All baseline controls must have "Create controls automatically" enabled
-   Required approvals must be completed

## State model attributes

Attributes add special capabilities to workflow states without requiring custom code. Attributes control features like approval requirements, report generation, related list actions, and UI page visibility for specific workflow states.

For a complete list of available attributes, see [Add existing attributes to a GRC workflow state](../task/configure-state-model-attributes.md).

## Workflow limitations

Without the CAM Advanced plugin \(app-grc-cont-auth-monitor-advanced\), you can create a maximum of two workflows \(including the NIST workflow\). Installing the CAM Advanced plugin removes this limitation and enables unlimited workflow configurations.

## Enabling workflow configuration

The workflow configurator is available only when CAM Workspace is installed. A system property controls whether custom workflows are enabled. For more information, see [Continuous Authorization and Monitoring system properties](../reference/cam-components-installed.md#).

When you enable the workflow configuration property:

-   The system displays a confirmation dialog explaining the impacts
-   Existing packages and boundaries must be migrated to associate them with workflows
-   The property can’t be inactive after activation
-   The system refreshes to apply the new configuration

**Important:** After enabling the property, you must run the migration scheduled job to associate existing packages and boundaries with the NIST workflow. Packages and boundaries without workflow associations have limited functionality.

## Migration behavior

When migrating existing data, CAM automatically assigns all packages and boundaries to the workflow.

The migration process:

-   Identifies all authorization packages and boundaries without workflow assignments
-   Associates them with the default NIST workflow configuration
-   Updates the home page to display workflow-specific tabs
-   Enables workflow-based filtering and reporting

## OSCAL export and import

When the workflow configuration property is enabled, OSCAL export includes workflow and framework metadata.

## Export and import scenarios

-   **Property off \(export\) → Property on \(import\)**

    Imported packages default to NIST workflow because no workflow data exists in the export

-   **Property on \(export\) → Property off \(import\)**

    Import succeeds but packages lack workflow functionality

-   **Property on \(both instances\)**
    -   If the workflow exists in the import instance: Package uses that workflow
    -   If the workflow doesn’t exist in the import instance: Package experience is broken and must be manually corrected

**Note:** CAM doesn’t support importing packages with missing workflow configurations. You must create matching workflows in the target instance before importing.

## Assessment capabilities

The Send Assessment button enables both classic assessments and risk assessments \(when Advanced Risk Management is installed\).

## Classic assessments

Platform assessments that use assessment metric types. You must create or modify assessment templates where the table is set to Authorization Package.

## Risk assessments

Risk Assessment Methodology \(RAM\) assessments that evaluate risks associated with packages and boundaries. Risk assessments appear in a separate related list on the package form.

**Note:** CAM doesn’t ship assessment templates for authorization packages. You must create or modify existing templates for both assessment types.

