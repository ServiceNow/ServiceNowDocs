---
title: OpenFrame events for work items, agent presence, and interactions
description: Use OpenFrame events to achieve better integration between Advanced Work Assignment \(AWA\) and Computer telephony integration \(CTI\) and aide in improved call routing.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Phone channel, Configure, Enable communication channels, Configure, Customer Service Management]
---

# OpenFrame events for work items, agent presence, and interactions

Use OpenFrame events to achieve better integration between Advanced Work Assignment \(AWA\) and Computer telephony integration \(CTI\) and aide in improved call routing.

OpenFrame events are enabled by default when your administrator installs the Openframe plugin \(com.sn\_openframe\) and Advanced Work Assignment for CSM plugin \(com.sn\_csm.awa\).

**Note:** The Advanced Work Assignment for CSM \(com.sn\_csm.awa\) plugin is automatically installed with the Customer Service plugin \(com.sn\_customerservice\).

As a CTI developer, ensure that you subscribe to the following events by using the subscribe method of the openFrameAPI.​ For more information, see [openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

|Event|Description|
|-----|-----------|
|openframe\_awa\_agent\_presence|Events are sent to OpenFrame when an agent's presence state changes.|
|openframe\_awa\_workitem\_offered|Events are sent to OpenFrame when a work item is offered to an agent.|
|openframe\_awa\_workitem\_accepted|Events are sent to OpenFrame when a work item is accepted by an agent.|
|openframe\_awa\_workitem\_rejected|Events are sent to OpenFrame when a work item is rejected by an agent.|
|openframe\_agent\_off\_interaction|Events are sent to OpenFrame indicating the presence of an agent on chat as off or available.|

Add and activate an OpenFrame configuration by navigating to **OpenFrame** &gt; **Configurations**. For more information, see [Create an OpenFrame configuration](../task/t_CreateAnOpenFrameConfiguration.md).

## Sample payloads

Refer to the sample payloads for each event as described in the following table.

<table id="table_xgj_vhg_x4b"><thead><tr><th>

Event

</th><th>

Sample payload

</th></tr></thead><tbody><tr><td>

openframe\_awa\_agent\_presence

</td><td>

```
{
  "result":{
    "presence":{
      "name":"Available",
      "sys_id":"0b10223c57a313005baaaa65ef94f970",
      "available":true,
      "channels":[
        {
          "name":"Case",
          "available":true,
          "sys_id":"d4a675e3739713004a905ee515f6a7e7",
          "restrict_update":false
        },
        {
          "name":"Phone",
          "available":true,
          "sys_id":"f6281cc39335330090813a53177ffb32",
          "restrict_update":false
        },
        {
          "name":"Chat",
          "available":true,
          "sys_id":"27f675e3739713004a905ee515f6a7c3",
          "restrict_update":false
        }
      ]
    }
  }
}
 
```

</td></tr><tr><td>

openframe\_awa\_workitem\_offered

</td><td>

```
{
  "result": {
    "workItem": {
      "sys_id": "14c86c40a1650610f87701807d9bc0be",
      "size": 1,
      "serviceChannel": {
        "name": "Chat",
        "sys_id": "27f675e3739713004a905ee515f6a7c3"
      },
      "document": {
        "sys_id": "aa582040a1650610f87701807d9bc076",
        "table": "interaction"
      },
      "previousWorkItem": "7c78a440a1650610f87701807d9bc02b",
      "isQueueTransferred": true,
      "isAutoAccepted": true
    }
  }
}
```

</td></tr><tr><td>

openframe\_awa\_workitem\_accepted

</td><td>

```
{
  "result": {
    "workItem": {
      "sys_id": "14c86c40a1650610f87701807d9bc0be",
      "size": 1,
      "serviceChannel": {
        "name": "Chat",
        "sys_id": "27f675e3739713004a905ee515f6a7c3"
      },
      "document": {
        "sys_id": "aa582040a1650610f87701807d9bc076",
        "table": "interaction"
      },
      "previousWorkItem": "7c78a440a1650610f87701807d9bc02b",
      "isQueueTransferred": true,
      "isAutoAccepted": true
    }
  }
}
```

</td></tr><tr><td>

openframe\_awa\_workitem\_rejected

</td><td>

```
{
   "payload":{
      "workItem":{
         "sys_id":"66c4071d1bf66410b8e3ea06624bcb59",
         "size":1,
         "serviceChannel":{
            "name":"Case",
            "sys_id":"d4a675e3739713004a905ee515f6a7e7"
         },
         "document":{
            "sys_id":"b6a4c31d1bf66410b8e3ea06624bcb93",
            "table":"sn_customerservice_case"
         },
         "rejection":{
            "reason":"Not my expertise",
            "sys_id":"31e3fa29b38023002e7b6e5f26a8dc17"
         }
      }
   }
}
```

</td></tr><tr><td>

openframe\_agent\_off\_interaction

</td><td>

```
{
   "result":{
      "interaction":{
         "sys_id":"da1dc9651bbe6410b8e3ea06624bcb51",
         "number":"IMS0000050",
         "type":"chat",
         "reason":"INTERACTION_INACTIVE"
      }
   }
}
```

</td></tr></tbody>
</table>**Related topics**  


[OpenFrame overview](c_OpenFrameOverview.md)

