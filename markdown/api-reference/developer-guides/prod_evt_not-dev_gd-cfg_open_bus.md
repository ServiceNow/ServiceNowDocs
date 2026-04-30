---
title: Configure the Producer Event Notification Framework to use the Open Message Bus
description: If you have deployed or plan to deploy the Open Message Bus in your instance, you must configure the Producer Event Notification Framework for this message-bus. You can deploy this message-bus for both cloud and on-premise instances.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Producer Event Notification Framework developer guide, Developer guides, API implementation and reference]
---

# Configure the Producer Event Notification Framework to use the Open Message Bus

If you have deployed or plan to deploy the Open Message Bus in your instance, you must configure the Producer Event Notification Framework for this message-bus. You can deploy this message-bus for both cloud and on-premise instances.

## Before you begin

Role required: admin

For additional information on the publishing of messages using the open message bus, see [Producing outbound API notifications using the open message bus](https://www.servicenow.com/docs/access?context=trouble-ticket-workflow-using-pub-sub-model&version=yokohama&pubname=yokohama-proactive-service-exp-workflows&ft:locale=en-US).

## Procedure

1.  Synchronize the topics in your current message-bus with your ServiceNow instance.

    For additional information on synchronizing topics, see [Producing outbound API notifications using the open message bus](https://www.servicenow.com/docs/access?context=trouble-ticket-workflow-using-pub-sub-model&version=yokohama&pubname=yokohama-proactive-service-exp-workflows&ft:locale=en-US).

2.  Customize the [OpenMessageBusEventPublisherOOB - publishMessageToComptibleRestProxy\(Object tmfEventPayload, Array compatibleTopicArr\)](../../../../app-store/dev_portal/API_reference/OpenMessageBusEventPublisherOOB/concept/OpenMsgBusEvtPubScopedAPI.md#) method to send messages directly to a preconfigured REST action.

    This method is responsible for sending a message to the custom message platform’s REST proxy using spoke selector. The custom message platform is your message-bus through which messages are published.

    The following code example shows how to customize this method to use spoke selector flow and a custom action instead of a spoke selector.

    ```
    publishMessageToComptibleRestProxy: function(tmfEventPayload, compatibleTopicArr) {
    
      if (gs.nil(tmfEventPayload) || gs.nil(compatibleTopicArr)) {
        return;
      }
      for (var i = 0; i < compatibleTopicArr.length; i++) {
    
        // Invoking spoke selector flow which will in turn pick the rest proxy based on the input condition
        var topicGr = new GlideRecord(Constants.TABLE_TOPIC);
        topicGr.get(compatibleTopicArr[i]);
        if (!topicGr.isValidRecord()) {
          this._logger.debug("Invalid topic sys_id passed to open message publisher. Sys_id passed is " + compatibleTopicArr[i]);
          return;
        }
    
        // NOTE THAT IN THIS IMPLEMENTATION INVOKES A CUSTOM ACTION INSTEAD OF SPOKE SELECTOR
        var restProxyResponse = new sn_appss.RequestAPI(spokeSelectorRequestTypeId, spokeSelectorRequestTypeInputMap, spokeSelectorRequestTypeContextObject).execute();
    
        // var restProxyResponse = sn_fd.FlowAPI.executeActionQuick('sn_api_notif_mgmt.demo_topic_rest_proxy_response', spokeSelectorRequestTypeInputMap);
        var responseCode = restProxyResponse.response.code;
        if (Constants.REGISTRATION_RESPONSE_SUCCESS_CODES.indexOf(responseCode) == -1) {
          this._logger.logErr("Publishing message to Message bus rest proxy failed with HTTP response code " + responseCode);
        }
      }
    },
    ```

3.  Configure the REST proxy for the topics.

    After the spoke is configured, messages are published in the specified REST proxy for topics configured in the spoke.

    1.  Navigate to **All** &gt; **Spoke selector** &gt; **Request type**

    2.  Select **Topic Rest Proxy Outbound Request**.

    3.  Select the tab **Integration request definitions**.

    4.  Create an integration request definition entry to configure the spoke.

        You can also refer to the **Demo Rest Proxy Response Def** entry for additional guidance.


