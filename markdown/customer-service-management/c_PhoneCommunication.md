---
title: Configure voice channel
description: Configure voice as an omnichannel communication channel in ServiceNow Customer Service Management so customers can reach agents by phone from your web portal or contact center. Calls route to live and AI agents, and live agent calls appear in the CRM Workspace with chat, email, messaging, and cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/c\_PhoneCommunication.html
release: brazil
topic_type: concept
last_updated: "2026-10-09"
reading_time_minutes: 6
keywords: [voice, phone, omnichannel, configure, CTI, OpenFrame, ICC]
breadcrumb: [Configure omnichannel, Configure, Customer Service Management]
---

# Configure voice channel

Configure voice as an omnichannel communication channel in ServiceNow Customer Service Management so customers can reach agents by phone from your web portal or contact center. Calls route to live and AI agents, and live agent calls appear in the CRM Workspace with chat, email, messaging, and cases.

## Voice channel integration options

Voice channel integration in ServiceNow supports two implementation options:

-   Integrations with third-party contact center as a service \(CCaaS\) platforms through computer telephony integration \(CTI\)

    ServiceNow supports voice integration through OpenFrame and Interaction Controls Component \(ICC\) for organizations using third-party CCaaS platforms such as Amazon Connect, Genesys, Five9, 3CLogic, and others. OpenFrame embeds the CTI softphone in the CRM Workspace so agents can access call controls and presence information without leaving ServiceNow.

-   Browser-based calling through Web Real-Time Communication \(WebRTC\). See [Enable WebRTC for voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/portal-phone-widget.md) to get an overview of how WebRTC voice call works.

The following example shows a customer service journey combining voice support with omnichannel capabilities via integration with a third-party CCaaS provider using OpenFrame and ICC.

Marcus is a customer service manager at a shipping company where voice is the primary support channel. His team handles calls in a separate telephony system, disconnected from chat, email, and casework. Agents switch between tools, customers repeat information, and calls aren't visible in unified routing.

After integrating the contact center with ServiceNow Voice, agents handle calls in the CRM Workspace alongside email, chat, and cases. Advanced Work Assignment routes each call to an agent with the right skills, and the call opens an interaction record with the customer's account history, open cases, and recent interactions.

Real-time transcription and automated summaries reduce after-call work, and Marcus manages routing, presence states, wrap-up codes, and reporting for voice and digital channels in one place.

The following diagram shows the voice configuration workflow for administrators, agents, and customers when integrating with a third-party CCaaS provider.

\[Omitted image "mmasset0022518-voice-configuration-overview-landing.svg"\] Alt text: Workflow diagram of voice configuration steps for administrators, agents, and customers integrating with a third-party contact center.

## Voice configuration steps

Voice integration requires setup that depends on your contact center platform and integration approach. The following configuration steps are specific to configuring Voice for CCaaS using ICC and OpenFrame configuration.

Follow the configuration steps in the following table for an overview of voice configuration using ICC and OpenFrame integration. The Role column lists who typically performs each step.

<table id="configure-voice-channel-table-2"><thead><tr><th>

Step

</th><th>

Configuration step

</th><th>

Description

</th><th>

Role

</th></tr></thead><tbody><tr><td>

1

</td><td>

