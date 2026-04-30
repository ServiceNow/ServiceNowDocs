---
title: Targeted Communications publication workflows
description: The Targeted Communications application \(com.sn\_publications\) includes default workflows that are used for publishing articles.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Targeted communications, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Targeted Communications publication workflows

The Targeted Communications application \(com.sn\_publications\) includes default workflows that are used for publishing articles.

The application includes two publishing workflows:

-   **Instant Publish**: Publishes an article instantly.
-   **Publish With Approval**: Requires approval before publishing.

## Migrating workflows to Workflow Studio flows

Starting with the Zurich release, legacy workflows for the Targeted Communications application have been migrated to low-code flows in [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US). The functionality of the new flows remains the same.

During an upgrade, the logic checks if a publication workflow or its configuration has been customized.

-   If customizations are detected in the workflows or the configuration, the system reverts to the legacy workflows and disables the new flows and related configurations.
-   If no customizations are detected, the system replaces the legacy workflows with the new flows.

This upgrade logic ensures that customizations are preserved and are not overwritten.

## Summary of upgrade actions

The following table provides a summary of the actions that take place during upgrade depending on publication workflow and configuration customization.

|Setting|Customization detected|No customization detected|
|-------|----------------------|-------------------------|
|Legacy workflows|Activated|Deactivated|
|New flows|Deactivated|Activated|
|Legacy UI policies|Activated|Deactivated|
|New UI policies|Deactivated|Activated|
|Legacy business rules|Activated|Deactivated|
|New business rules|Deactivated|Activated|
|Workflow config value|Set to legacy workflows|Set to new flows|

## Key steps during upgrade to Zurich

The following table describes the key steps that the system takes during upgrade to the Zurich release.

<table id="table_cfg_bz1_5fc"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Customization detection

</td><td>

The logic checks if the legacy workflows or the sn\_publications\_workflow\_config table record 6c9b0e65c30112004bd67bfaa2d3ae56 have been customized. If customizations are found, the system reverts to the legacy workflows.

</td></tr><tr><td>

2. Legacy workflow activation

</td><td>

-   The legacy versions of the workflows are activated:
    -   Instant Publish
    -   Publish With Approval
-   The script chooses the correct workflow version based on the installed plugins.
-   If the Customer Service Base plugin is active, the script activates the following workflow versions:
    -   Instant Publish \(Base\): e7de79b7c3401300e7c7d44d81d3aece
    -   Publish With Approval \(Base\): 33987078c3d01300e7c7d44d81d3ae2f
-   If the plugin is not active, the script activates the following workflow versions:
    -   Instant Publish: f6d5c49a93201300ac40f5be867ffb3f
    -   Publish With Approval: 5be6c89a93201300ac40f5be867ffba1

</td></tr><tr><td>

3. New flow deactivation

</td><td>

-   New Flow Designer flows for publications are deactivated:
    -   Publish With Approval Flow
    -   Instant Publish Flow
-   All snapshots for these flows are also deactivated.

</td></tr><tr><td>

4. UI policy management

</td><td>

-   Legacy UI policies are activated:
    -   Approver field required \(legacy\)
    -   Hide approver field \(legacy\)
    -   Show legacy workflow
-   New UI Policies are deactivated:
    -   Hide approver field
    -   Show process flow
    -   Approver field required

</td></tr><tr><td>

5. Business rule management

</td><td>

-   Legacy business rules for starting the old publication workflow are activated.
-   New business rules related to new flows are deactivated.

</td></tr><tr><td>

6. Workflow configuration update

</td><td>

The workflow configuration record \(sn\_publication\_workflow\_config\) is updated to point out to the correct process workflow:-   If legacy workflows are present, the config is set to use the corresponding legacy flow.
-   If not, it defaults to the Instant Publish Flow.

</td></tr></tbody>
</table>## What to do before and after upgrading

Follow these steps before and after upgrading to the Zurich release:

-   Before upgrading, review your publication workflow customizations.
-   After upgrading, verify that the correct workflows, flows, UI policies, and business rules are active as expected.
-   If you want to use the new flows, remove customizations and reactivate the new flows and related configurations.

<table id="table_pgg_hcb_5fc"><thead><tr><th>

Setting

</th><th>

If customization detected \(sys\_id\)

</th></tr></thead><tbody><tr><td>

Legacy workflows

</td><td>

Activated:-   Instant Publish: a9587563d76302004f1e82285e6103ae
-   Publish With Approval: 51a2f923d76302004f1e82285e610355

</td></tr><tr><td>

New flows

</td><td>

Deactivated:-   Publish With Approval: e91f81a9a3e352107ee9d8b8651e6137
-   Instant Publish: ec48616da36752107ee9d8b8651e611f

</td></tr><tr><td>

Legacy UI policies

</td><td>

Activated:-   Mandatory Approver: df2ea83bc34112004bd67bfaa2d3aef5
-   Hide Approver: 3afeac3bc34112004bd67bfaa2d3ae29
-   Show Legacy Workflow: 567136f84f0c62107ee9a701b1ce0b31

</td></tr><tr><td>

New UI policies

</td><td>

Deactivated:-   Mandatory Approver \(Flow\): 5a0f230ea3a312107ee9d8b8651e6110
-   Hide Approver \(Flow\): 26d92306a3a312107ee9d8b8651e6107
-   Show Process Flow: 57f5c434a39b52107ee9d8b8651e61e4

</td></tr><tr><td>

Legacy business rules

</td><td>

Activated:-   Start New Publication: 11eb8390c3a012004bd67bfaa2d3aeb8
-   Approver List Required: 6a88a328c39112004bd67bfaa2d3ae04

</td></tr><tr><td>

New business rules

</td><td>

Deactivated:Approver List Required \(New Flows\): 47b133b2a36b12107ee9d8b8651e61d1

</td></tr><tr><td>

Workflow config value

</td><td>

Set to legacy flow:-   Config Record: 6c9b0e65c30112004bd67bfaa2d3ae56
-   Legacy Workflow sys\_ids: a9587563d76302004f1e82285e6103ae, 51a2f923d76302004f1e82285e610355

</td></tr></tbody>
</table>## Workflow Config table update

The upgrade to Zurich adds the following columns to the Workflow Config \[sn\_publications\_workflow\_config\] table:

-   **Process Workflow** \(Workflow Studio flow field\)
-   **Workflow** \(legacy workflow field\)
-   **Approvers**

