---
title: Skill Recommendation components in Workforce Optimization for ITSM
description: Workforce Optimization for ITSM uses roles to administer skill recommendation, tables to store skill data, and properties to modify default behavior, and scheduled job to recommend skills in configurable Workforce Optimization for ITSM.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Skills Management in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Skill Recommendation components in Workforce Optimization for ITSM

Workforce Optimization for ITSM uses roles to administer skill recommendation, tables to store skill data, and properties to modify default behavior, and scheduled job to recommend skills in configurable Workforce Optimization for ITSM.

## Roles

<table id="id_ihj_xzg_jvb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Skill Recommendation User \[sn\_sre.user\]

</td><td>

Grants rights to view skill recommendation tables.

</td><td>

wfo.user

</td></tr><tr><td>

Skill Recommendation Admin \[sn\_sre.admin\]

</td><td>

Grants administrative rights to edit the properties for skill recommendation.

</td><td>

-   wfo.admin
-   sn\_sre.user

</td></tr></tbody>
</table>## Properties

Navigate to **Skill Recommendation** &gt; **Configuration** to configure these properties.

<table id="table_zhp_cdq_dlb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable skill recommendation.

sn\_sre.enable\_skill\_recommendation

</td><td>

Enable this property to start recommending skills for agents.-   **Type:**true \| false
-   **Default value:**true

</td></tr><tr><td>

Maximum number of skills to predict based on supervised learning.

sn\_sre.max\_supervised\_skills

</td><td>

Using supervised learning, the maximum number of skills to predict for each incident ordered by confidence of prediction.-   **Type:**Integer
-   **Default value:**3

</td></tr><tr><td>

Maximum number of skills to predict based on supervised learning.

sn\_sre.max\_unsupervised\_skills

</td><td>

Using unsupervised learning, the maximum number of skills to predict for each incident ordered by confidence of prediction.-   **Type:**Integer
-   **Default value:**3

</td></tr><tr><td>

Number of resolved similar tasks to use for predicting skills.

sn\_sre.number\_of\_similar\_incidents

</td><td>

The number of resolved similar incidents to use to predict skills using supervised learning, ordered by confidence of prediction, to resolve similar types of incidents.-   **Type:**Integer
-   **Default value:**15

</td></tr><tr><td>

Number of times Predictive Intelligence must predict the same skill for an agent before recommending it for the agent.

sn\_sre.user\_predicted\_skill\_threshold

</td><td>

The number of times Predictive Intelligence must predict the same skill for an agent before recommending the skill for the agent. -   **Type:**Integer
-   **Default value:**20

</td></tr><tr><td>

Similarity solution definition to recommend skills from similar incidents.

sn\_sre.unsupervised\_solution\_definition\_for\_incidents

</td><td>

Name of the Predictive Intelligence solution definition used for predicting skills to resolve incidents using unsupervised learning. If you have created your own solution definition, you can replace the default one with the one you have created.-   **Type:**String
-   **Default value:**ml\_sn\_sn\_sre\_global\_recommend\_similar\_skills\_for\_incidents

</td></tr><tr><td>

Similarity solution definition to recommend skills for incidents.

sn\_sre.supervised\_solution\_definition\_for\_incidents

</td><td>

Name of the Predictive Intelligence solution definition used for predicting skills to resolve incidents using supervised learning. If you have created your own solution definition, you can replace the default one with the one you have created.-   **Type:**String
-   **Default value:**ml\_sn\_sn\_sre\_global\_recommend\_skills\_from\_similar\_incidents

</td></tr></tbody>
</table>## Scheduled job

|Scheduled job|Description|
|-------------|-----------|
|Start skill prediction|Runs the job every day at 1 AM on all incidents that were closed the previous day. Recommends the skills used to close the incidents to resolve similar open incidents.|

## Tables

<table id="table_gkk_4hd_llb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Predicted Skill \[sn\_sre\_user\_predicted\_skill\]

</td><td>

-   Stores how many times a skill has been predicted for the user.
-   Skills not recommended in the last 60 days are automatically deleted from this table.

</td></tr><tr><td>

Task Predicted Skill \[sn\_sre\_task\_predicted\_skill\]

</td><td>

-   Stores the skills predicted to resolve each type of incident.
-   Tables created over 60 days ago are automatically deleted from this table.

</td></tr></tbody>
</table>**Parent Topic:**[Skills Management in Workforce Optimization for ITSM](../concept/skills-management-wfo-itsm.md)