[Integrate with a CCaaS provider](https://mynow.servicenow.com/now/best-practices/assets/contact-center-integration-framework-ccif)

</td><td>

Complete the base integration with your CCaaS provider by following the Contact Center Integration Framework guide. You need a user account to download the Contact Center Integration Framework \(CCIF\) - Implementation Guide.

 Verify that your CCaaS platform supports integration with ServiceNow. The integration connects your contact center platform to your instance and supports screen pop, select-to-dial, presence synchronization, and call controls in the CRM Workspace. Agents who use the integrated voice features need the OpenFrame user \(sn\_openframe\_user\) role.

</td><td>

CSM admin

</td></tr><tr><td>

2

</td><td>

[Create an OpenFrame configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/t_CreateAnOpenFrameConfiguration.md)

</td><td>

Create an OpenFrame configuration to embed your contact center's softphone in the CRM Workspace. The configuration specifies the OpenFrame window settings, the URL that opens in OpenFrame, and the user groups that can access it. With OpenFrame, agents can manage incoming calls, outbound dialing, holds, transfers, and conference calls without leaving ServiceNow.

</td><td>

CSM admin

</td></tr><tr><td>

3

</td><td>

[Configure OpenFrame events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/openframe-cti-events.md)

</td><td>

Subscribe to OpenFrame events so that your contact center platform stays in sync with Advanced Work Assignment \(AWA\). The events report agent presence changes and work items that agents are offered, accept, or reject. OpenFrame events are enabled by default when the OpenFrame \(com.sn\_openframe\) and Advanced Work Assignment for CSM \(com.sn\_csm.awa\) plugins are installed.

</td><td>

Developer

</td></tr><tr><td>

4

</td><td>

[Implement the Interaction Controls Component \(ICC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/enable-icc-for-ccaas.md)

</td><td>

Implement prebuilt, certified CCaaS integrations available as apps on the ServiceNow Store. Use the Interaction Controls Component \(ICC\) to manage voice calls and callbacks with native controls in Workspace. Select **Enable interaction controls** on the OpenFrame configuration record. The Interaction Controls Component \(ICC\) plugin \(com.app\_interaction\_control\) and the certified plugin from your CCaaS provider must be installed.

</td><td>

CSM admin

</td></tr><tr><td>

5

</td><td>

[Integrating ServiceNow Voice with CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/integrating-ccc-csm.md) \(optional\)

</td><td>

To integrate ServiceNow Voice with your CCaaS platform, integrate with CSM to access inbound and outbound contact flows and operation handlers specific to CSM for automated case interactions. Agents can preview caller information before accepting a call and transfer calls with transcripts and interaction history.

</td><td>

CSM admin

</td></tr><tr><td>

6

</td><td>

[Activate ServiceNow Otto Skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/now-assist-for-csm/activate-now-assist-for-customer-service-management-csm-skills_0.md) \(optional\)

</td><td>

Check your entitlements to determine whether you have access to Now Assist for CSM. Activate the Call Summarization skill to generate summaries of agent-customer calls, and the Wrap-up completion skill to generate notes and suggest wrap-up codes, which reduces after-call work time. You configure and activate skills in the AI Admin Hub console. These skills are part of the broader ServiceNow Now Assist and Otto AI experience.

</td><td>

CSM admin

</td></tr><tr><td>

7

</td><td>

[Configure Real Time Transcription for ServiceNow Voice Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configure-rtt-sn-voice.md) \(optional\)

</td><td>

Configure real-time transcription so agents see a live transcript of the call in the interaction record. The CCaaS platform must provide real-time transcription; ServiceNow provides APIs to consume and display it. Live transcription reduces agent note-taking and supports post-call automation, such as call summaries.

</td><td>

CSM admin

</td></tr><tr><td>

8

</td><td>

[AI voice agents in CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/now-assist-for-csm/voice-ai-agent.md)

</td><td>

Use AI Voice Agents to complete tasks such as checking case status or creating cases through natural voice conversations, with a handoff to a Live Agent for complex issues. AI voice agents integrate with supported contact center platforms and are created and managed in AI Agent Studio. To enable customer access, install the Customer Service Management AI agent collection plugin.

</td><td>

CSM admin

</td></tr><tr><td>

9

</td><td>

[Configure Omnichannel Callback for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-omni-callback.md) \(optional\)

</td><td>

Install and configure Omnichannel Callback for Customer Service Management so your customers can request a callback from various channels such as Virtual Agent, the Customer Service Portal, and Engagement Messenger. Callback requests route through AWA to agent inbox, where agents accept and initiate the call.

</td><td>

CSM admin

</td></tr><tr><td>

10

</td><td>

[Integrate with Workforce Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configurable-servicenow-voice-cs.md) \(optional\)

</td><td>

Feed voice interaction data from your contact center platform into Workforce Optimization for Customer Service, so managers can view call metrics, recordings, transcripts, and sentiment analysis alongside other channels in Channel Management. Voice uses AWA to report data from the contact center queues. This integration requires that the platform posts voice interaction data into ServiceNow.

</td><td>

CSM admin

</td></tr></tbody>
</table>**Note:**

For WebRTC-based voice calling, which doesn't require an external contact center platform, configure the voice call widget in your Customer Service Portal or Engagement Messenger. This approach supports browser-to-browser calling without platform dependencies. For more information, see [Enable WebRTC for voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/portal-phone-widget.md).

