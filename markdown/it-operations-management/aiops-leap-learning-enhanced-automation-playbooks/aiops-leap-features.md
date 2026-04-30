---
title: AIOps LEAP features
description: AIOps LEAP includes features such as grouping incidents, creating problem records, and generating playbooks.
locale: en-US
release: xanadu
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2025-03-17"
reading_time_minutes: 1
breadcrumb: [Exploring AIOps LEAP, AIOps Learning Enhanced Automation Playbook \(LEAP\), Now Assist for IT Operations Management \(ITOM\), IT Operations Management]
---

# AIOps LEAP features

AIOps LEAP includes features such as grouping incidents, creating problem records, and generating playbooks.

-   **Incident clustering and comprehensive summaries**

    AIOps LEAP categorizes IT incidents based on short descriptions and assignment groups. It uses historical data to summarize issues into actionable resolutions. AIOps LEAP consolidates information from different incidents to help with decision making and serves as a repository of knowledge.

-   **Grouping incidents using the ServiceNow® Group Action Framework \(GAF\) plugin**

    AIOps LEAP uses the GAF plugin to organize and group incidents based on specific parameters. These groups, referred to as clusters or automation opportunities, are created by analyzing incident data, such as work notes and resolution notes. AIOps LEAP uses these automation opportunities to generate resolution steps to help solve similar future incidents. The automation architects can pin required automation opportunity records for easy access or to filter records for further analysis. Automation architects can use the pinned records to conduct root cause analysis. They can create problem records and identify patterns to streamline resolutions and improve overall efficiency.

-   **Automation recommendations and playbook generation**

    AIOps LEAP identifies frequent issues and offers automation recommendations to address them. It creates actionable playbooks based on historical data and resolution workflows. Additionally, it builds a knowledge base by documenting workflows and solutions through detailed resolution steps, enabling further analysis, learning, and continuous improvement. These resolution steps can be shared across teams to facilitate collaboration and operational efficiency, even without formal playbook creation. Thus, automated playbook generation is a valuable output of the AIOps LEAP platform.

    AIOps LEAP uses prioritization logic to automatically group and prioritize incidents depending on how critical the service is, number of handoffs, and incident information. The logic helps you to target high-impact issues. For new users, during initial setup, AIOps LEAP generates resolution steps for the top 50 priority groups.

-   **Automation feedback and tracking**

    The Automation opportunity details page has a Comments and Activity section. An automation architect can include comments for the selected automation opportunity. Operators can also add comments about insufficient or missing resolution steps, a playbook failing to work, and so on. Each activity for the selected automation opportunity is logged in the Activity section. The section includes filters for field changes, post types, and flagged changes that help you to narrow your search. You can view all the action that happens for the automation opportunity.


