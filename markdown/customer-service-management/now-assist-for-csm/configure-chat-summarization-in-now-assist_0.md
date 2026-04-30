---
title: Configure chat summarization
description: Configure Chat Summarization to generate condensed summaries of conversations between agents or with a Virtual Agent, highlighting key points for quick reference.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Configure chat summarization

Configure Chat Summarization to generate condensed summaries of conversations between agents or with a Virtual Agent, highlighting key points for quick reference.

Configure the chat summarization skill 

## Before you begin

Role required: Admin

Chat summarizations are generated when:

-   The conversation ends.
-   The agent uses the summarize quick action in Agent Chat.
-   The user selects chat summarization or enters summarize chat in the Ask Now Assist field on the Now Assist panel.
-   A live agent transfers an interaction to a different live agent.

    When an interaction is transferred from a Virtual Agent to a live agent and is at least six lines long, the chat summarization displays in a summary card in the conversation and populates the interaction's summarization and short description fields.


## Procedure

1.  Navigate to **Admin &gt; Now Assist Admin &gt; Now Assist Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate Skill for the **Chat Summarization** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **Define Triggers** and switch the toggles to choose how and when the summarization is configured.

    |Trigger|Description|
    |-------|-----------|
    |Virtual Agent to Live Agent handoff|Chat summary that is generated when the chat handoff is done from Virtual Agent to a live agent.|
    |Live Agent to Live Agent handoff|Chat summary that is generated when the chat handoff is done from a live agent to a live agent.|
    |Quick action|Chat summary that is generated when the live agent performs the `/summarize` quick action.|
    |Chat wrap-up|Chat summary that is generated when the live agent ends the chat. The **Chat Summary** field is updated for the interaction.|
    |Short description|**Short description** field that is updated for the interaction when the live agent ends the chat.|
    |Task creation|**Short description** and **Description** fields that are auto-populated on the task record when a task is created from an interaction.|

    You can also toggle the bulleted list property to display the chat summary as an unordered list.

5.  Select **Choose Input** and review the portal and channel selections that determines where data is pulled from.

    **Note:** You cannot modify or deselect the default product portal data source. Additionally, portals that are already in use by other products cannot be selected.

<table id="id_xlz_fhc_4fc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input fields

</td><td>

-   CSM \(Default portal for CSM\)
-   CSP \(Default portal for CSM\)
-   AIS\_ADMIN\_TOOLS
-   APM
-   APM\_PLANNER
-   ARC
-   ASC
-   ASC\_OLD
-   ASP
-   ASSIGN\_INSIGHTS\_OWNER
-   BENCHMARKS
-   BLANK
-   BLSP
-   BUSINESS\_PORTAL
-   CAB
-   CEM
-   CLAROTY\_CTD\_VR
-   CLOUD\_ADMIN\_PORTAL
-   CLOUD\_PORTAL
-   COMMUNITY
-   COMMUNITY\_CXS
-   CONTENT\_DELIVERY\_DEMO
-   CSM\_OUTLOOK
-   CSM\_WALKUP
-   DB\_BUILDER
-   DEMO\_BUILDER
-   DH\_TOOLS
-   DHAPP
-   DHAPP\_DSP
-   DHBE
-   DHEXECON
-   ECDEMO\_KIOSK
-   ECK
-   EESP
-   ELP
-   EMEXP
-   ESG\_REPORTING
-   FSMCP
-   IDEA
-   INDEMO
-   INDUSTRY
-   INDUSTRYDEMO
-   KB
-   KIOSK
-   LEGAL
-   LEGAL\_OUTLOOK
-   LMP
-   MEB
-   MESP
-   MOA
-   MY\_WORK\_HUB
-   NEW\_HIRE
-   PC
-   PERF
-   PPSRP
-   PPSWORKBENCH
-   PPT
-   PROGRAM\_STATUS
-   PROJECT\_STATUS
-   RC
-   SNCOUTLOOK
-   SP
-   SP\_CONFIG
-   SUPPLIER
-   SVDP
-   SWP
-   TCP
-   WALKUP
-   WS
-   WSDDEMO
-   ECDEMO
-   ECKDEMO
-   ESC
-   ESCP


</td></tr></tbody>
</table>6.  Select **Define Availability** to customize how and when the skill capability is active and accessible.

    -   Select **Skill is always available** so no restrictions are placed on when a skill is available.
    -   Select **Customize skill availability** to define conditions and use the condition builder to configure fields and values.
7.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default roles sn\_customerservice\_agent and sn\_customerservice.consumer\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

8.  Select **Display** to determine where the resolution notes appear.

    -   Select **In-product desktop** to display Now Assist skills on forms and workspaces.
    -   Select **Now Assist panel** to display Now Assist skills in the Now Assist panel.
9.  After selecting **Review and Activate** to examine changes, select **Done** to close the Chat Summarization generation settings.

10. Select **Skill** to turn on the skill for agents and complete the configuration.


