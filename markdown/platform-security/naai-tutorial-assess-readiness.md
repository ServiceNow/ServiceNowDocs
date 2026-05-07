---
title: Assess readiness
description: Verify that your instance is prepared for AI agent deployment, install the required applications, assign the required roles, and classify user identity types before you begin building.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 2
breadcrumb: [Create and secure an AI agent in Now Assist, Agentic AI security and governance]
---

# Assess readiness

Verify that your instance is prepared for AI agent deployment, install the required applications, assign the required roles, and classify user identity types before you begin building.

Before building an AI agent, verify that your instance meets the technical and organizational requirements for deployment. Identifying and resolving gaps now helps to prevent blockers during the build and testing stages.

## Run the readiness evaluation

The Now Assist Readiness Evaluation app automates the process of checking whether your instance is ready for generative AI and agentic AI deployment. It identifies configuration gaps, data readiness issues, and customizations that could affect your implementation, and provides direct links to resolve each issue. Activate the Now Assist Readiness Evaluation \[sn\_assess\] plugin to use this feature. Learn more about this evaluation at Now Assist Readiness Evaluation.

**Important:** Don't proceed until all blocking issues identified by the readiness evaluation have been resolved.

## Install required applications

Verify that the following application is installed on your instance before proceeding.

-   **Now Assist Admin Console \[__sn\_nowassist\_admin__\]**

    Provides the **sn\_nowassist\_admin.nsa\_admin** and **sn\_generative\_ai.data\_steward** roles. Install from the ServiceNow Store. See .


**Note:** Now Assist Admin Console requires a ServiceNow Pro Plus or Enterprise Plus license and AI Search enabled on your instance. Review the application listing in the ServiceNow Store for full dependency and licensing requirements before installing.

## Assign roles

Once the required applications are installed, assign the following roles to the people who will build, configure, and manage AI agents.

-   **__sn\_aia.admin__**

    Required to create, configure, and manage AI agents and agentic workflows in AI Agent Studio.

-   **__sn\_nowassist\_admin.nsa\_admin__**

    Required to configure Now Assist Admin settings, activate guardrails, and manage privacy policies.

-   **__sn\_generative\_ai.data\_steward__**

    Required to make data sharing decisions and configure privacy policies. Assign this role before configuring data protection settings in [Configure security controls](naai-tutorial-configure-security.md).


For a full list of roles installed with Now Assist, see [Now Assist Admin roles](https://www.servicenow.com/docs/access?context=roles-installed-with-now-assist-admin&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Classify user identity types

The ServiceNow AI Platform uses the **Identity type** field on the User \[**sys\_user**\] table to distinguish between human users, AI agent users, and machine accounts. Classifying users correctly before you build ensures that your access control and role masking configuration works as intended.

For any dedicated AI user accounts your agents will run as, set the Identity type to **AI Agent**. Existing human user records default to **Unclassified** until updated. Records with the web service account flag set to true are automatically classified as **Machine**.

## Next step

When your instance passes the readiness evaluation and roles are assigned, proceed to [Plan your agent](naai-tutorial-plan-agent.md).

**Parent Topic:**[Create and secure an AI agent in Now Assist](naai-tutorial-overview.md)

