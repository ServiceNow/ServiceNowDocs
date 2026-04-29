---
title: Unified experience framework for integrations powered by Capability Framework
description: In the classic UI, the experience is disjointed when performing orchestration activities such as running threat look, performing sighting search, and so on. Each capability has its own experience while executing it. In the new workspace, there is unified experience across all capabilities.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SIR Workspace Orchestration, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Unified experience framework for integrations powered by Capability Framework

In the classic UI, the experience is disjointed when performing orchestration activities such as running threat look, performing sighting search, and so on. Each capability has its own experience while executing it. In the new workspace, there is unified experience across all capabilities.

The unified experience is applicable only for those integrations and orchestration activities that fall within the capability framework. There can be actions specific to integration, for example, Create Indicators in Microsoft Defender. These actions will have its own experience as required by the use-case.

The new framework consists of modal screens with three steps as explained below.

1.  **Implementations**: The first step involves selecting one or more implementations that are present against the selected capability.

    For example, when the Analyst clicks **Run Threat Look Up**, the Analyst will be able to select one or more implementations that are present for **Run Threat Look Up capability**.

    Each implementation will have the details of the Integration Source. Refer to the table below. Additional information is also presented against each implementation.

    Additional Information can include for example information on any filters, types of observables supported, etc. The Additional Information can be configured as desired. For more information, to UX framework technical configuration procedure.

<table id="table_ysx_rc1_vvb"><thead><tr><th>

Implementation

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the implementation.

</td></tr><tr><td>

Integration Source

</td><td>

The source of the implementation such as the configuration that is being used.

</td></tr><tr><td>

Additional Information

</td><td>

This column captures the static information which adds more context to the security analyst against the selected implementation\(s\) to proceed with an action. For example, supportability or filtered information. Also, if an implementation supports only a certain type of observables such as Domain or URL, then you can add that additional information here in this column to provide the context to the user.**Note:** The UI framework would basically allow the selection of any type of implementation and any type of observables. During the submission, the existing base system integrations that are shipped will take care of the filtering in the backend and submit only the supported type of observables. The rest of the records that don't match the supportability will be ignored. Hence, a UI information message is displayed while you select the capability: **Only supported records will be submitted against the selected implementation\(s\).**

</td></tr></tbody>
</table>    ![Run Threat Lookup view: Available Implementations.](../image/screen1.png "Screen 1: Implementation(s)")

2.  **Common inputs**: Add common inputs for the selected implementations or for all the selected applicable implementations. This is the screen 2 of your implementation. For example, as of now only **Sightings Search** has the common inputs screen. This implementation is a combination of screen 1 \(Implementations\) and screen 2 \(common inputs\).

    ![Run Sighting Search view: Common inputs.](../image/common-input-hours.png "Screen 1 + Screen 2")

3.  **Run time details**: Add specific run time inputs for the selected implementations which are different from each other implementation. This is the screen 3 of your implementation. This implementation is a combination of screen 1 \(Implementations\) and screen 3 \(specific run time inputs\).

    ![Run Additional Actions view: Run time details.](../image/screen3.png "Specific inputs")


**Note:** Not all three steps are always required. Depending on the capability and the type of inputs required, the runtime details step and common inputs step will be visible.

-   **[Unified experience capabilities and modal screens](../reference/capabilities-and-modal-screens.md)**  
The following table below describes the capabilities and applicable screens.
-   **[Unified Experience examples](unified-expereince-example.md)**  
This example demonstrates the unified experience framework capabilities.

**Parent Topic:**[SIR Workspace Orchestration](security-incident-response-workspace-orchestration-activities.md)

**Related topics**  


[SIR Workspace Investigation Canvas](security-incident-response-investigation-canvas.md)

