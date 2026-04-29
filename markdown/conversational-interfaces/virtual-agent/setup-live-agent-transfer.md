---
title: Sync agents to set up live agent transfer
description: After the installation and configuration of Amazon Connect, you must sync agents to enable live transfer. You can sync agents stored in Amazon Connect with the agents on your ServiceNow agents.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Conversational IVR with Amazon Connect, Configuring Conversational IVR with Amazon Connect, Conversational IVR with Amazon Connect, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Sync agents to set up live agent transfer

After the installation and configuration of Amazon Connect, you must sync agents to enable live transfer. You can sync agents stored in Amazon Connect with the agents on your ServiceNow agents.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **Virtual Agent**.

2.  On the Virtual Agent Settings page, navigate to the Configure your interactive voice response \(IVR\) section and click **Configure IVR** under Configure pre-built adapter.

3.  On the Configure interactive voice response page, select **VA Amazon Connect Adapter Provider** from the Select IVR service provider drop-down.

4.  Under Provider Channel Identities, select the identity provider that you want to sync agents for.

5.  On the Amazon Connect information form, in the Sync your call center agents tile, click **Sync agents**.

6.  Add the following roles to the agents to sync them with your ServiceNow instance and the Amazon Connect account.

    -   sn\_va\_as\_service.contact\_center\_api
    -   awa\_agent
    -   interaction\_agent
    -   agent\_workspace\_user
    -   sn\_openframe\_user
    -   awa\_integration\_user
    Add each user, who must handle a Live Agent Transfer, to the Agent Phone Group by navigating to **System Security** &gt; **Users and Groups** &gt; **Groups**.

7.  In the filter navigation bar on your ServiceNow instance, enter `awa_presence_state.list` to find the Presence States table.

8.  Open the **Available** state, move the **Phone** Service Channel from the Available field to the Selected field and click **Update**.

    Login as the synced user and make sure that the agent is available in Agent Workspace and also login to the Amazon Connect instance with the same ServiceNow user to verify.


**Parent Topic:**[Configure Conversational IVR with Amazon Connect](configure-va-ivr.md)

