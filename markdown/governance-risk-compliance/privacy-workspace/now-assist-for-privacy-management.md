---
title: ServiceNow Otto for Privacy Management
description: ServiceNow Otto for Privacy Management is a GenAI‑powered capability that streamlines privacy workflows by summarizing risk assessments, condensing issue details, and identifying redundant control objectives for rationalization into a common control objective.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/privacy-workspace/now-assist-for-privacy-management.html
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist for Privacy Management]
breadcrumb: [Privacy Management, Governance, Risk, and Compliance]
---

# ServiceNow Otto for Privacy Management

ServiceNow Otto for Privacy Management is a GenAI‑powered capability that streamlines privacy workflows by summarizing risk assessments, condensing issue details, and identifying redundant control objectives for rationalization into a common control objective.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see .

Privacy teams and approvers often wade through lengthy assessments, complex issue histories, and overlapping control objectives. Now Assist reduces this overhead by producing concise, actionable summaries and recommendations.

ServiceNow Otto for Privacy Management is delivered as a separate plugin. Administrators must assign the sn\_prm\_gen\_ai.user role for access.

## What ServiceNow Otto for Privacy Management does

-   Generate risk assessment summarization: ServiceNow Otto generates a summary of a privacy risk assessment based on inherent risk, residual risk, target risk, and control effectiveness. This lets approvers absorb context quickly, reducing the need to read every detail.
-   Create issue summarization: ServiceNow Otto creates a summary of an issue by analyzing its description, activity log, and remediation tasks. The summary captures the issue definition, actions taken, and tasks in progress, giving teams quick awareness about the issue.
-   Provide recommendations for similar control objectives: ServiceNow Otto identifies similar control objectives and provides recommendations that can enable you to merge the duplicate control objectives into a single, consolidated common control objective.

## Roles required

The role required to access ServiceNow Otto for Privacy Management features \(risk summaries, issue summaries, and recommendations of similar control objectives\) is sn\_prm\_gen\_ai.user.

sn\_prm\_gen\_ai.user consists of the following roles:

-   sn\_grc\_sharegenai.compliance\_library\_gen
-   sn\_grc\_sharegenai.risk\_asmt\_user
-   sn\_grc\_genai.issue\_user

