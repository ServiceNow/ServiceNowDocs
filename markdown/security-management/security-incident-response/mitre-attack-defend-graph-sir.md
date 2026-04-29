---
title: MITRE attack and defend technique graph
description: The MITRE attack and defend technique graph provides security analysts with an interactive, node-based visualization of attack techniques, defense techniques, and associated artifacts for a security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# MITRE attack and defend technique graph

The MITRE attack and defend technique graph provides security analysts with an interactive, node-based visualization of attack techniques, defense techniques, and associated artifacts for a security incident.

## MITRE attack and defend technique graph Overview

The MITRE attack and defend technique graph enables analysts to explore relationships between security threats and defensive measures, helping them understand the complete attack and defense landscape for an incident. The graph uses a hierarchical structure with the SIR record as the root node, branching out to display attack techniques, defend techniques, and their associated artifacts.

Analysts can interact with nodes to view details, establish associations, and manage the visibility of information based on their investigation needs. The visualization only appears when MITRE attack and defend technique data has been ingested into the system. Without ingested data, the MITRE attack and defend technique tab remains hidden from the SIR workspace.

## Graph structure

The graph consists of the following node types arranged in a hierarchical structure:

-   SIR node \(root\): The central node representing the Security Incident Response record.
-   Attack technique nodes: First or second-level nodes representing specific attack methods.
-   Defend technique nodes: First or second-level nodes representing defensive measures.
-   Artifact nodes: Second or third level nodes representing specific artifacts related to defend techniques.

Nodes at the same hierarchical level can have cross-references, creating connecting edges when the same node relates to multiple parent nodes.

## Available actions

The graph provides different actions depending on the node type being interacted with.

SIR node actions

-   **Show attack technique:** Display all attack techniques associated with the SIR.
-   **Show defend technique:** Display all defend techniques associated with the SIR.
-   **Associate attack technique:** Open a modal window to associate new attack techniques with the SIR.
-   **Associate defend technique:** Open a modal window to associate new defend techniques with the SIR.

Attack technique node actions

-   **Show details:** Opens a panel displaying the details of the selected node.
-   **Show defend techniques:** Display all defend techniques associated with this specific attack technique.
-   **Hide node:** Temporarily remove a node from the graph view. A **Show hidden nodes** option becomes available to restore hidden nodes.

Defend technique node actions

-   **Show details:** Opens a panel displaying the details of the selected node.
-   **Show defend artifacts:** Display all artifacts associated with the selected defend technique. Artifacts shared across multiple defend techniques appear as a single node with multiple connecting edges. Edge labels indicate the relationship between the defend technique and artifact.
-   **Hide node:** Temporarily remove the defend technique node from the graph view. A **Show hidden nodes** option becomes available to restore hidden nodes.

Graph-level actions

-   **Save**: Preserve the current graph view state. Saved views persist when users return to the tab. Includes node visibility, expanded sections, and layout preferences.
-   **Refresh**: Update the graph with the latest data from the backend. Updates node labels if names have changed, removes associations that have been deleted from the backend, and displays newly associated techniques not currently visible in the graph. Maintains the saved view structure while refreshing the data.
-   **Find on map**: Search for specific nodes by name. Highlights and centers the selected node in the graph. Useful for locating nodes in complex graphs with many techniques.
-   **Show hidden nodes**: Restore all nodes that have been hidden from view.

## Association actions

When associating attack or defend techniques:

-   **Select technique:** Choose from available techniques in the modal window.
-   **Save association:** Confirm and create the association. Newly associated nodes appear at the end of the graph. Use the **Find on map** function to locate newly added nodes.
-   **Cancel:** Close the modal without creating an association.

The association modal uses the same interface experience as the MITRE-ATT&amp;CK technique functionality.

## Node relationships and edges

The graph displays relationships between nodes using connecting lines \(edges\):

-   Direct associations: Lines connect parent nodes to their directly associated child nodes.
-   Shared relationships: When a defend artifact relates to multiple defend techniques, a single artifact node connects to multiple parent nodes via separate edges.
-   Cross-level references: When nodes at the same hierarchical level share relationships, connecting lines appear between them.
-   Edge labels: Labels on the edges between defend techniques and artifacts indicate the relationship type \(sourced from MITRE-ATT&amp;CK data\).

**Parent Topic:**[Working with Security Incident Records](using-analyst-workspace.md)

**Related topics**  


[Security Incident Overview section](security-incident-overview.md)

[Security Incident Details section](security-incident-details.md)

[SIR Workspace Orchestration](security-incident-response-workspace-orchestration-activities.md)

[Security Incident Response Tasks](security-incident-response-tasks.md)

[Security Incident Response Other Records](security-incident-response-other-records.md#)

[Security Incident Response Post Incident Review](security-incident-response-post-incident-review.md)

[Update information in security incident related records](../task/edit-related-records-in-list.md)

[TISC integration within SIR Workspace](../../secops-integration-threat-security-center/concept/tisc-sir-workspace.md)

[Reports in Security Incident Response](report-templates-sir.md)

[Collaborate using conference call or chat in Security Incident Response](collab-sir-call-chat.md)

[Viewing incident details with a relationship graph](sir-relationship-graph.md)

