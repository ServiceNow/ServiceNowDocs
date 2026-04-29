---
title: Integrating Operational Sustainability Management with Socialsuite
description: Socialsuite is a platform for conducting materiality assessments. You can import material topics from Socialsuite into your ServiceNow instance and manage them in the Operational Sustainability Management application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Integrating Operational Sustainability Management with Socialsuite

Socialsuite is a platform for conducting materiality assessments. You can import material topics from Socialsuite into your ServiceNow instance and manage them in the Operational Sustainability Management application.

The integration supports both double materiality and single materiality assessments. Double materiality assesses both impact and financial materiality. Single materiality assesses either impact or financial materiality. Assessments comply with the Corporate Sustainability Reporting Directive \(CSRD\), European Sustainability Reporting Standards \(ESRS\), Global Reporting Initiative \(GRI\), and International Financial Reporting Standards \(IFRS\).

## Assessment data

The integration imports the following data from Socialsuite:

-   Material topics
-   Impact materiality scores
-   Financial materiality scores

## Integration workflow

1.  Conduct materiality assessments in Socialsuite.
2.  Sync the assessment results to your ServiceNow instance.

    For more information, see [Sync material topics from Socialsuite](sync-material-topics-from-socialsuite.md).

    The imported material topics appear in your ServiceNow instance in workflow states based on their status in Socialsuite. For details about how Socialsuite states map to the ServiceNow instance states, see [Material topic workflow and states](material-topic-workflow-and-states.md).

3.  Associate the material topics with goals and targets.

-   **[Activate Operational Sustainability Integration with Socialsuite](activate-operational-sustainability-integration-with-socialsuite.md)**  
You can activate the Operational Sustainability Integration with Socialsuite plugin \(sn\_osm\_ma\) for Operational Sustainability Management if you have the admin role. The plugin enables you to import materiality assessment results from Socialsuite for reporting and compliance.
-   **[Set Material topic selection system property](../task/set-material-topic-selection-system-property.md)**  
Set the Material topic selection system property to enable the Socialsuite integration features.
-   **[Create a Socialsuite connection](create-a-socialsuite-connection.md)**  
Create a Socialsuite connection to sync material topics and materiality assessment results from Socialsuite into your ServiceNow instance.
-   **[Sync material topics from Socialsuite](sync-material-topics-from-socialsuite.md)**  
Sync material topics from Socialsuite to import materiality assessment results into the Operational Sustainability Management application.

**Parent Topic:**[Integrating Operational Sustainability Management \(formerly ESG\) with other applications](integrate-esg.md)

**Related topics**  


[Socialsuite material topic fields](../reference/socialsuite-material-topic-fields.md)

[Socialsuite import log](../reference/socialsuite-import-log.md)

