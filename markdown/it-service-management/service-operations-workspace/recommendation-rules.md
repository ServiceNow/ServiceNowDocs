---
title: Recommendation rules for an incident in Service Operations Workspace
description: Recommendations for an incident are based on rules defined in Recommendation Framework.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Reference, Service Operations Workspace for ITSM, IT Service Management]
---

# Recommendation rules for an incident in Service Operations Workspace

Recommendations for an incident are based on rules defined in Recommendation Framework.

Recommendation Framework is now deprecated and no longer supported or available for new activation. Recommended Actions for ITSM feature provides the latest experience for this functionality. To get the advanced version, you must install the Advanced Recommended actions for ITSM \(com.snc.uib.sow\_itsm\_ra\_advanced\) plugin and you must procure ITSM Pro package subscription.

**Note:** The best practice to get the advanced version is to install the Task Intelligence for ITSM \(com.snc.itsm\_ml\_task\) plugin and procure the ITSM Pro package subscription. For more information, see [Exploring Recommended Actions for ITSM in Service Operations Workspace](../concept/exploring-recommended-actions-for-itsm-in-service-operations-workspace.md).

For each recommendation rule to work, install the relevant plugin that installs the corresponding solution definition. Based on this solution definition, the recommendation rule predicts values or records for an incident.

For information about the plugins and the corresponding solution definitions, see [Configuring Recommendation Framework in Service Operations Workspace](../concept/set-up-recommendation-framework-sow.md).

<table id="table_atz_nn5_rsb"><thead><tr><th>

Recommendation rule

</th><th>

Solution definition

</th><th>

Incident field where the recommendation is available

</th></tr></thead><tbody><tr><td>

Assignment group recommendation

</td><td>

Incident Assignment

 Predicts values for the **Assignment group** field based on the short description of the incident.

</td><td>

Assignment group

</td></tr><tr><td>

Configuration item

</td><td>

Incident Configuration Item

 Predicts values for the **Configuration Item** field based on the short description of the incident.

</td><td>

Configuration item

</td></tr><tr><td>

Service recommendation rule

</td><td>

Incident Service

 Predicts values for the **Incident Configuration Item** field based on the short description of the incident.

</td><td>

Service

</td></tr></tbody>
</table><table id="table_x4c_dgq_xsb"><thead><tr><th>

Recommendation rule

</th><th>

Solution definition

</th><th>

Associated card group in the Recommendations panel

</th><th>

Primary action for the card group

</th><th>

Other actions for the card group

</th></tr></thead><tbody><tr><td>

Knowledge articles

</td><td>

Similar Knowledge Articles

 Predicts knowledge articles that the current incident can be linked to.

</td><td>

Knowledge articles

</td><td>

Attach: Attaches the recommended knowledge article to the current incident. On the incident record page, this article is displayed in the Attached Knowledge list of the **Related records** tab.

</td><td>

Discard: Discards the recommendation and moves it to the **History** tab in the **Recommendations** panel.

</td></tr><tr><td>

Propose major incident

</td><td>

Major Incident Recommendation

 Recommends the current incident to be proposed as a major incident.

</td><td>

Propose major incident

</td><td>

Propose major incident: Proposes the current incident as a major incident. The **Major incident state** field is set to **Proposed** for the incident.

</td><td>

View similar incidents: Displays a list of similar incidents related to the current incident. After viewing similar incidents, you can decide if the current incident can be proposed as a major incident.

</td></tr><tr><td>

Relevant problems

</td><td>

Similar Open Problems

 Predicts relevant problems that the incident can be linked to.

</td><td>

Relevant problems

</td><td>

Link problem: Links the recommended problem to the current incident. On the incident record page, this problem is displayed in the **Related Records** section of the **Details** tab.

</td><td>

Discard: Discards the recommendation and moves it to the **History** tab in the **Recommendations** panel.

</td></tr><tr><td>

Similar major incidents

</td><td>

Major Incident Recommendation

 Predicts similar active major incidents that the current incident can be linked to.

</td><td>

Similar major incidents

</td><td>

Add as a child incident: Adds the recommended incident as a parent to the current incident. On the current incident record page,the parent incident is then displayed in the **Related Records** section of the **Details** tab.

</td><td>

Discard: Discards the recommendation and moves it to the **History** tab in the **Recommendations** panel.

</td></tr><tr><td>

Similar open incidents

</td><td>

Similar Open Incidents

 Predicts similar open incidents that the current incident can be linked to.

</td><td>

Similar open incidents

</td><td>

Link as a parent incident: Adds the recommended incident as a parent to the current incident. On the current incident record page, the parent incident is then displayed in the **Related Records** section of the **Details** tab.

</td><td>

Discard: Discards the recommendation and moves it to the **History** tab in the **Recommendations** panel.

</td></tr><tr><td>

Similar resolved incidents

</td><td>

Similar Resolved Incidents

 Predicts similar resolved incidents to help with incident investigation and resolution processes.

</td><td>

Similar resolved incidents

</td><td>

Link incident: Links the recommended incident to the current incident. On the current incident record page, the linked incident is then displayed as the parent incident in the **Related Records** section of the **Details** tab.

</td><td>

Discard: Discards the recommendation and moves it to the **History** tab in the **Recommendations** panel.

</td></tr></tbody>
</table>**Parent Topic:**[Service Operations Workspace for ITSM reference](../concept/sow-reference.md)

**Related topics**  


[Service Operations Workspace for ITSM data model](sow-itsm-data-model.md)

[Components installed with Service Operations Workspace ITSM Applications](components-installed-with-sow.md)

[Components installed with Agent Client Collector for Investigation](components-installed-investigate.md)

[Components installed with Microsoft Endpoint Configuration Manager for Investigation](components-installed-mecm-adapter.md)

[Components installed with Remedial Actions Framework](components-installed-with-remediation-fw.md)

[Components installed with Metrics and CI Actions Framework](components-installed-metrics-ci-action-fw.md)

[Recommended Actions for ITSM reference](../concept/recommended-actions-for-itsm-reference.md)

[Reference section for Problem Management in Service Operations Workspace](../concept/reference-problem-management-sow.md)

[Features of the Investigation tab](features-of-investigation-tab.md)

[Extension points for batch processing in Service Operations Workspace](mra-extension-points-batch-processing-sow.md)

[Quick start tests for Incident Management in Service Operations Workspace](../../../administer/atf-quick-start-tests/reference/quick-start-tests-im-sow.md)

[Components installed with Universal Request for Service Operations Workspace](components-installed-ur-sow.md)

[Components installed with Universal Task for Service Operations Workspace](components-installed-ut-sow.md)

[Password Reset Reference](pr-sow-reference.md)

