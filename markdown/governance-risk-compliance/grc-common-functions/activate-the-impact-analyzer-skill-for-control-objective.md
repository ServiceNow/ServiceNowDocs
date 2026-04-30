---
title: Activate the control objective impact analyzer skill
description: Enable the control objective impact analyzer skill from the Now Assist Skills page. When this skill is activated, the system uses generative AI to identify control objectives that should be updated based on the modified citation details.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Activate the control objective impact analyzer skill

Enable the control objective impact analyzer skill from the Now Assist Skills page. When this skill is activated, the system uses generative AI to identify control objectives that should be updated based on the modified citation details.

## Before you begin

Role required: sn\_grc\_sharegenai.compliance\_library\_gen\_ai\_user

## About this task

To recommend impacted control objectives, predefined similarity parameters are used. The generative AI analyzes the updated description and supplemental guidance of the citation and identifies which control objectives need updates based on relevance.

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **Now Assist Admin** &gt; **Skills**.

2.  On the **Now Assist Skills** tab, under the Technology workflow group, select **Risk &amp; Sustainability**.

3.  Under the control objective impact analyzer skill, select **Activate skill**.

4.  Review the information on **General details** tab and select **Save and Continue**.

    The **General Details** tab is in read-only mode and lists the name, description, and additional details about the skill.

5.  Review the **Define access** tab and select **Save and Continue**.

    The **Define access** tab is in read-only mode and lists the access control lists \(ACLs\) and role restrictions for the skill.

6.  On the **Review and Activate** tab, select **Activate**.

    The **Review and Activate** tab displays information about who can access the skill and the data and resources \(tables and roles\) that the skill can access.

    A skill activation success message appears. After the skill is activated, the **Analyze change** button becomes available on the citation page for users with the appropriate access.


