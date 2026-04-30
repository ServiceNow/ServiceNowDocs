---
title: Troubleshooting issues of Azure DevOps integration with SAFe
description: Resolve common issues that you might face while working with the integration of Azure DevOps and SAFe.
locale: en-US
release: yokohama
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Azure DevOps integration with SAFe, Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Troubleshooting issues of Azure DevOps integration with SAFe

Resolve common issues that you might face while working with the integration of Azure DevOps and SAFe.

<table id="table_nsr_k31_w4b"><thead><tr><th>

Issue

</th><th>

Action

</th></tr></thead><tbody><tr><td>

The **ART** and **ART Iteration Path** fields are not displayed in the Azure DevOps project form.

</td><td>

Ensure that table mapping exists for SAFe stories.

</td></tr><tr><td>

Sprint is not imported from Azure DevOps to SAFe.

</td><td>

-   Check the state of the sprints. Sprints of only the states Future and Current are imported.
-   Ensure that there are no overlapping sprints.

</td></tr><tr><td>

PI is not imported from Azure DevOps to SAFe.

</td><td>

-   Ensure that there are no overlapping PIs.
-   Ensure that the correct ART Iteration Path is selected in the Azure DevOps project form.

</td></tr><tr><td>

The error message **Ensure that the selected assignment group belongs to the ART and try again** is displayed in the Azure DevOps project form.

</td><td>

The assignment groups in all the team integration settings of this Azure DevOps project must be the SAFe teams that belong to the ART selected for this project.

 If not, add these SAFe teams to the ART and proceed to create team integration settings using these SAFe teams as assignment groups.

</td></tr><tr><td>

Sprints are not linked with SAFe features

</td><td>

Features can be linked to the PI but not with the sprints, as it's not supported in SAFe. Select the PI iteration path in the feature in the Azure DevOps portal, which should link the feature to the PI in SAFe.

</td></tr></tbody>
</table>**Related topics**  


[Troubleshooting issues for Azure DevOps integration with Agile Development](troubleshooting-issues-agile-azure-int.md)

