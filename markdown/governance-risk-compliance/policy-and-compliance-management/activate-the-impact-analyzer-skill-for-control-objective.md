---
title: Activate the Control Objective Impact Analyzer skill
description: Enable the Control Objective Impact Analyzer skill from Now Assist Skills page. When this skill is activated, the system uses Generative AI to identify control objectives that should be updated based on the modified citation details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/policy-and-compliance-management/activate-the-impact-analyzer-skill-for-control-objective.html
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for Integrated Risk Management \(IRM\), Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Activate the Control Objective Impact Analyzer skill

Enable the Control Objective Impact Analyzer skill from Now Assist Skills page. When this skill is activated, the system uses Generative AI to identify control objectives that should be updated based on the modified citation details.

## Before you begin

Role required: sn\_grc\_sharegenai.compliance\_library\_gen\_ai\_user

## About this task

To recommend impacted control objectives, predefined similarity parameters are used. The Generative AI analyzes the updated description and supplemental guidance of the citation and Identifies which control objectives need updates based on relevance.

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **AI Admin Hub**.

2.  In the **AI Skills** tab, navigate to **Technology** &gt; **Risk &amp; Sustainability**.

3.  Under the control objective impact analyzer skill, select **Activate skill**.

4.  Review the information in **General details** tab and select **Save and Continue**.

    The General Details tab is in read-only mode and lists the name, description, and additional details about the skill.

5.  Review the **Define access** tab and select **Save and Continue**.

    The Define access tab is in read-only mode and lists the Access control lists \(ACLs\) and role restrictions to the skill.

6.  On the **Review and Activate** tab, select **Activate**.

    The Review and Activate tab displays information about who can access the skill and the data and resources \(tables and roles\) that the skill can access.

    A skill activation success message appears. After the skill is activated, the **Analyze change** button is available on the citation page for users with the appropriate access.


