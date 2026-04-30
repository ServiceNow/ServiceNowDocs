---
title: Formula override example
description: Use the following formula override example to craft your own formula overrides.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create custom override definitions, Setting up the Conversational Analytics dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Formula override example

Use the following formula override example to craft your own formula overrides.

## Group End State definitions

The end state of a conversation specifies how a conversation ended. For example, it could end with the user not responding, or the user closed the chat window. There are 12 default definitions of end state. For more information on conversation end states, see [Virtual Agent interaction records](../concept/va-interactions.md). The following script groups them as follows:

-   VA closed the chat session
    -   System Closed VA – User No Response
    -   System Closed VA – Topic Complete
    -   System Closed VA – Left With AI Search
    -   System closed VA – Auto Closed
    -   System Closed VA – User Never Engaged
-   Live agent closed the chat session
    -   System Closed LA – User No Response
    -   System Closed LA – Chat Complete
    -   Agent Closed LA – Clicked End/X
    -   System Closed LA – Before Agent Engagement
-   User closed the chat session
    -   User Closed LA – Clicked End/X
    -   User Closed VA – Clicked End/X
    -   User Closed LA - Before Agent Engagement

To create these groupings of the 12 end states, follow the instructions for [creating a formula override](../task/set-up-custom-definitions-pae.md) and use the following script.

```
(function calc(convGr) {
    // Returns 'System Closed VA', 'System Closed LA', 'User Closed' states.
    function getFinalEndState(state) {
        var arrayUtil = new global.ArrayUtil();
        VA_END_STATE = ['System Closed VA – User No Response',
            'System Closed VA – Topic Complete',
            'System Closed VA – Left With AI Search',
            'System closed VA – Auto Closed',
            'System Closed VA – User Never Engaged'
        ];
        LA_END_STATE = ['System Closed LA – User No Response',
            'System Closed LA – Chat Complete',
            'Agent Closed LA – Clicked End/X',
            'System Closed LA – Before Agent Engagement'
        ];
        USER_CLOSED_END_STATE = ['User Closed LA – Clicked End/X',
            'User Closed VA – Clicked End/X',
            'User Closed LA - Before Agent Engagement'
        ];
        if (state) {
            if (arrayUtil.contains(VA_END_STATE, state))
                return 'System Closed VA';

            if (arrayUtil.contains(LA_END_STATE, state))
                return 'System Closed LA';

            if (arrayUtil.contains(USER_CLOSED_END_STATE, state))
                return 'User Closed';
        }
        return state;
    }

    var conversationId = convGr.getValue('sys_id');
    var interactionGr = new GlideRecord('interaction');
    interactionGr.addQuery('channel_metadata_document', conversationId);
    interactionGr.addQuery('channel_metadata_table', 'sys_cs_conversation');
    interactionGr.query();
    if (interactionGr.next()) {
        var state = interactionGr.getValue('state');
        var reason = interactionGr.getValue('state_reason');
        var isVAChat = interactionGr.getValue('virtual_agent');
        var isLAChat = interactionGr.getValue('agent_chat');
        var endState = new CAUtil().getEndState(state, reason, isVAChat, isLAChat);
        return getFinalEndState(endState);
    }
})(convGr);

```

**Parent Topic:**[Create custom override definitions](../task/set-up-custom-definitions-pae.md)

